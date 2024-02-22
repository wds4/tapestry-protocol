Tapestry Implementation Proposals (TIPs)
=====

## Motivation

This work was motivated by the observation that web of trust cannot successfully curate content, facts and information if it does not simultaneously curate the digital tools that are used to communicate about those things. 

## Purpost 

The tapestry protocol was developed as a tool to create the world's first [decentralized digital languages]().

## A note on organization

Many [pseudo-arbitary](https://github.com/wds4/tapestry-protocol/blob/main/glossary/pseudoArbitrary.md) decisions are required to build out a fully functioning tapestry protocol. An example is that this protocol makes extensive use of JSON rather than, say, XML. We will place as much of the protocol as possible into the core (TIPs 0.x), with the requirement that the core must contain no *pseudo-arbitrary* decisions. If a TIP requires any *pseudo-arbitrary* decision to be made, it must be pushed to 1.x or higher.

## [Core Protocol: TIPs 0.x](core-protocol)

## [Concept Graph: TIPs 1.x](concept-graph)

## [Grapevine: TIPs 2.x](grapevine)

## [Networking: TIPs 3.x](networking)

### Tables

- [word types](tables/wordTypes.md)
- [relationship types](tables/relationshipTypes.md)
- [principles of organization](tables/principlesOfOrganization.md)
- table of nostr id (& IPFS hashes?) for published words

### Folders
- folder for each word type: 
- page for JSON Schema 
- page for example of word of that type

### Subprotocols

A subprotocol is a subset of TIPs which serve a particular purpose.

- [DCoSL](subprotocols/DCoSL.md): decentralized curation of simple lists
- [DCoG](subprotocols/DCoG.md): decentralized curation of graphs
  - [DCoG-cat](subprotocols/DCoG-cat.md): DCoG for set trees or category trees
