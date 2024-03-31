Incorporation of the proposed Grapevine NIP into a specific platform
=====

In this post we discuss how to harness the [proposed Grapevine NIP](https://github.com/wds4/tapestry-protocol/blob/main/guides/grapevineIncorporation/NIP-proposal.md) to adopt context-specific web of trust into whatever nostr app or platform you are building.

## Preamble: Choose context(s) most relevant to your app

The first step will be to think about the context or contexts that are most relevant for your platform or application. In many cases, this may involve selecting or creating the single *action* that best applies to your app, and probably a large number of *categories* that are relevant to your app. If they already exist, great! If not, you can create them at a site that enables users to explore and manage contexts. (Not yet built, but it needs to be!)

### Pick an action

The first step will be to choose an action that is relevant for your app or platform. Often, a single action *to curate content on My Awesome Site* will suffice. 

For example: Suppose you are building an e-commerce site called zap.store. The first step will be to create an action, like the following:

`to rate and recommend products on zap.store`

Using this action, Alice can attest that she does or does not endorse Bob _to rate and recommend products on zap.store_.

It may be preferable to make use of an *action* that is not specific to your site. For example, instead of the action above, you may wish to use a more generic action:

`to rate and recommend products`

The advantage of using the more generic action is that trust attestations using this action may already be in existence from competing nostr apps.

A third option would be to give your users the option to use either of the above actions in their attestations.

If the action: `to rate and recommend products` already exists, but you decide to create and utilize `to rate and recommend products on zap.store` on your site, you will probably want to indicate that `to rate and recommend products on zap.store` is a child of `to rate and recommend products`. 

### Pick one or more categories

Your us

## Step 1: Use Proxy Data to calculate a WoT Score

Problem: How do we weed out spam content?

Solution: Use nostr follow lists (+/- mute lists) as raw data to generate a web of trust (WoT) score using your method of choice, similar to what has already been achieved by wikifreedia and some of the nostr clients. 

There is no single best method to calculate the WoT score.

As of the time of this writing, [Coracle](https://coracle.social/), [Wikifreedia](https://wikifreedia.xyz), [nosWoT](https://noswot.org) and probably several other nostr apps already calculate some sort of WoT score.

## Step 2: Introduce Explicit Trust Attestations

