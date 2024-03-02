```json
{
    "wordData": {
        "slug": "jsonSchemaFor_list",
        "name": "json schema for list",
        "title": "JSON Schema for List",
    },
    "jsonSchemaData": {
        "name": "list",
        "title": "List",
        "$schema": "http://json-schema.org/draft-07/schema",
        "type": "object",
        "required": [
            "listData"
        ],
        "definitions": {},
        "properties": {
            "listData": {
                "type": "object",
                "name": "list data",
                "title": "List Data",
                "description": "data about this list",
                "require": true,
                "required": [
                    "name",
                    "description"
                ],
                "definitions": {},
                "properties": {
                    "name": {
                        "type": "object",
                        "required": [
                            "singular",
                            "plural"
                        ],
                        "properties": {
                            "singular": {
                                "type": "string"
                            },
                            "plural": {
                                "type": "string"
                            }
                        }
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
