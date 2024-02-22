back to [TIPs: Core Protocol main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/core-protocol/README.md)

TIP-0.1.0
=====

knowledge is represented as a graph
---

`draft` `author:wds4`

## Synopsis

Knowledge will be broken down into chunks, called nodes, and organized as a graph, which is a collection of nodes connected by edges. Edges will represent relationships between the nodes and will be used to organize nodes into sets. Linguistic questions can be formulated by representing individually proposed answers as nodes and arranging them into a set.

<img src="../../images/createdAtQuestionAsGraph.png" width="50%" />

The above figure illustrates two methods that a pseudo-arbitrary question can be represented using this TIP.

## General Discussion

In the [Tapestry Protocol](https://github.com/wds4/tapestry-protocol/blob/main/glossary/tapestryProtocol.md), data is represented using [graphs](https://github.com/wds4/tapestry-protocol/blob/main/glossary/graph.md), which is a collection of [nodes](https://github.com/wds4/tapestry-protocol/blob/main/glossary/node.md) and [edges](https://github.com/wds4/tapestry-protocol/blob/main/glossary/relationship.md). A [concept graph](https://github.com/wds4/tapestry-protocol/blob/main/glossary/conceptGraph.md) is a graph with additional structure provided by [principles of organization](https://github.com/wds4/tapestry-protocol/blob/main/glossary/principleOfOrganization.md) such as the [class thread princiuple](https://github.com/wds4/tapestry-protocol/blob/main/glossary/classThreadPrinciple.md), as described though this series of TIPs.


## Knowledge Representation

This TIP is about the *representation* of knowledge, as opposed to knowledge *curation*, which is the next TIP.

## Nodes

A Node is any piece of information, of any size, in any format. It can be analog or digital, binary or trinary. 

For the most part, we will be restricing our attention to data in the form of objects, using [json](https://www.json.org), and will be relying heavily upon [json schema](https://json-schema.org) to keep track of their formats. But in principle, a node could represent data files in other formats, such as XML, CSV, SQL, TXT, etc. A node could even represent the information recorded on a physical object: a book, a piece of paper, the back of a napkin, puffs of smoke in the air.

If you don't like json or json schema, realize that DCoSL can be readily reformulated using some alternative to json, or with json but using some alternative to json schema, while keeping the overall structure and approach of DCoSL intact.

## Sets

Methods will be developed in subsequent TIPs to organize nodes into sets, which may also be termed groups, categories, lists, etc.

## Edges

An edge, a.k.a a relationship, is a connection between two nodes. Like a node, an edge contains information. But unlike a node, the amount of information stored in an edge is kept to a minimum. Each edge has a small handful of attributes:
- Each edge is dirrectional or undirected.
- Each edge has an identifier which is a string.

## How to ask a linguistic ("pseudo-arbitrary") question using this TIP

### Example

created_at vs createdAt vs CreatedAt

(show figure of graph with nodes, universal identifier for the organizing node)

### Additional Examples: digital realm

Further examples of linguistic questions

- binary vs trinary
- json vs XML

### Additional Examples: biological realm

What do you call this (picture of a pencil)

## Questions that are not pseudo arbitrary

We make note of the fact that this method allows us to ask questions that are not pseudo arbitrary, such as questions of fact. 

## Pseudo arbitrary decisions

We argue the pseudo-arbitrary burden is small.

## Notes

Although the graphs used in the tapestry protocol are not technically a "graph database", many of the ideas and principles are the same.

