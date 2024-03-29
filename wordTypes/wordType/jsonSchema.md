
```json
{
    "wordData": {
        "slug": "jsonSchemaFor_wordType",
        "name": "json schema for word type",
        "title": "JSON Schema for Word Type",
    },
    "jsonSchemaData": {
        "name": "word type",
        "title": "Word Type",
        "$schema": "http://json-schema.org/draft-07/schema",
        "type": "object",
        "required": [
            "wordTypeData"
        ],
        "definitions": {
            "unitData": {
                "type": "object",
                "required": ["singular", "plural"],
                "properties": {
                    "singular": {
                        "type": "string"
                    },
                    "plural": {
                        "type": "string"
                    }
                }
            }
        },
        "properties": {
            "wordTypeData": {
                "type": "object",
                "name": "word type data",
                "title": "Word Type Data",
                "description": "data about this word type",
                "require": true,
                "required": [
                    "oSlug",
                    "oName",
                    "oTitle",
                    "propertyPath",
                    "description"
                ],
                "definitions": {},
                "properties": {
                    "oSlug": {
                       "$ref": "#/definitions/unitData"
                    },
                    "oName": {
                       "$ref": "#/definitions/unitData"
                    },
                    "oTitle": {
                        "$ref": "#/definitions/unitData"
                    },
                    "propertyPath": {
                        "type": "string"
                    },
                    "description": {
                        "type": "string"
                    }
                }
            }
        }
    }
}
```

