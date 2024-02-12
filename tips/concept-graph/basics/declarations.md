back to [TIPs for the Concept Graph main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/concept-graph/README.md)

TIP-1.0.3
=====
declarations
---

`draft` `author:wds4`

## Synopsis

The `declaration` of a `concept` refers to the addition or inclusion of that `concept` into a specific `concept graph`.

## declaration methods:

- create new concept
- importation of an existing concept

### creation of a new concept

A user can be said to `declare` a new concept by supplying the minimum amount of information (generally considered to be the singular and plural forms of the concept name, slug, and/or title, as well as a concept description; see the relevant TIP for `word type`) required to create a new `word type` and by indicating that the new concept should be added to a specific concept graph.

The existence of a specific `word type` in a concept graph should be presumed to trigger the creation of the entire concept and full cohort of nodes, including the `superset` node, `JSON Schema` node, etc, if they do not already exist.

### incorporation of an existing concept

The addition or inclusion of a preexisting `word type` to a concept graph is equivalent to the declaration of a new concept, if that concept does not already exist. For example: the inclusion of the `word type`: `dog` in a concept graph is sufficient to declare the concept of `dog`.

