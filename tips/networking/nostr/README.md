back to [networking main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/networking/README.md)

### TIPs 3.1.x

Data storage & retrieval: nostr
=====
How to use nostr to store and retrieve *words* efficiently and effectively
-----

## Background

As per the relevant TIP, a *word* is a node that is formatted using json. This set of TIPs describes how to store, transmit, and retrieve words from the nostr network.

## Concept Graph-specific: TIPs 3.1.0.x

- #### publication of words: TIPs 3.1.0.0.x
  - [TIP-3.1.0.0.0](publication.md): publication of a word over nostr
  - [TIP-3.1.0.0.1](kinds.md): event kinds
  - [TIP-3.1.0.0.2](tags.md): event tags
  - [TIP-3.1.0.0.3](publicationByWordType.md): publication of a word over nostr with specification of wordType

- ### retrieval of words: TIPs 3.1.0.1
  - [TIP-3.1.0.1](retrieval.md): retrieval of a word from the nostr network

- ### metadata: TIPs 3.1.0.2
  - [TIP-3.1.0.2](.md): what goes into wordData.metaData.nostr

- ### stewardship: TIPs 3.1.0.3
  - [TIP-3.1.0.3](.md): stewardship

- ### relays: TIPs 3.1.0.4
  - [TIP-3.1.0.4](relays.md) relays

## Grapevine-specific: TIPs 3.1.1.x

- [TIP-3.1.1.0](.md): publication of an attestation over nostr
- [TIP-3.1.1.1](.md): alternate formatting and publication over nostr using [NIP-32](https://github.com/staab/nips/blob/nip-32-labeling/32.md)

## Work in progress

Divide publication to nostr into multiple DIPs. Each publication method has its own task slug and uses its own set of tags, to assist in retrieval of data. For example: createInstance allows you to put the name of the parent list or parent concept in a tag, to make it easier to search for all items on that parricular list or concept.

- createWord: publish a word (simplest)
- createInstance: publish a word as an item (= an instance) on a particular list. 
