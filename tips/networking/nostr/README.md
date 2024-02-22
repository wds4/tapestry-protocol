back to [networking main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/networking/README.md)

Data storage & retrieval: nostr
=====
How to use nostr to store and retrieve data (nodes, words) efficiently and effectively
-----

## Concept Graph-specific

- [TIP-3.1.x](.md): what goes into wordData.metaData.nostr
- [TIP-3.1.x](publication.md): publication of a word over nostr
- [TIP-3.1.x](.md): retrieval of a word from the nostr network
- [TIP-3.1.x](.md): stewardship

## Grapevine-specific

- [TIP-](.md): publication of an attestation over nostr
- [TIP-](.md): alternate formatting and publication over nostr using [NIP-32](https://github.com/staab/nips/blob/nip-32-labeling/32.md)

## Work in progress

Divide publication to nostr into multiple DIPs. Each publication method has its own task slug and uses its own set of tags, to assist in retrieval of data. For example: createInstance allows you to put the name of the parent list or parent concept in a tag, to make it easier to search for all items on that parricular list or concept.

- createWord: publish a word (simplest)
- createInstance: publish a word as an item (= an instance) on a particular list. 
