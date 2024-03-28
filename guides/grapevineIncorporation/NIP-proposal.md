Proposed NIP
======

Contextual Trust Attestations as the foundation for a Web of Trust
-------------------------------

`draft` 

## Background 

Many platforms use various proxy indicators of trust, most commonly follows and mute lists, to calculate "web of trust" scores. The purpose of this NIP is to initiate the transition from proxy indicators of trust to *contextual trust attestations* as the raw data used to calculate trust scores. The long-term goal will be to enable Alice's web of trust to calculate an array of `Trust Scores` for any given user and for any given context.

Trust in a broad context should imply trust in all sub-contexts, unless stated otherwise. For example: if Alice endorses Bob as trustworthy to recommend movies, this will automatically imply that he is trustworthy to rate and recommend comedies, dramas, and sci-fi movies, without the need to make an independent attestation for each sub-context. This will enable trust to be as fine-grained or as coarse-grained as we want it to be, which is something that cannot be achieved reliably using proxy data.

## Contexts

Context will be represented using two dimensions: the action dimension and the category dimension.

Example: Alice may endorse Bob as trustworthy (or not trustworthy) to rate and recommend movies (the action) in the category of dramas (the category). If left unspecified, the set of all actions and all categories will be the default.

## Context: actions and categories

```json
{
  "contextActionData": {
    "name": "to rate and recommend",
    "description": "lorem ipsum",
  }
}
```

```json
{
  "contextCategoryData": {
    "name": "movies",
    "description": "lorem ipsum",
  }
}
```

Each action and category will be wrapped into a note and referenced by naddr.

## Hierarchies

```json
{
  "relationshipData": {
    "nodeFrom": naddr_for_comedies,
    "relationshipType": "isASubcategoryOf",
    "nodeTo": naddr_for_movies,
  }
}
```

```json
{
  "relationshipData": {
    "nodeFrom": naddr_for_toProduceMovies
    "relationshipType": "isASubcategoryOf",
    "nodeTo": naddr_for_toCreateMovies
  }
}
```

## Trust Attestations

A trust attestation will take the following form:

```json
{
  "trustAttestationData": {
    "ratee": pk_ratee,
    "score": 100, // 0 means DO NOT trust; 100 means TRUST
    "confidence": 80, // OPTIONAL; number between 0 and 100 percent
    "context": {
      "action": naddr_action,
      "category": naddr_category
    }
  }
}
```

The above json will be stringified and placed into the content of a note as described below.

## Event kinds and tags

Trust attestations, actions, categories, and relationships will be encoded as kind 399201 events with the d-tag used to specify whether the event is an attestation, a kind, or a category.

Example: 

```json
{
  "content": "{ trustAttestationData: { ... } }", // stringified json 
  "tags": [
    [d, "trustAttestation"] // options: trustAttestation, contextAction, contextCategory, relationship
  ],
  "kind": 399201,
}
```

## Trust Scores

Trust scores are calculated using trust attestations as raw data. Any statement of a Trust Score must include the `context`, the `score` itself, and the `confidence` in that score. In other words, its format parallels that of the Trust Attestation (above). 

Details of how trust scores are calculated will be the topic of a separate NIP.

