```json
{
    "wordData": {
        "slug": "jsonSchemaFor_set",
        "title": "JSON Schema for set",
        "name": "json schema for set",
        "wordTypes": [
            "word",
            "jsonSchema"
        ],
    },
    "jsonSchemaData": {
        "name": "set",
        "title": "Set",
        "slug": "set",
        "$id": "http://ipfs.ontheblockchain.com/ipns/tobedetermined",
        "$schema": "http://json-schema.org/draft-07/schema",
        "definitions": {},
        "type": "object",
        "required": [
            "setData"
        ],
        "properties": {
            "setData": {
                "type": "object",
                "name": "set data",
                "title": "set Data",
                "description": "data about this set",
                "types": [
                    "primaryProperty"
                ],
                "require": true,
                "required": [],
                "unique": [],
                "properties": {
                    "slug": {
                        "type": "string",
                        "name": "slug",
                        "title": "Slug",
                        "description": "The top-level slug for this set",
                        "slug": "slug"
                    },
                    "name": {
                        "type": "string",
                        "name": "name",
                        "title": "Name",
                        "description": "The top-level name for this set",
                        "slug": "name"
                    },
                    "title": {
                        "type": "string",
                        "name": "title",
                        "title": "Title",
                        "description": "The top-level title for this set",
                        "slug": "title"
                    },
                    "description": {
                        "type": "string",
                        "name": "description",
                        "title": "Description",
                        "description": "The top-level description for this set",
                        "slug": "description"
                    }
                },
                "slug": "setData"
            }
        },
    },
}
```
