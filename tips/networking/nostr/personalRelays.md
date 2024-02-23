back to the [main nostr page](https://github.com/wds4/tapestry-protocol/blob/main/tips/networking/nostr/README.md)

### TIP 3.2.0
personal nostr relays
=====

## Discussion

Users will be encouraged, although not required, to specify a single personal relay, which may be termed a *personal tapestry nostr relay*, that is dedicated to this purpose and that stores data relevant to the tapestry protocol, including words that are not intended for publication over the nostr network. This may be particularly useful for words that are undergoing frequent editing or expected to undergo a large number of edits in a short period. This personal relay will perform the function of a local database, but one that is universally accessible.

Encryption of locally stored data may be considered at a future date for increased data security. However, data leaks and loss may be expected to occur during the early build-out phase of the tapestry protocol. Therefore, the storage of sensitive data should be discouraged.

## Write access

Only the owner of the relay will have write access.

## Read access

The owner of the relay will have a control panel with settings to control who has read access. By default, only the relay owner will have read access.

Optional feature: the relay owner will have the ability to keep some aspects of the local database private and other parts publicly available. 

Optional feature: the relay owner will have the ability to make different subsets of the concept graph available to different subscribers.

