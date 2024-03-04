back to the [TIPs main page](..)

Concept Graph: TIPs 1.x
=====

## Concept Graph Basics: TIPs 1.0.x
- [TIP-1.0.1](basics/conceptGraphs.md): concept graphs
- [TIP-1.0.2](basics/words.md): words are in json
- [TIP-1.0.3](basics/declarations.md): declaration of new concepts (new word types)
- [TIP-1.0.3](): constraint nodes
  - [TIP-1.0.3.0](): JSON Schemas
- [TIP-1.0.4](): word identifiers: universally versus locally unique
- [TIP-1.0.5](): naming conventions
- [TIP-1.0.6](basics/principlesOfOrganization.md): principles of organization
  - goal: use principles that maximize integration of the graph
    - vertical integration
    - horizontal integration
- [TIP-1.0.7](): lists
- [TIP-1.0.8](): concepts
- [TIP-1.0.9](): concept graphs

## Principles of Organization: TIPs 1.1.x
- [TIP-1.1.0](principlesOfOrganization/setsOfNodes.md): arranging nodes into groups, sets, collections, lists
- [TIP-1.1.x]() for every set, there is a single control, master, leader node (the list node or the class node)
  - [TIP-1.1.0](principlesOfOrganization/simpleLists.md): simple lists
  - [TIP-1.1.0](principlesOfOrganization/classThreadPrinciple.md): from lists to concepts: the class thread principle
    - [TIP-1.1.x]() rule: every node must be an instance of at least one class thread
- [TIP-1.1.1](principlesOfOrganization/constraints.md): constraints
  - [TIP-1.1.x]() maximize the ability to deconmpose constraints into properties which can be integrated horizontally

## Concept to concept relationships: TIPs 1.2.x
- [TIP-1.2.x]() subset
- [TIP-1.2.x]() specific instance
- [TIP-1.2.x]() enumeration of a property

## user input to the concept graph
- creating / editing a word
- creating / editing a concept
- connecting two concepts
  - subset
  - specific instance
  - input to a property
- importing a word from an external source

## Word Types: TIPs 1.2.x
#### Core Concept Graph word types
- [TIP-1.wordTypes.words](): words
- [TIP-1.wordTypes.wordTypes](): word types
- [TIP-1.wordTypes.relationships](): relationships
- [TIP-1.wordTypes.relationshipTypes](): relationship types
- [TIP-1.wordTypes.lists](): lists
- [TIP-1.wordTypes.jsonSchemas](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/jsonSchema): json schemas
- [TIP-1.wordTypes.sets](https://github.com/wds4/tapestry-protocol/tree/main/wordTypes/set): sets
- [TIP-1.wordTypes.supersets](): supersets
- [TIP-1.wordTypes.constraints](): constraints
- [TIP-1.wordTypes.graphs](): graphs
- [TIP-1.wordTypes.concepts](): concepts
- [TIP-1.wordTypes.concepts](): conceptGraphs
- [TIP-1.wordTypes.dictionaries](): dictionaries
- [TIP-1.wordTypes.schemas](): schemas

## Relationship Types: TIPs 1.3.x
- [TIP-1.relationshipTypes.0](): relationship type naming conventions
- [TIP-1.relationshipTypes.1](): initiation, propagation, termination
- [TIP-1.relationshipTypes.isTheJsonSchemaFor](): isTheJsonSchemaFor
- [TIP-1.relationshipTypes.isASubsetOf](): isASubsetOf
- [TIP-1.relationshipTypes.isASpecificInstanceOf](): isASpecificInstanceOf
  
## Data visualization: TIPs 1.5.x
