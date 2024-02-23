back to [networking main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/networking/README.md)

Data storage & retrieval: nostr
=====
How to use nostr to store and retrieve data (nodes, words) efficiently and effectively
-----

## Concept Graph-specific

#### publication: TIPs 3.1.0.x
- [TIP-3.1.0.0](publication.md): publication of a word over nostr
- [TIP-3.1.0.x](kinds.md): event kinds
- [TIP-3.1.0.x](tags.md): event tags
- [TIP-3.1.0.1](publicationByWordType.md): publication of a word over nostr with specification of wordType

### retrieval: TIPs 3.1.1.x
- [TIP-3.1.1.0](retrieval.md): retrieval of a word from the nostr network

metadata
- [TIP-3.1.2](.md): what goes into wordData.metaData.nostr

stewardship
- [TIP-3.1.3](.md): stewardship

### misc topics
- [TIP-3.2.0](relays.md)

## Grapevine-specific

- [TIP-](.md): publication of an attestation over nostr
- [TIP-](.md): alternate formatting and publication over nostr using [NIP-32](https://github.com/staab/nips/blob/nip-32-labeling/32.md)

## Work in progress

Divide publication to nostr into multiple DIPs. Each publication method has its own task slug and uses its own set of tags, to assist in retrieval of data. For example: createInstance allows you to put the name of the parent list or parent concept in a tag, to make it easier to search for all items on that parricular list or concept.

- createWord: publish a word (simplest)
- createInstance: publish a word as an item (= an instance) on a particular list. 
