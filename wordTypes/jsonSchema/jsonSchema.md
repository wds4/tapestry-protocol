```json
{
    "wordData": {
        "slug": "jsonSchemaFor_jsonSchema",
        "title": "JSON Schema for JSON Schema",
        "name": "json schema for json schema",
        "wordTypes": [
            "word",
            "jsonSchema"
        ],
    },
    "jsonSchemaData": {
        "name": "json schema",
        "title": "JSON Schema",
        "slug": "jsonSchema",
        "$schema": "http://json-schema.org/draft-07/schema",
        "definitions": {},
        "type": "object",
        "required": [
            "jsonSchemaData"
        ],
        "properties": {
            "jsonSchemaData": {
                "type": "object",
                "name": "json schema data",
                "title": "JSON Schema Data",
                "description": "data about this json schema",
                "required": [
                    "name",
                    "title",
                    "slug",
                    "metaData"
                ],
                "unique": [
                    "name",
                    "title",
                    "slug"
                ],
                "properties": {
                    "name": {
                        "type": "string",
                        "name": "name",
                        "title": "Name",
                        "description": "The name for this json schema",
                        "slug": "name"
                    },
                    "title": {
                        "type": "string",
                        "name": "title",
                        "title": "Title",
                        "description": "The title for this json schema",
                        "slug": "title"
                    },
                    "slug": {
                        "type": "string",
                        "name": "slug",
                        "title": "Slug",
                        "description": "The slug for this json schema",
                        "slug": "slug"
                    },
                    "description": {
                        "type": "string",
                        "name": "description",
                        "title": "Description",
                        "description": "The description for this json schema",
                        "slug": "description"
                    },
                    "metaData": {
                        "type": "object",
                        "name": "metaData",
                        "title": "MetaData",
                        "description": "",
                        "required": [
                            "governingConcept"
                        ],
                        "unique": [],
                        "properties": {
                            "governingConcept": {
                                "type": "object",
                                "name": "governing concept",
                                "title": "Governing Concept",
                                "description": "",
                                "required": [
                                    "slug"
                                ],
                                "unique": [],
                                "properties": {
                                    "slug": {
                                        "type": "string",
                                        "name": "slug",
                                        "title": "Slug",
                                        "description": "",
                                        "slug": "slug"
                                    }
                                },
                                "slug": "governingConcept"
                            }
                        },
                        "slug": "metaData"
                    }
                },
                "types": [
                    "primaryProperty"
                ],
                "slug": "jsonSchemaData"
            }
        },
    },
}
```
