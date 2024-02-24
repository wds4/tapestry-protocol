back to the [TIPs main page](..)

Grapevine: TIPs 2.x
=====

## Grapevine Basics: TIPs 2.0.x
- [2.0.0](intent.md) statement of intent
- [2.0.0](influence.md) influence
- [2.0.1](context.md) context

## ratings and attestations: TIPs 2.1.x
- [2.1.2](attestations/attestations.md) attestations (requires a rater)
- [2.1.2](attestations/ratings.md) ratings (requires a ratee)
- [2.1.1](attestations/context.md) context for trust ratings
- [2.1.2](attestations/fields.md) fields
  - [2.1.2](attestations/comments.md) comments
  - [2.1.2](attestations/confidence.md) confidence
  - [2.1.2](attestations/comments.md) numerical fields: 0-100, 5star, binary, flag (none), etc (needs a context ???)
  - [2.1.2](attestations/comments.md) rating context
  - [2.1.2](attestations/comments.md) bundling fields into fieldsets
    - [2.1.2](attestations/comments.md) the trust rating fieldset

## calculating average scores: TIPs 2.2.0.x
- [2.1.x](compositeScores/averageScore.md) average score
- [2.1.x](compositeScores/weight.md) weight
- [2.1.x](compositeScores/input.md) input
- [2.1.x](compositeScores/certainty.md) certainty

## influence: TIPs 2.3.x
- [2.1.2](influence/trustAttestations.md) trust attestations
- [2.1.0](influence/influence.md) influence = average * certainty
- [2.1.1](influence/context.md) trust context
- [2.1.1](influence/inheritance.md) inheritance

## control panel: TIPs 2.4.x
- [2.1.x](controlPanel/attenuationFactor.md) attenuation factor
- [2.1.x](controlPanel/attenuationFactor.md) rigor
- [2.1.x](controlPanel/defaultScores.md) default user trust scores

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
