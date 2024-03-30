back to the [glossary main page](https://github.com/wds4/tapestry-protocol/blob/main/glossary/README.md)

pseudo arbitrary
=====

## Definition 

A *pseudo-arbitrary* question is one with the following characteristics:
- It has a large number of perfectly acceptable answers.
- It is vitally important for everyone in a community to settle on the same answer.
- There is no Schelling point that points everyone to the same answer.

Canonical pseudo-arbitrary questions are questions pertaining to _language_, where the question at hand is what symbol we should use to represent some thought or idea.

Example: The string we use to represent the timestamp of a [nostr event](https://github.com/nostr-protocol/nips/blob/master/01.md) is pseudo-arbitrary. *created_at*, *createdAt*, or *CreatedAt* are all perfectly reasonable answeres, so which answer we pick is _arbitrary_. For most of us, the overriding concern is that we want to communicate with others, which means most of us use the same string that everyone else is already using: *created_at*.

The prefix "pseudo" is meant to imply that there may be some small subset of entities who do express a strong preference among the various alternatives which are deemed more or less equivalent in terms of acceptability by the majority of entities. In the example above, there are presumably some subset of developers who have strong opinions on the relative merits of snake_case, UppserCamelCase, lowerCamelCase. According to the theory of decentralized language, this small subset of entities may become the drivers of whatever solution ends up gaining wide acceptance by the community.

## Synonyms

We may use the term *linguistic* and *pseudo-arbitrary* interchangeably, since we model a language as consisting of a long series of pseudo-arbitrary questions or choices (with answers).

## Discussion

Questions can be pseudo arbitrary for several reasons. One reason could be that various alternatives are genuinely equally acceptable from the perspective of the individual entity. Another reason could be that some reasons are marginally more acceptable than others, but only marginally so, and being on the same page as the majority is deemed by the individual to be more important. A third reason could be that the relative acceptability of various alternatives is unknown by the individual entity, but the entitiy estimates that the amount of effort it would require to evaluate the acceptability of various options makes it not worth the expenditure. Such may often be the case in the digital realm, where evaluating the relative acceptability of various options would require an entity who does not know how to code to learn to do so, and then to become an expert in the question at hand.

## Examples

*Digital realm*:
- whether to use *created_at*, *createdAt*, or *CreatedAt* to indicate the timestamp of a [nostr event](https://github.com/nostr-protocol/nips/blob/master/01.md)
- whether to encode nostr events as json or xml
- whether a digital system should be binary or trinary

*Biological realm*:
- the word for pencil could just as well be pen or rock or cheese or any one of a large configuration of letters and sounds
- whether a writing system should be phonetic (e.g., English) or logographic (e.g., Chinese)

## Significance

The concept of pseudo arbitrary questions is central to the theory of decentralized language, according to which all pseudo arbitrary questions are curated by your web of trust and are not stewarded.
