back to [curation of structured data main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/structuredData/README.md)

DCoSL
=====
Decentralized Curation of Simple Lists
-----

## Synopsis

Start with DCAS, then add a cutoff to determine what makes the list and what doesn't.

## User actions

The user can perform the following actions:
- create a new list
- add an item to any existing list
- endorse or reject any individual item as belonging or not belonging to a particular list
- endorse or reject any individual entity as a curator of this particular list

## relevant word types

## relevant relationship types
- endorsesAsACuratorOfTheList
- endorsesAsAnItemOnTheList
- rejectsAsACuratorOfTheList
- rejectsAsAnItemOnTheList

## attestations

There are two primary types of attestations:
- Alice endorses (or rejects) X as an item on the list Y
- Alice endorses (or rejects) Bob as a curator of the list Y

Secondary attestation types:
- Alice endorses (or rejects) that item A and item B are duplicates and should be merged

## Calculations

Each user will have an influence score in the context of curation of this list.

Each list item will have a score which is used to partition into 3 bins: accepted, rejected, and pending.

## Control Panel

The user will have the ability to control the following:
- default user (curator) scores
- default list item scores
- cutoff scores (used to segregate items into bins)

