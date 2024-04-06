Representation of a thing
=====

This NIP introduces a simple and highly flexible method to represent almost any piece of data as JSON and store it in nostr in a way that facilitates category-based search.

## Format

JSON with the top-level property being an object, *thing*Data, where *thing* is a string to represent the _classification_ of the thing.

Any piece of JSON that follows this format will be called a _word_.

```json
{
  "thingData": {
    //
  }
}
```

This will be packaged into an event using kind 9902 or 39902 as follows:

```json
{
  "kind": 9902 // or 39902
  "word": "{ 'thingData': { ... }}" // serialized version of the word
  "tags": [
    ["w", "thing"]
  ],
}
```

The structure of the data inside *thing*Data will depend upon the thing in question and will be established by convention, with the assistance of web of trust.

## Examples

### Example 1: *thing* = `dog`

```json
{
  "dogData": {
    "name": "Spot",
    "owner": "Alice",
    "breed": "mutt"
  }
}
```

```json
{
  "kind": 9902 
  "word": "{ 'dogData': { 'name': 'Spot', 'owner': 'Alice', 'breed': 'mutt' }}"
  "tags": [
    ["w", "dog"]
  ],
}
```

### Example 2: *thing* = *nostrDeveloper*

```json
{
  "nostrDeveloperData": {
    "pubkey": "abc123",
  }
}
```

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

### Step 1: determine the event ID

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

Then use the event ID of the above note 

```json
{
  "abcde12345Data": {
    "pubkey": "abc123",
  }
}
```
