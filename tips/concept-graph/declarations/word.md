Declaration of `word`
=====

## Declaration

New word types are declared as outlined in [DIP-102](../102.md).

```json
{
  "wordData": {
    "slug": "word",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "word"
        }
      }
    }
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "word",
      "plural": "words"
    },
    "oName": {
      "singular": "word",
      "plural": "words"
    },
    "oTitle": {
      "singular": "Word",
      "plural": "Words"
    },
    "propertyPath": "wordData",
    "description": "A node in a graph, formatted in json, with additional requirements and conventions specified according to the tapestry protocol."
  }
}
```
