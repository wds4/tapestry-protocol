Context
=====

Example:

```json
{
  "contextData": {
    "name": "to curate Wikifreedia content in the category of economics",
    "description": "lorem ipsum",
    "action": {
      "name": "to curate Wikifreedia content",
      "nodeId": "abc123",
      "naddr": "abc123",
    },
    "category": {
      "name": "economics",
      "nodeId": "abc123",
      "naddr": "abc123",
    },
    "transitive": true, 
  }
}
```

This will be encoded into a note as per the following example:

```json
{
  "content": "to curate Wikifreedia content in the category of economics",
  "kind": 9902,
  "tags": [
    ["P","tapestry],
    ["w", "context"],
    ["wordtype", "context"],
    ["action", "abc123"],
    ["category", "abc123"],
  ]
}
```

Context can be referenced in an event tag by name, by note id, or by naddr.

Example:

`["c","to curate Wikifreedia content in the category of economics"]`
