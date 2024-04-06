Representation of a thing
=====

This NIP introduces a simple and highly flexible method to represent almost any piece of data -- any _THING_ -- as JSON and store it in nostr in a way that facilitates category-based search. The only requirement is that the _THING_ in question must be assigned to a _category_ (a.k.a. a _class_, a _list_, a _set_, a _group_, a _type_ -- doesn't matter what you call it!).

## Format

Any piece of JSON that follows the format of this NIP will be called a _word_. Every word will belong to one or more _word types_.

There is only one requirement for a JSON to be a _word_: There must be a top-level property which is of type: object, called *thing*Data, where *thing* is a string to represent the _classification_ of the thing.

```json
{
  "thingData": {
    //
  }
}
```

The structure of the data inside *thing*Data will depend upon the classification being used and will be established by convention, with the assistance of web of trust.

The word will be packaged into an event using kind 9902 or 39902 as follows:

```json
{
  "kind": 9902 // or 39902
  "word": "{ 'thingData': { ... }}" // serialized version of the word
  "tags": [
    ["w", "thing"]
  ],
}
```

The w-tag is used to facilitate search based on class. Any given word may belong to multiple classes; therefore, multiple w-tags are allowed.

## Examples

### Example 1: Spot, who is a *dog*

The _word_:

```json
{
  "dogData": {
    "name": "Spot",
    "owner": "Alice",
    "breed": "mutt"
  }
}
```

The above _word_, packaged into a note:

```json
{
  "kind": 9902 
  "word": "{ 'dogData': { 'name': 'Spot', 'owner': 'Alice', 'breed': 'mutt' }}"
  "tags": [
    ["w", "dog"]
  ],
}
```

### Example 2: Alice, who is a *nostrDeveloper*

The _word_:

```json
{
  "nostrDeveloperData": {
    "pubkey": "abc123",
    "name": "Alice",
  }
}
```

The above _word_, packaged into a note:

```json
{
  "kind": 9902 
  "word": "{ 'nostrDeveloperData': { 'pubkey': 'abc123' }}"
  "tags": [
    ["w", "nostrDeveloper"]
  ],
}
```

## Universally unique identifiers

Option: use an event ID or naddr to refer to the class, e.g. `abcd12345Data` in place of `nostrDeveloperData`

### Step 1: define the class

```json
{
  "wordTypeData": {
    "slug": "nostrDeveloper",
    "description": "lorem ipsum"
  }
}
```

Publish over nostr: 

```json
{
  "kind": 9902 
  "word": "{ 'wordTypeData': { 'slug': 'nostrDeveloper', 'description': 'lorem ipsum' }}"
  "tags": [
    ["w", "wordType"]
  ],
}
```

If the event ID of the above note is _abcde12345_, use it as follows:

```json
{
  "abcde12345Data": {
    "pubkey": "abc123",
  }
}
```

## Applications

### List

The example above shows how to manage a list of nostr developers.

### Attestations

We invent the notion of the `trustAttestation` by defining it as a word type:

```json
{
  "wordTypeData": {
    "slug": "trustAttestation",
    "description": "lorem ipsum"
  }
}
```

Example of its usage:

```json
{
  "trustAttestationData": {
    "ratee": "abc123",
    "score": 100,
    "confidence": 80,
    "transitivity": true,
    "comments": "lorem ipsum",
  }
}
```

## Multiple word types

Words can belong to multiple word types, as in the example below:

```json
{
  "animalData": {
    "species": "dog",
  },
  "dogData": {
    "name": "Spot",
  }
}
```

An additional top-level property, `wordData`, may optionally be included with metadata like `wordTypes` to assist in automated processing of the file:

```json
{
  "wordData": {
    "wordTypes": ["animal","dog"],
  },
  "animalData": {
    "species": "dog",
  },
  "dogData": {
    "name": "Spot",
  }
}
```

The note for a word that belongs to multiple word types can have multiple w-tags:

```json
{
  "kind": 9902 // or 39902
  "word": "{ ... }" // serialized version of the word
  "tags": [
    ["w", "animal"],
    ["w", "dog"],
  ],
}
