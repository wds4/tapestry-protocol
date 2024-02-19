Tapestry Implementation Proposals (TIPs)
=====

## A note on pseudo-arbitrary decisions and the organization of the protocol into TIPS

Many *pseudo-arbitary* decisions are required to build out a fully functioning tapestry protocol. An example is that this protocol makes extensive use of JSON rather than, say, XML. 

We require there to be no *pseudo-arbitrary* decisions to be included withint the core tapestry protocol, defined as TIPs 0.x. If a TIP requires any *pseudo-arbitrary* decision to be made, it must be 1.x or higher. One of the goals of organization is to place as much of the protocol as possible into the core. In the biological world, many decentralized languages exist: English, Chinese, etc; and within them, many dialects exist, with varying degrees of overlap. We envision the same will be true in the digital world, with multiple languages and dialects existing, with varying degrees of overlap.

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
