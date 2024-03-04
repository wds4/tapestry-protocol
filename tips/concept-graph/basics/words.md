back to [TIPs for the Concept Graph main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/concept-graph/README.md)

TIP-1.0.2
=====

words
---

`draft` `author:wds4`

## Synopsis

A `word` is a node of a graph that is formatted in json.

## Instantiations

There will be several instantiations that a word can take, the two main ones being:
- the instantiation of a word inside a concept graph
- the instantiation of a word being communicated from one entity to another, or to a community of entities

When inside a concept graph, there will be a lot of information stored within a word that is determined by its relationship to other words inside the concept graph.

A major question will be how to divide concept graph-specific data from the essential, or core, data of the word.

One option will be that concept graph specific data will be stored within a field called metaData, and that every top-level field in a word can have a metaData field. In addition, there may be one or more top-level fields that are dedicated to concept graph specific data. In Plex, globalDynamicData and metaData served in this capacity.
