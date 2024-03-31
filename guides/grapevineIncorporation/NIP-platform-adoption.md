Incorporation of the proposed Grapevine NIP into a specific platform
=====

In this post we discuss how to harness the [proposed Grapevine NIP](https://github.com/wds4/tapestry-protocol/blob/main/guides/grapevineIncorporation/NIP-proposal.md) to adopt context-specific web of trust into whatever nostr app or platform you are building.

## Preamble: Choose context(s) most relevant to your app

The first step will be to think about the context or contexts that are most relevant for your platform or application. In many cases, this may involve selecting or creating the single *action* that best applies to your app, and probably a large number of *categories* that are relevant to your app. If they already exist, great! If not, you can create them at a site that enables users to explore and manage contexts. (Not yet built, but it needs to be!)

### Pick the most relevant action for your app

The first step will be to choose an action that is relevant for your app or platform. Often, a single action *to curate content on My Awesome Site* will suffice. 

For example: Suppose you are building an e-commerce site called zap.store. The first step will be to create an action, like the following:

`to rate and recommend products on zap.store`

Using this action, Alice can attest that she does or does not endorse Bob _to rate and recommend products on zap.store_.

It may be preferable to make use of an *action* that is not specific to your site. For example, instead of the action above, you may wish to use a more generic action:

`to rate and recommend products`

The advantage of using the more generic action is that trust attestations using this action may already be in existence from competing nostr apps.

Of course, your users will be able to create trust attestations in whatever context they choose, so ultimately they will be the ones who decide which of the above actions they prefer, or whether they wish to create new ones. Your job as developer will merely be to get the ball rolling.

If the action: `to rate and recommend products` already exists, but you decide to create and utilize `to rate and recommend products on zap.store` on your site, you will probably want to indicate that `to rate and recommend products on zap.store` is a child of `to rate and recommend products`. 

Of note: there may be additional actions that you wish to add on down the road. For example, consider the action:

`to sell products`

This would be a way to rate the vendors themselves, as opposed to the customers. To keep things simple, you might want to stick with just one action, at least at first.

### Pick one or more categories relevant to your app

Let's stick with our example, the e-commerce site: zap.store. Categories might include: electronics, books, clothes, shirts, pants, etc. You may find that these categories have already been created, but if not, you can create them. As was the case with actions, you will also want to establish relationships, e.g. that *shirts* is a child category of *clothes*.

## Step 1

It may be that you have already created a WoT score for your site using follows. If so, great! Many nostr sites have already done this, including [Coracle](https://coracle.social/), [Wikifreedia](https://wikifreedia.xyz), and others. If you haven't, you don't necessarily have to do this step, but I'm going to include it in this roadmap because it may be a useful "baby step" to get us where we want to be.

## Step 2: Introduce Explicit Trust Attestations

Using the context(s) you selected in the Preamble section, present your users with the ability to create Trust Attestations using those contexts. Using our example of the nostr e-commerce site, you may want to keep things simple and give your users just one option: the ability to indicate that the DO or DO NOT trust another user `to rate and recommend products`. And to keep things simple, you may want to keep the catagory field empty at first, which by default is interpreted as "the set of all categories." In the future, you will probably want to expand attestation options by allowing them to select specific categories, but you may want to save that until later.

## Step 3: Phase Out Follows Data in favor of explicit Trust Attestations from Step 2

The WoT scores from Step 2 are probably calculated using follows data. In this step, you combine follows data with Trust Attestations from Step 2. The plan will be to phase out using follows data, but follows data is plentiful and you'll want to keep using that until users have become accustomed to issuing the relevant Trust Attestations for your app.

## Step 4: Replace WoT Scores with the Grapevine Influence Score

Change the method of calculating WoT scores. 

*work in progress*



