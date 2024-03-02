```json
{
    "wordData": {
        "slug": "JSONSchemaFor_concept",
        "title": "JSONSchema for concept",
        "name": "JSONSchema for concept",
        "description": "",
        "wordType": "JSONSchema",
        "wordTypes": [
            "word",
            "JSONSchema"
        ],
    },
    "JSONSchemaData": {
        "name": "concept",
        "title": "Concept",
        "$schema": "http://json-schema.org/draft-07/schema",
        "definitions": {},
        "type": "object",
        "required": [
            "conceptData"
        ],
        "properties": {
            "conceptData": {
                "type": "object",
                "name": "concept data",
                "title": "concept Data",
                "description": "data about this concept",
                "types": [
                    "primaryProperty"
                ],
                "require": true,
                "required": [
                    "name",
                    "title",
                    "slug"
                ],
                "unique": [
                    "name",
                    "title",
                    "slug"
                ],
                "properties": {
                    "slug": {
                        "type": "string",
                        "name": "slug",
                        "title": "Slug",
                        "description": "The top-level slug for this concept",
                        "slug": "slug"
                    },
                    "name": {
                        "type": "object",
                        "name": "name",
                        "title": "Name",
                        "description": "The top-level name for this concept",
                        "required": [
                            "singular",
                            "plural"
                        ],
                        "unique": [],
                        "properties": {
                            "singular": {
                                "type": "string",
                                "name": "singular",
                                "title": "Singular",
                                "description": "",
                                "slug": "singular"
                            },
                            "plural": {
                                "type": "string",
                                "name": "plural",
                                "title": "Plural",
                                "description": "",
                                "slug": "plural"
                            }
                        },
                        "slug": "name"
                    },
                    "title": {
                        "type": "string",
                        "name": "title",
                        "title": "Title",
                        "description": "The top-level title for this concept",
                        "slug": "title"
                    },
                    "description": {
                        "type": "string",
                        "name": "description",
                        "title": "Description",
                        "description": "The top-level description for this concept",
                        "slug": "description"
                    }
                },
                "slug": "conceptData"
            }
        },
    },
}
```
