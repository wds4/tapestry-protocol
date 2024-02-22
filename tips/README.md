back to the [tapestry protocol main page](https://github.com/wds4/tapestry-protocol/blob/main/README.md)

Tapestry Implementation Proposals (TIPs)
=====

## [Core Protocol: TIPs 0.x](core-protocol)

We review the underlying principles of the protocol and introduce the concept graph and the grapevine, which are developed in detail in the sections that follow. Although subsequent sections require the incorporation of some [linguistic burden](https://github.com/wds4/tapestry-protocol/blob/main/glossary/linguisticOverhead.md) -- e.g., we make heavy use of json for data files -- the core protocol is designed to contribute minimal, or arguably zero, linguistic burden to the overall protocol. Variations on the tapestry protocol, such as variations that rely upon xml in place of json, could therefore be imagined which adopt the core protocol as is.

## [Concept Graph: TIPs 1.x](concept-graph)

The concept graph achieves *knowledge representation* by organizing information into a graph, governed by a handful of linguistic-overhead-minimizing *principles of organization* which provide structure to the graph.

## [Grapevine: TIPs 2.x](grapevine)

The Grapevine achieves *knowledge curation* using the web of trust in a manner designed to integrate naturally with the Concept Graph.

## [Networking: TIPs 3.x](networking)

A section of the protocol is dedicated to the storage and transmission of data using [nostr](https://github.com/nostr-protocol/nostr). TIPs for additional networks (e.g., IPFS, GUN) can be added later. Multiple networks can be used simultaneously for the sake of redundancy.

## Subprotocols

A subprotocol is a subset of TIPs which serve a particular purpose.

- [DCoSL](subprotocols/DCoSL.md): decentralized curation of simple lists
- [DCoG](subprotocols/DCoG.md): decentralized curation of graphs
  - [DCoG-cat](subprotocols/DCoG-cat.md): DCoG for set trees or category trees



