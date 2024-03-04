back to [TIPs for the Grapevine main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/grapevine/README.md)

### TIP-2.0.2
context
=====

`draft` `author:wds4`

## Synopsis

Context plays a central role in the Grapevine. Trust ratings are contextual, trust scores are contextual; and content is contextual. 

## Definition

Context will be composed of two dimenstions: an *action* dimension and a *category* dimension. In some cases both dimensions will be required, e.g.: Alice trusts Bob to perform an action in a particular category. In other cases, only the category dimension is required, e.g.: Alice attests that Bob's product belongs to the category of smartphones, or Alice attests that some particular piece of content belongs to the category of NSFW.

## Examples

Trust ratings and trust (influence) scores will require specification of both dimenstions. For example: Alice attests that she recommends Bob to *curate her nostr feed* (action) in the category of *sports-related nostr posts* (category).

Questions and content that are curated by the Grapevine may be tagged with a category, so that the relevant influence score can be applied in an appropriate manner. For example: Charlie's post on the football game may be labelled with the category: *sports-related nostr post*.

### Dimensions and their organization

The action and the category dimensions will each be represented as a graph, which will be curated by the Grapevine using TIPs to follow. Prior to that point, "starter" graphs for actions and categories will be specified in this protocol.
