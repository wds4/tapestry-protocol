back to the [main nostr page](https://github.com/wds4/tapestry-protocol/blob/main/tips/networking/nostr/README.md)

### TIP 3.2.0
relays
=====

## Synopsis

Relays must support *regular events* and *parameterized replaceable events* to be deemed acceptable.

Users will be encouraged, although not required, to specify a single personal relay that stores personal data, including words that are not intended for publication over the nostr network. This may be particularly useful for words that are undergoing frequent editing or expected to undergo a large number of edits in a short period. This personal relay will perform the function of a local database, but one that is universally accessible.
