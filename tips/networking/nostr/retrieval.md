back to the [main nostr page](https://github.com/wds4/tapestry-protocol/blob/main/tips/networking/nostr/README.md)

### TIP 3.1.1.0
retrieval of a word from nostr
=====

## Synopsis

Words published as per the relevant TIPs using the `createWord` task can be retrieved using a filter similar to the following example, which is taken from the [declation for word (from DCoSL protocol, being deprecated)](https://github.com/wds4/DCoSL/blob/main/dips/conceptGraph/declarations/word.md):

```json
{
  "since": 0,
  "kinds": [9xyz], // or 39xyz
  "authors": ["c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"],
  "#c": ["concept-graph-testnet-902"],
  "#w": ["word"],
}
```

or

```json
{
  "ids": ["4a5517d25ebae34b9794f1b8d4dba0681f7ff7297bacbc29de2c915695c53bfe"],
}
