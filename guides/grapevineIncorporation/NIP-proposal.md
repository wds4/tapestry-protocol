Proposed NIP
======

Contextual Trust Attestations as the foundation for a Web of Trust
-------------------------------

`draft` 

## Background 

Many nostr platforms today use various proxy indicators of trust, most commonly follows and mute lists but also including likes, zaps, etc, to calculate "web of trust" scores. The purpose of this NIP is to initiate the transition from proxy indicators of trust to *explicit attestations of context-specific trust*, referred to in this document as `Trust Attestations`, as a replacement for proxy indicators of trust.

The long-term goal will be to enable Alice to calculate an array of `Trust Scores` for any given user and for any given context, and that these `Trust Scores` will be used for a variety of purposes. However, how *exactly* a `Trust Score` should be calculated, and how *exactly* it should be used, is intentionally left out of this NIP. We anticipate that `Trust Attestations` and other pieces of data defined in this NIP will be useful for a variety of purposes: content filters, data vending machines, calculation of WoT scores, categorization of content, etc. It is important to stress that different users and platforms must have the freedom to process data in whatever ways they see fit. Nevertheless, for the sake of presenting a complete picture, we do outline in broad brushstrokes (below) ONE way that context-specific `Trust Scores` could be calculated.

This NIP includes specification of a method to represent context, as well as a method to indicate parent-child relationships between those contexts. Trust in a broad (parent) context should be assumed to imply trust in all child contexts, unless stated otherwise. For example: if Alice endorses Bob as trustworthy to rate and recommend movies, this will automatically imply that he is trustworthy to rate and recommend comedies, dramas, and sci-fi movies, without the need to make an independent attestation for each child context. But if she issues an additional attestation that Bob shouild NOT be trusted to recommend comedies, her more specific attestation will override the more general one. This will enable trust to be as fine-grained or as coarse-grained as we want it to be, which is something that cannot be achieved reliably using proxy data. If the context fields are left out of a `Trust Attestation`, it is assumed to apply to the superset of all contexts.

We anticipate that in the beginning, users will issue `Trust Attestations` predominantly in very broadly defined contexts (e.g.: Alice trusts Bob to curate nostr content in all nostr apps and platforms), will issue predominantly endorsements, will issue them publicly, and will make them transitive. As time goes on, users may discover the need for more focused contexts (e.g.: *Alice trusts Bob to curate Wikifreedia articles*), for attestations with a low score (e.g. *Alice does NOT trust Bob to curate Wikifreedia articles in the category of politics*), for attestations that are private rather than public, and for attestations that are not transitive (e.g. Alice trusts Bob to curate Wikifreedia articles himself, but does NOT trust him to rate other users' trustworthiness to curate Wikifreedia articles).

# word types

This NIP will make user of four types of data: `trust attestations`, `actions`, `categories`, and `relationships`, with the option to add more data types in the future if deemed necessary. We will rely upon only two event kinds: 33902 and 9902, depending on whether we desire parameterized replaceable events or regular events.

## Contexts

Context will be represented using two dimensions: the `action` dimension and the `category` dimension. Example: Alice may endorse Bob as trustworthy (or not trustworthy) `to rate and recommend movies` (the `action`) in the category of `dramas` (the `category`). If left unspecified, the supersets of all `actions` and all `categories` will be presumed.

We anticipate that if a platform, such as Wikifreedia, were to incorporate this NIP for the first time, then a small handful of relevant "starter" `actions` and `categories` will be created by the developer, if they have not already been created. For example, the Wikifreedia developer may create the single `action`: `to curate content on WikiFreedia`, and perhaps a small handful of `categories`: `electronics`, `sports`, `history`, `politics`, `entertainment`. In the case of Wikifreedia, individual articles may be assigned to individual `categories`, perhaps by the article authors. Eventually, users will be given the opportunity to submit and utilize additional `actions` and `categories`, so that there will be no need to rely upon developers to do so. 

## Context: actions and categories

### actions

Examples of `actions` include:
- to curate content on nostr (in all platforms)
- to curate content on WikiFreedia
- to rate and recommend products
- to sell products
- to rate and recommend movies
- to create movies
- to edit movies
- to produce movies
- to give advice

An action will be formatted using JSON according to the following example:

```json
{
  "contextActionData": {
    "name": "to rate and recommend",
    "description": "lorem ipsum",
  }
}
```

### categories

Examples of `categories` include:
- movies
- comedies
- electronics
- smartphones

A category will be formatted using JSON according to the following example:

```json
{
  "contextCategoryData": {
    "name": "movies",
    "description": "lorem ipsum",
  }
}
```

Each action and category will be wrapped into a note and referenced by naddr (or note id?). JSON will be stringified and included into the content field. Tags ("d" tag?) will also be used to encode the name of each action and each category.

## Organizing contexts into hierarchies

Users will submit `relationships` to indicate the parent-child relationship between a pair of actions or between a pair of categories, formatted according to the following two examples:

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

Trust attestations, actions, categories, and relationships will be encoded as kind 39902 (parameterized replaceable) event OR a kind 9902 (regular) event.

### Trust Attestations

`Trust Attestations` will use parameterized replaceable events (kind 39902), and will include the following tags.
- The (required) `wordType`-tag specifies whether the event is a `trust attestation`, an `action`, a `category`, or a `relationship`.
- The (required) `p`-tag indicates the pubkey of the ratee.
- The (required) `action`-tag specifies the action, and can be either the name, the naddr, or the note id of the action
- The (required) `category`-tag specifies the category, and can be either the name, the naddr, or the note id of the category
- The (optional) `score`-tag specifies the score, and is an integer between 0 and 100
- The (optional) `confidence`-tag specifies the confidence, and is an integer between 0 and 100 (percent)
- The (optional) `tr`-tag specifies whether the attestation is transitive and takes values `true` or `false`; if left absent, the default is `true`.

As a paraterized replaceable event, `Trust Attestations` must also include an "a" tag, which will be a concatenation of:
- the `wordType`-tag, i.e. "trustAttestation"
- the pubkey of the ratee 
- the naddr (or note id?) of the action
- the naddr (or note id?) of the category

Example: 

```json
{
  "content": "{ trustAttestationData: { ... } }", // stringified json 
  "tags": [
    ["wordType", "trustAttestation"], // options: trustAttestation, action, category, relationship
    ["p", pk_ratee],
    ["action", "to rate and recommend movies"], // may use the naddr or the note id of the action instead of the name
    ["category", "comedies"], // may use the naddr or the note id of the category instead of the name
    ["a","trustAttestation-"pk_ratee-naddr_action-naddr_category],
    ["score", 100],
    ["confidence", 80],
    ["tr", true], // true or false; default is true
  ],
  "kind": 39901, // or 9902
}
```

### Actions

_work in progress_

### Categories

_work in progress_

### Relationships

_work in progress_

## Private attestations

Users may be given the option of creating attestations that are private. When choosing this option, the stringified JSON will be encrypted, and the encrypted file will be placed in the content field in place of the stringified JSON. The user will also be presented with the following additional options:
- encrypt the tags field in its entirety. This
- encrypt a subset of the tags. this will allow the attestation to be searchable without revealing its full contents; e.g. it will be known publicly that Alice created an attestation regarding Bob, but the score (endorse versus block) will be encrypted.

## Trust Scores

Trust scores are calculated using trust attestations as raw data. Any statement of a Trust Score must include the `context`, the `score` itself, and the `confidence` in that score. In other words, its format parallels that of the Trust Attestation (above). The fact that Trust Attestations ("I know X from personal experience") and Trust Scores ("I am merely passing along what my web of trust tells me") are formatted similarly will enable *plausible deniability*.

Details of how Trust Scores are calculated will be the topic of a separate NIP. In general, the `score` should be calculated as a weighted average of trust attestations from all trusted sources, with the weights being functions of the `influence` of the rating authors, optionally multiplied by the confidence of the rating itself. The `confidence` in the Trust Score will be calculated according to the principles outlined in [this post](https://habla.news/a/naddr1qqxnzdes8q6rwv3hxs6rjvpeqgs98k45ww24g26dl8yatvefx3qrkaglp2yzu6dm3hv2vcxl822lqtgrqsqqqa28kn8wur). Influence of any given user will be calculated using the relevant Trust Score as the produce of the `score` and the `confidence` in that score.

