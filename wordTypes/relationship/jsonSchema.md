```json
{
  "wordData": {
    "slug": "relationship",
    "version": "hybridSandbox",
    "wordTypes": ["jsonSchema"],
  },
  "jsonSchemaData": {
    "name": "relationship",
    "title": "Relationship",
    "$schema": "http://json-schema.org/draft-07/schema",
    "type": "object",
    "required": [
      "relationshipData"
    ],
    "definitions": {
      "word": {
        // need external reference
      },
      "relationshipType": {
        // need external reference
    },
    "properties": {
      "relationshipData": {
        "type": "object",
        "name": "relationship data",
        "title": "Nostr Curated List Data",
        "description": "data about this nostrCuratedList",
        "required": [
          "nodeFrom",
          "relationshipType",
          "nodeTo"
        ],
        "definitions": {},
        "properties": {
          "nodeFrom": {
            "$ref": "#/definitions/word"
          },
          "relationshipType": {
            "$ref": "#/definitions/relationshipType"
          },
          "nodeTo": {
            "$ref": "#/definitions/word"
          }
        }
      }
    }
  }
}
```
