<h1>Incorporation of the Grapevine into Your Application or Platform</h1>

This guide is intended for the developer or dev team who wishes to incorporate the Grapevine into a specific application or platform. It is divided into two sections: _Define the Goal_, and _Plan the Roadmap_. For illustration purposes, we will imagine building on a fork of the decentralized wikipedia application called [Wikifreedia](https://wikifreedia.xyz) which we will call Pretty Good Wikipedia, or pgWiki. Although Wikifreedia and pgWiki are built on top of nostr, the Grapevine and this guide can be readily modified to any one of a number of nostr alternatives: IPFS, slashtags/hyperdrive, GUN, etc.

# Define the Goal 

## Step 1: Statement of General Purpose 

The first step is to create a clear statement of the purpose that the Grapevine will serve in the app in question. This could be as short as one sentence and may be of the following format: _My Awesome App uses the Grapevine to enable you and your community to identify who is the most trustworthy, and in what context, so they can help you curate the content, facts, and information relevant to My Awesome App._

For example: _The Pretty Good Wiki uses the Grapevine to enable you and your community to manage the organization of the encyclopedia's entries into categories and to identify the most trustworthy curators for each category._

## Step 2: Define User Actions

Define all of the relevant actions that a user can take in your app. This can be divided into content-specific and attestation-specific actions. Note that these will likely not all be rolled out at once, and the list of planned available actions may be updated as user feedback is obtained.

Using Pretty Good Wiki as an example:

### content
- users can submit and edit individual wiki entries (already available on Wikifreedia)
- users can fork and edit an existing wiki entry that was started by someone else (already available on Wikifreedia)
- users can submit individual categories (e.g. technology, history, entertainment, movies, sci-fi, etc) (not yet available on Wikifreedia)

### attestations
- Alice can endorse (or block) Bob as a curator for the wiki, either in general or in a category-specific fashion, e.g.: Alice endorses Bob to curate content for the Pretty Good Wiki (optional: in the category of technology)
- Alice can endorse (or veto) Entry A as a valid entry for Category X, e.g: Bob's article on Satoshi is a valid entry in the category of Bitcoin History. If Alice leaves the category blank, she is effectively endorsing the article to exist within the Pretty Good Wiki, regardless of category.
- Alice can endorse that some given category is (or is not) a valid category, e.g.: Alice endorses that entertainment is a valid category
- Alice can endorse that category A is (or is not) a subcategory of category B, e.g.: Alice endorses movies as a subcategory of entertainment
- (optional) Alice can endorse that category A and category B are (or are not) duplicates that should be merged, e.g.: Alice endorses that Satoshi and Satoshi Nakamoto articles are duplicates

## Step 3: Define the Data Model

Define how the above content and attestations will be stored and represented. This should be done to maximize interoperability with external applications and platforms that also use the Grapevine. In particular, trust attestations and context should be defined in a manner that maximizes overlap with other apps and platforms, preexisting and anticipated.

The recommended data model for context is to use the method outlined in this article (provide link). Context is defined using two dimensions: the action dimension and the category dimension. For each dimension, the list of nodes and its organization into hierarchies is managed by your Grapevine. Example: Alice trusts Bob to be a critic of (vs: to 

Using Pretty Good Wiki as an example:

### content
- wiki entries and wiki category entries are each stored in nostr as kind 3xxxx (parameterized replaceable) events and can referenced either by the nostr event id (universally unique) or by the entry name (which is not necessarily unique) + author
- each category entry comes with a name and a description. (It is an element of the relevant concept: contextCategories and formatted according to the Concept Graph, as per example.)
 
### attestations


## Step 4: Pick Methods to calculate Influence

The central function of Alice's Grapevine is to calculate a context-dependent influence score for each user. For example, Alice's Grapevine may tell her that Bob merits a high influence score in the context of reviewing sci-fi movies, and an even higher influence score in the context of writing the screenplay for movies in the genre of romantic comedies. Each context has two dimensions: an action (reviewing, writing the screenplay, editing, etc) and a category (entertainment, movies, sci fi, etc). Each of these dimensions is represented as a hierarchical graph which is curated by your Grapevine, in the app (if necessary) or outside of the app (preferred) if suitable graphs already exist in the ecosystem.

There are two categories of how to perform these calculations: the starter method and the Grapevine method. Started methods are useful and relatively easy to implement from the perspective of the developer but carry drawbacks. Those drawbacks may not be evident until the app attracts a wide userbase, which in turn attracts scammers and other bad actors. The Grapevine is a generic method designed to address those drawbacks but is much more challenging for the designer and developer.

# Plan the Roadmap

In this step, we decide what features will be rolled out and in what order. For pgWiki, the roadmap could be the following:

## Phase 1

Problem: How do we weed out spam articles and edits?

Solution: Use nostr follow lists and mute lists as raw data for a rudimentary web of trust.
- Users are in one of three categories: whitelisted, blacklisted, or uncategorized
- If Alice follows (mutes) Bob, then Bob is on Alice's whitelist (blacklist)
- For any given user Bob, if N whitelisted users follow Bob and M whitelisted users mute Bob, then if N - M > 2, then Bob becomes whitelisted; or if M > N > 2, then Bob becomes blacklisted

As of the time of this writing, Pablo's [Wikifreedia](https://wikifreedia.xyz) already does this.

## Phase 2

Problem: Just because Alice follows Bob doesn't mean she trusts him to curate wikis.

Solution: Introduce explicit attestations (as above). Use explicit attestation data in addition to follow and mute list data. Gradually phase out the usage of follow and mute lists as the explicit attestation dataset increases.

## Phase 3

Replace the simple Grapevine algorithm with the more sophisticated algorithm that is used in Curated Lists app of Pretty Good Apps.

## Phase 4

Introduce wikipedia categories.

