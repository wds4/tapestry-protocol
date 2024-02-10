Refactor the Concept Graph app
=====

The Concept Graph has been implemented in as a desktop app called [Plex ](), which stores information in IPFS and was made before nostr was well developed. The purpose of these bounties will be:
- to refactor the Concept Graph using nostr
- in a webapp that integrates with DCoSL web app (in progress, Feb 2024)
- to contribute to open source Concept Graph and Grapevine libraries that can be used by other projects including web apps, desktop apps, etc

# Concept Graph WebApp

Refactor these functions, all of which already work in Plex. 

- Support for JSON Schema
  - validation of JSON

- Support for JSON forms or equivalent library

- Enable users to create and submit a word to nostr using the relevant TIPs
  - create new words as per the relevant TIPs
    - view word in JSON
    - view rendered JSON using
    - upload to nostr per the relevant networking TIP (replaceable or not?)
    - download all words by user

- same as above, but able to select any of the basic word types declared in the Tapestry protocol
  - wordType, relationshipType, schema, concept, etc

- enable users to manage concepts
  - create a new concept
  - view all concepts
  - edit individual concept
  - rearrange set tree
  - edit property tree

- enable users to connect concepts together

- visualization tools
  - individual concepts
  - relationships between concepts

- publishing
  - view which words have been published and which have not
  - publish / delete unpublished words

- NeuroCore library
  - enforce class thread principle
