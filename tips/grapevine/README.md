back to the [TIPs main page](..)

Grapevine: TIPs 2.x
=====

## Grapevine Basics: TIPs 2.0.x
- [2.0.0](intent.md) statement of intent
- [2.0.1](influence.md) influence
- [2.0.2](context.md) context

## ratings and attestations: TIPs 2.1.x
- [2.1.0](attestations/attestations.md) attestations (requires a rater)
- [2.1.1](attestations/ratings.md) ratings (requires a ratee)
- [2.1.2](attestations/context.md) context for trust ratings
- [2.1.3.0](attestations/fields.md) fields for ratings
  - [2.1.3.1](attestations/comments.md) comments
  - [2.1.3.2](attestations/confidence.md) confidence
  - [2.1.3.3](attestations/comments.md) numerical fields: 0-100, 5star, binary, flag (none), etc (needs a context ???)
  - [2.1.3.4](attestations/comments.md) rating context
  - [2.1.3.5](attestations/comments.md) bundling multiple fields into fieldsets
    - [2.1.3.5.0](attestations/comments.md) the trust rating fieldset
    - [2.1.3.5.1](attestations/comments.md) the standard 5-star rating fieldset

## composite scores: TIPs 2.2.x
- ## the basics of calculating average scores: TIPs 2.2.0.x
  - (is average score as a data structure distinct from the previous TIPs?)
  - []() the general idea of average scores (rated items, trust scores, whatever): 4 numbers
  - []() ambiguity by design: my rating versus my grapevine's rating
  - [2.1.x](compositeScores/averageScore.md) average score
  - [2.1.x](compositeScores/weight.md) weight
  - [2.1.x](compositeScores/input.md) input
  - [2.1.x](compositeScores/certainty.md) certainty

- ## influence: TIPs 2.2.1.x
  - [2.1.2](influence/trustAttestations.md) trust attestations
  - [2.1.0](influence/influence.md) influence = average * certainty
  - [2.1.1](influence/context.md) trust context
  - [2.1.1](influence/inheritance.md) inheritance

- ## special topics: TIPs.2.2.1.x
  - []() default averages
  - []() inheritance down the category tree
  - []() weights (default: context tells us which influence score to use; but you can adjust it in more complicated fashion)

- ## control panel: TIPs 2.2.3.x
  - [2.1.x](controlPanel/attenuationFactor.md) attenuation factor
  - [2.1.x](controlPanel/rigor.md) rigor
  - [2.1.x](controlPanel/defaultScores.md) default user trust scores
  - [2.1.x](controlPanel/defaultScores.md) default rated item scores

## data structures: TIPs 2.3.x
- [2.3.0](dataStructures/dataStructures.md) Basic idea: start with simple data structures, gradually get more complex

- ## DCoSL: decentralized composite average scores: TIPs 2.3.1.x
  - [2.3.1.0](dataStructures/simpleRanking/simpleRanking.md) intro to composite average score
  - [2.3.1.1]() 
  - [2.3.1.2]()

- ## DCoSL: decentralized curation of simple lists: TIPs 2.3.2.x
  - [2.3.2.0](dataStructures/DCoSL/DCoSL.md) DCoSL intro
  - [2.3.2.1]() average score subtype
  - [2.3.2.2]() cutoff parameters

- ## DCoG: decentralized curation of graphs: TIPs 2.3.3.x
  - [2.3.3.0](dataStructures/DCoSL/DCoSL.md) DCoG intro
  - [2.3.3.1]() 
  - [2.3.3.2]()
  - ## DCoG-DAG: decentralized curation of graphs that are DAGs and have a master node and one type of relationship type (action, category, subset)
  - ## DCoG-property: DCoG for property tree

- ## curation of a concept
- ## curation of schemas (as per schema.org)
- ## content algorithms (rank a list by score)
  - multivariable (weight by more than one quality score, weight for age of content, etc)

*old, being deprecated*:
- 2.0.1 - components of the trust ratings
- 2.0.2 - averages are weighted
- 2.0.3 - default user trust scores
- 2.0.4 - control panel
- 2.0.0.x - trust scores
- 2.0.0.0.x - components of trust scores
- 2.0.0.0.1 - average scores
- 2.0.0.0.2 - input
- 2.0.0.0.2 - certainty
- 2.0.0.0.3 - influence = average * certainty
- 2.0.0.1.x - sybil mitigation strategies
- 2.0.0.1.1 - attenuation factor
- 2.0.0.1.2 - default user trust scores
- 2.0.0.1.3 -

## regular (non-trust) ratings
- scoring systems
- 5-star
- 0-100 scale
- 2.0.0.4.x - context basics
- 2.0.0.4.1 - context: two dimensions
- 2.1.x - algorithms and equations
- 2.1.0 - calculation of certainty from input

## new word types
- attestation
- rating
- trust rating
- category (dimension of context)
- action (dimension of context)

## data visualization
