back to the [main nostr page](https://github.com/wds4/tapestry-protocol/blob/main/tips/networking/nostr/README.md)

### TIP 3.1.x
publication of a word over nostr
=====

## Synopsis

By definition according to the tapestry protocol, a *word* is json-formatted object which may be designated `oWord`. To publish a word, it will be converted into a string (the `stringify` command in javascript) and inserted into the content field of a nostr event.

`sWord = stringify(oWord)`

The kind will be either 9xyz or 39xyz, depending on whether the events should be `regular` vs `parameterized replaceable`. As of Feb 2024, 9901 and 39901 (901 in place of xyz) have been used with the understanding these kinds are designated as testnets.

```json
{
    "id": "ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9",
    "content": "{ ... }",
    "kind": 9901, // or 39901
    ...other fields
}
```

## Tags

The `tags` field is not required but may be optionally included as per subsequent TIPs.

