back to [curation of structured data main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/structuredData/README.md)

DCAS
=====
Decentralized Composite Average Score
-----

## Synopsis

For every rating with a primary numeric field, there is a corresponding Composite Average Score.

## Discussion

DCAS is a sub-protocol that allows a community to rank the `items` of a `simple list` (or the `instances` of a `concept`) along an `axis` (specifically, a `value axis`), from some maximum score to some minimum score. Only certain types of ratings qualify as input for DCAS; specifcally, an attestation that specifies an axis and either an list or a concept. For example, a rating that asks to rank the best coffee shops in some small town. The axis would be: best quality coffee shops; and the list (or concept) would correspond to the list of coffee shops in the town in question.

## User actions

Users can rate an item on a list (or an instance of a concept) using a rating system that is value-aware.

## Attestation type

link to the relevant ratingType that will be used for DCAS

## Calculations

- average score
- input
- certainty
