Steps in Grapevine Incorporation
=====

## Step 1: Use Proxy Data to calculate a WoT Score

Problem: How do we weed out spam content?

Solution: Use nostr follow lists (+/- mute lists) as raw data to generate a web of trust (WoT) score using your method of choice, similar to what has already been achieved by wikifreedia and some of the nostr clients. 

There is no single best method to calculate the WoT score.

As of the time of this writing, [Coracle](https://coracle.social/), [Wikifreedia](https://wikifreedia.xyz), [nosWoT](https://noswot.org) and probably several other nostr apps already calculate some sort of WoT score.

## Step 2: Introduce Explicit Trust Attestations

Problem: Just because Alice follows Bob doesn't mean she trusts him to curate content.

Solution:
- Introduce explicit trust attestations formatted according to the tapestry protocol, in the format: "Alice endorses Bob as trustworthy to curate nostr feed in all categories." Alternatively, change the context to fit the app in question, e.g.: "Alice endorses Bob to rate products in the zap.store." In step 5 (below), we will allow the option of more contexts, e.g.: "Alice endorses Bob to rate products in the zap.store in the category of electronics."
- Take the follows data and the attestations data and pool them together, meaning that a follow and a trust attestation are interpreted in the same way when calculating the WoT score.
- Eventual plan is to phase out the usage of follow and mute lists gradually as the explicit attestation dataset increases.

## Step 3: Replace WoT Scores with the Grapevine Influence Score

Replace the WoT score from Step 1 with an Influence Score using the same format that Curated Lists already uses.

## Step 4: Phase Out Proxy Data in favor of Explicit Trust Attestations

## Step 5: Introduce developer-managed Categories

Introduce categories that are relevant to the app in question.

## Step 6: Allow Users to Curate Categories






