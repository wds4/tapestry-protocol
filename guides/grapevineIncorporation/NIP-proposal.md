Proposed NIP
======

Contextual Trust Attestations as the foundation for a Web of Trust
-------------------------------

`draft` 

## Background 

Many platforms use various proxy indicators of trust, most commonly follows and mute lists, to calculate "web of trust" scores. The purpose of this NIP is to initiate the transition from proxy indicators of trust to explicit, contextual trust attestations. The long-term goal will be to enable Alice's web of trust to calculate of an array of `Trust Scores` for any given user and for any given context. 

Ultimately, trust in a broad context should imply trust in all sub-contexts, unless stated otherwise. For example: if Alice attests that Bob 

## Trust Attestations

Trust attestation will take the following form:

```json
{
  trustAttestationData: {
    ratee: pk_ratee,
    score: 100, // 0 means DO NOT trust; 100 means TRUST
    confidence: 80, // OPTIONAL; number between 0 and 100 percent
    context: {
      action: naddr_action,
      category: naddr_category
    }
  }
}
```

The above json will be stringified and placed into the content of a note as described below.

## Event kinds and tags

Trust attestations, actions, and categories will be encoded as kind 399201 events with the d-tag used to specify whether the event is an attestation, a kind, or a category.

Example: 

```json
{
  content: stringified_json, // see above
  tags: [
    [d, "trustAttestation"]
  ],
  kind: 399201,
}
```

## Trust Scores

The calculation of trust scores using trust attestations as raw data will be the topic of a separate NIP. 
