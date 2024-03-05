DCoConcepts
=====

## Synopsis

DCoConcepts makes use of preexisting curatio protocols to curate a concept.

## Discussion

DCoConcepts makes use of preexisting curatio protocols to curate a concept:
- DCoG-objectPropertyTrees to curate the json schema
- DCoG-categories to organize the instances of the concept into a category tree

The `concept` node contains fields that specify whatever details are needed to implement the above curation in a consistent fashion (e.g. specialized relationship types in place of the defaults defined by this TIP: `isASPecificInstanceOf` and `isASubsetOf`, etc). The end user can choose to follow or ignore those suggestions, but will probably want to follow them.
