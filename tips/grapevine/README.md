back to the [TIPs main page](..)

### TIPS 2.x

The Grapevine
=====

## Grapevine Basics: TIPs 2.0.x
- [TIP-2.0.x](intent.md) purpose of the Grapevine
- [TIP-2.0.x](influence.md) influence
- [TIP-2.0.x](context/context.md) context
  -  dimensions:
      -  [TIP-2.0.x](context/action.md) the action dimension
      -  [TIP-2.0.x](context/category.md) the category dimension
- [TIP-2.0.x](value.md) the value dimension (highest quality, most virtuous, speediest delivery, etc) - form the basis of DCAS

## ratings and attestations: TIPs 2.1.x
- [TIP-2.1.x](attestations/attestations.md) attestations (requires a rater)
- [TIP-2.1.1](attestations/ratings.md) ratings (requires a ratee)
- [TIP-2.1.2](attestations/context.md) context (for trust ratings, other ratings, other purposes)
- [TIP-2.1.3.0](attestations/fields.md) fields for ratings
  - [TIP-2.1.3.1](attestations/comments.md) comments
  - [TIP-2.1.3.2](attestations/confidence.md) confidence
  - [TIP-2.1.3.3](attestations/comments.md) numerical fields: 0-100, 5star, binary, flag (none), etc (needs a context ???)
  - [TIP-2.1.3.5](attestations/comments.md) bundling multiple fields into standardized fieldsets
    - [TIP-2.1.3.5.0](attestations/comments.md) the trust rating fieldset
    - [TIP-2.1.3.5.1](attestations/comments.md) the standard 5-star rating fieldset
- [TIP-2.1.x]() rating templates
- [TIP-2.1.x]() trust ratings

## composite scores: TIPs 2.2.x
- ## the basics of calculating average scores: TIPs 2.2.0.x
  - [TIP-2.2.x]() the general idea of average scores (rated items, trust scores, whatever): 4 numbers
  - [TIP-2.2.x]() ambiguity by design: my rating versus my grapevine's rating
  - [TIP-2.2.x](compositeScores/averageScore.md) average score: averages are weighted
  - [TIP-2.2.x](compositeScores/weight.md) weight
  - [TIP-2.2.x](compositeScores/input.md) input
  - [TIP-2.2.x](compositeScores/certainty.md) certainty: a function of input
  - [TIP-2.2.x](compositeScores/influence.md) influence = average * certainty

- ## influence: TIPs 2.2.1.x
  - [2.1.2](influence/trustAttestations.md) trust attestations
  - [2.1.0](influence/influence.md) influence = average * certainty
  - [2.1.1](influence/context.md) trust context
  - [2.1.1](influence/inheritance.md) inheritance

- ## regular scores (not trust scores)
  - []() scoring systems
    - []() 5-star
    - []() 0-100 scale

- ## Trust Scores
  - []() components of the trust score

- ## sybil mitigation strategies for trust scores
  - default user trust score
  - attenuation factor

- ## special topics: TIPs.2.2.1.x
  - []() default averages
  - []() inheritance down the category tree
  - []() weights (default: context tells us which influence score to use; but you can adjust it in more complicated fashion)

- ## control panel: TIPs 2.2.3.x
  - [2.1.x](controlPanel/attenuationFactor.md) attenuation factor
  - [2.1.x](controlPanel/rigor.md) rigor
  - [2.1.x](controlPanel/defaultScores.md) default user trust scores
  - [2.1.x](controlPanel/defaultScores.md) default rated item scores

## Grapevine word types
- [TIP-2.wordTypes.attestations](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/attestation): attestations
- [TIP-2.wordTypes.ratings](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/rating): ratings
  - [TIP-2.wordTypes.trustRatings](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/trustRating): trust rating
- [TIP-2.wordTypes.contexts](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/context): context
  - [TIP-2.wordTypes.contextDimenstions](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/contextDimension): dimension of a context
  - [TIP-2.wordTypes.categories](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/contextCategory): category (dimension of context)
  - [TIP-2.wordTypes.actions](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/contextAction): action (dimension of context)
- [TIP-2.wordTypes.values](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/value): value
  - [TIP-2.wordTypes.valueAxes](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/valueAxis): axis of value
  - [TIP-2.wordTypes.valueAxes](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/valueCategory): category (axis of value)
 
## Grapevine relationship types
