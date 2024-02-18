Declaration of `word type`
=====

## Declaration

New word types are declared as outlined in [DIP-102](../102.md).

```json
{
  "wordData": {
    "slug": "wordType",
    "version": "standard",
    "wordTypes": ["wordType"]
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "wordType",
      "plural": "wordTypes"
    },
    "oName": {
      "singular": "word type",
      "plural": "word types"
    },
    "oTitle": {
      "singular": "Word Type",
      "plural": "Word Types"
    },
    "propertyPath": "wordTypeData",
    "description": "A category of word, as specified by the tapestry protocol. The creation of a word of type: wordType is the primary method for declaration of a new list or concept."
  }
}
```
