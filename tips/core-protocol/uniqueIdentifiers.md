back to [TIPs: Core Protocol main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/core-protocol/README.md)

### TIP-0.0.7
unique identifiers
=====

`draft` `author:wds4`

## Synopsis

In the global environment, cryptographic identifiers will be relied upon as *universally unique identifiers*. However, locally unique identifiers may be found in some instances to improve communication between entities, with ambiguity of meaning as a potential tradeoff.

## Discussion

*Unique identifiers* will be used to refer to individual nodes, to facilitate communication between entities. The question will arise: unique to what environment? A variety of environments will be utilized, including *universally unique identifiers* (such as cryptographic hashes) and *locally unique identifiers*, such as the username used for an entity under the assumption that no other entity in some specified local community uses the same username, with no guarantee that the same username might not be used in some alternate community.

Thus, care will be taken to keep careful track of the environment in which data identifiers (identifiers of nodes) will be presumed to be unique. Examples of environments (that will be fleshed out in subsequent TIPs) include:
- the global domain
- an individual concept graph
- an individual concept

In communications between entities, universally unique identifiers will have the advantage of eliminating ambiguity. For example, the word *troll* might be interpreted differently by different users, and this ambiguity can be resolved with the use of a cryptographic identifier which points to a file with one specific definition. 

However, there may be instances where ambiguity is unavoidable, or perhaps even desirable. Consider that the definitions of words like *troll* will need to be updated from time to time. If Alice creates an attestation that Bob is a troll, she may want the attestation to point to one particular unchanging definition. However, she recognizes that the definitions of words change over time. What if the file with the definition is lost and cannot be found? This would render her attestation uninterpretable. Therefore, she may find it more useful to use the word troll with the understanding that the reader's interpretation of the attestation must depend upon whatever definition of troll is preferred by the reader. Alternatively, a composite approach can be taken: she can use the word troll and also provide a universally unique identifier to point to her preferred definition of the word, with the understanding that the reader will default to his local definition if her preferred definition cannot be found or if it cannot be interpreted.

## Notes

May replace the word *environment* with *domain*.
