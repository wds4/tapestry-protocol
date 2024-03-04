back to [TIPs for the Grapevine main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/grapevine/README.md)

### TIP-2.1.1
context of an attestation
=====

`draft` `author:wds4`

## Synopsis

Influence scores will be a function of *context*, will be specified using two dimensions: an *action* dimension and a *category* dimension. Questions and content that are curated by the Grapevine will be tagged with a category, so that the relevant influence score can be applied in an appropriate manner.

## Example

Alice attests that she recommends Bob to *curate her nostr feed* (action) in the category of *sports-related nostr posts* (category).

## Discussion

### Dimensions

The action and the category dimensions will each be represented as a graph, which will be curated by the Grapevine using TIPs to follow. Prior to that point, "starter" graphs for actions and categories will be specified in this protocol.
