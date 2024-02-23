back to [TIPs: Core Protocol main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/core-protocol/README.md)

### TIP-0.1.1
the Grapevine: curation of knowledge using the web of trust
=====

`draft` `author:wds4`

## Synopsis

The tapestry protocol will provide methods for entities to delegate curation of knowledge to the web of trust, referred to as the *Grapevine*, and will be done so in a manner designed to pair well with the Concept Graph.

## Discussion

The general idea is that the Concept Graph will be used to formulate questions, and the Grapevine can be used to answer them.

*Curation of knowledge* refers to various categories:
- answers to linguistic (pseudo-arbitrary) questions, e.g.: what do we call a particular object?
- answers to subjective questions, e.g.: what is the best movie of all time?
- answers to objective questions, e.g.: is the moon made of cheese?

## Example

An example of a pseudo-arbitrary question would be the one in the following figure: *How do we indicate the timestampt of a nostr event?*

<img src="../../images/createdAtQuestionAsGraph.png" width="50%" />

As shown in the figure, the question is represented by a single node (circles with green background). Each individual of several propsoed answers is represented by individual nodes (circles with red borders). The answers are grouped into a set using edges that connect the question to each answer. Two different connection methods are used. On the left, the question is connected directly to each propsoed answer. On the right, the question is connected to each proposed answer by a specialized path, called a class thread, consisting of two or more edges in sequence. The method on the right has the advantage that answers can be organized into subsets (circles with thin borders). Class threads will be discussed in detail in a later TIP.

