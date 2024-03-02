```json
{
    "wordData": {
        "slug": "JSONSchemaFor_relationshipType",
        "title": "JSON Schema for: relationshipType",
        "name": "JSON Schema for: relationshipType",
        "description": "",
        "wordType": "JSONSchema",
        "wordTypes": [
            "word",
            "jsonSchema"
        ]
    },
    "jsonSchemaData": {
        "name": "relationshipType",
        "title": "Relationship Type",
        "slug": "relationshipType",
        "$id": "http://ipfs.ontheblockchain.com/ipns/tobedetermined",
        "$schema": "http://json-schema.org/draft-07/schema",
        "definitions": {},
        "type": "object",
        "required": [
            "relationshipTypeData"
        ],
        "properties": {
            "relationshipTypeData": {
                "type": "object",
                "name": "relationshipType data",
                "title": "relationshipType Data",
                "description": "data about this relationshipType",
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
                        "description": "the name of this relationshipType",
                        "slug": "name"
                    },
                    "title": {
                        "type": "string",
                        "name": "title",
                        "title": "Title",
                        "description": "What is the title of this relationshipType?",
                        "slug": "title"
                    },
                    "description": {
                        "type": "string",
                        "name": "description",
                        "title": "Description",
                        "description": "Provide a description for this relationshipType.",
                        "slug": "description"
                    },
                    "slug": {
                        "type": "string",
                        "name": "slug",
                        "title": "Slug",
                        "description": "The slug for this relationshipType",
                        "slug": "slug"
                    },
                    "relationshipTypeUIData": {
                        "type": "object",
                        "name": "relationshipType UI data",
                        "title": "relationshipType UI Data",
                        "description": "data regarding the appearance of this relationshipType when displayed graphically using vis.js",
                        "required": [],
                        "properties": {
                            "color": {
                                "type": "string",
                                "name": "color",
                                "title": "Color",
                                "description": "What is the color of this relationshipType?",
                                "slug": "color"
                            },
                            "polarity": {
                                "type": "string",
                                "name": "polarity",
                                "title": "Polarity",
                                "description": "what is the polarity of this relationshipType when depicted graphicall: forward or reverse?",
                                "slug": "polarity"
                            }
                        },
                        "unique": [],
                        "slug": "relationshipTypeUIData"
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
                                "name": "governingConcept",
                                "title": "GoverningConcept",
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
                                        "enum": [
                                            "relationshipType",
                                            "animal",
                                            "wordType",
                                            "dog",
                                            "superset",
                                            "cat",
                                            "JSONSchema",
                                            "animalType",
                                            "schema",
                                            "cow",
                                            "property",
                                            "pig",
                                            "concept",
                                            "bird",
                                            "word",
                                            "pattern",
                                            "action",
                                            "propertyType",
                                            "patternInputField",
                                            "singleNodeFieldset",
                                            "singleRelationshipFieldset",
                                            "doubleRelationshipFieldset",
                                            "neuroCoreActionPurposeClassification",
                                            "set",
                                            "enumeration",
                                            "nodeShape",
                                            "kingdom",
                                            "plant",
                                            "fungus",
                                            "organism",
                                            "entityType",
                                            "entity",
                                            "user",
                                            "listing",
                                            "post",
                                            "selfDrivingCar",
                                            "rating",
                                            "ratingTemplate",
                                            "dogBreed",
                                            "irishSetter",
                                            "goldenRetriever",
                                            "sheepDog",
                                            "germanShepherd",
                                            "conceptGraph"
                                        ],
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
                "slug": "relationshipTypeData"
            }
        },
    },
}
```
