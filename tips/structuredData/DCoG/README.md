back to [curation of structured data main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/structuredData/README.md)

DCoSG
=====
Decentralized Curation of Simple Graphs
-----

## Synopsis

Use DCoSL to curate one simple list, a list for nodes, and one slighlty modified list, one for edges (modified because several customized fields are required to specify an edge).

## User actions

The user can perform the following actions:
- create a new graph, which will have a name, a description; an optional list of allowed nodes; and an optional list of allowed relationship Types
- create a node for the list
- create a relationship for the list
- endorse or reject any individual node as belonging or not belonging to the graph
- endorse or reject any individual relationship as belonging or not belonging to the graph
- endorse or reject any individual entity as a curator of this particular graph

## relevant word types

## relevant relationship types

- endorsesAsACuratorOfTheGraph (or reject-)
- endorsesAsANodeInTheGraph (or reject-)
- endorsesAsARelationshipInTheGraph (or reject-)

## attestations

There are three primary types of attestations:
- Alice endorses (or rejects) X as an node of the graph G
- Alice endorses (or rejects) R as a relationship of the graph G
- Alice endorses (or rejects) Bob as a curator of the graph G

Secondary attestation types:
- Alice endorses (or rejects) that node A and node B are duplicates and should be merged

## Calculations

Each user will have an influence score in the context of curation of this graph.

Each node and each relationship will have a score which is used to partition each into 3 bins: accepted, rejected, and pending.

## Control Panel

The user will have the ability to control the following:
- default user (graph curator) scores
- default graph node and relationship scores
- cutoff scores (used to segregate nodes and relationships into bins)
- option of whether or not to accept a node that belongs to a relationship that is accepted even if the node itself is not accepted
