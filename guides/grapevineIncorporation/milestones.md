Milestones
=====

## Phase 1

Problem: How do we weed out spam content?

Solution: Use nostr follow lists (+/- mute lists) as raw data to generate a web of trust (WoT) score using your method of choice, similar to what has already been achieved by wikifreedia and some of the nostr clients. 

There is no single best method to calculate the WoT score.

As of the time of this writing, [Coracle](https://coracle.social/), [Wikifreedia](https://wikifreedia.xyz), [nosWoT](https://noswot.org) and probably several other nostr apps already calculate some sort of WoT score.

## Phase 2

Problem: Just because Alice follows Bob doesn't mean she trusts him to curate content.

Solution:
- Introduce explicit trust attestations using the same format that Curated Lists already uses.
- Take the follows data and the attestations data and pool them together, meaning that a follow and a trust attestation are interpreted in the same way when calculating the WoT score.
- Eventual plan is to phase out the usage of follow and mute lists gradually as the explicit attestation dataset increases.

## Phase 3

Replace the WoT score from Milestone 1 with an Influence Score using the same format that Curated Lists already uses.

## Phase 4

Introduce wikipedia categories.






