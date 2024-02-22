back to [TIPs: Core Protocol main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/core-protocol/README.md)

### TIP-0.0.3
no scraped data
=====

`draft` `author:wds4`

## Synopsis

Trust and reputation scores should rely more heavily on explicit, intentional attestations rather than inferred from observations or "scraped" data.

## General principle

Explicit attestations, such as the statement: *Alice trusts Bob to rate movies*, will be the primary source of data for the calculation of trust and reputation scores. Inferences of trust from other data, e.g. the fact that Alice follows Bob or "likes" a post by Bob about movies, will be avoided by this protocol.

The primary rationale for this is that the inferences are quite often simply incorrect. *Just because Alice follows Bob does not necessarily indicate that she trusts him in any way, shape, or form.* Explicit attestations also carry the advantage that their contexts can be made precise; they can be fine tuned to be as generic or as specific as desired. In this way, specific exceptions to more general statements can be made. For example, Alice may express her opinion that Bob has good taste in movies of all categories, with the exception of westerns, in which she believes he has bad taste.

This TIP does not mean that scraped data cannot be utilized by the tapestry protocol. An entity, such as a bot or AI, could be made which takes scraped data as input, makes inferences from that data, and expresses those inferences in the form of signed attestations. Users then have the choice whether or not to trust that entity with respect to the inferences in question.
