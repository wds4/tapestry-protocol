back to the [tapestry theory table of contents](https://github.com/wds4/tapestry-protocol/blob/main/tapestry-theory/toc.md)

The Constraints Hypothesis
=====

Concepts are formatted according to constraint nodes.
-----

<span style="display:inline-block" >
  <img
    align="top"
    width="45%"
    src="../../images/aFormattedConcept.png"
  />
</span>

The purple square is a *constraint node*. It specifies formatting rules that must be follwed by each instance of that concept (red circles). In the figure, each node represents a JSON file. The constraint node specifies that each instance must have two properties, name and breed, the values of which must be strings. The file for Spot follows this format, as expected.

## The concept as a pattern recognizer, and the cortex as a series of filters

"The eye does not see what the brain does not know."
-- Dr Kaminski

It has been suggested (add refs) that one of the principle functions of the cortex is to filter information, each filter being a pattern recognition, and with filters existing in series as well as in parallel.

The addition of the constraint node effectively turns a concept into a tool for the recognition of patterns. Whenever a new piece of informaiton (a node) is obtained and added to the tapestry, the entity can run through the list of know concepts and check whether the node fits the formatting rules of the constraint. In the Pretty Good Apps implementation of the concept graph, each node represents a JSON data file, constraint nodes are JSON Schemas, and the process of checking whether a node follows the format of the JSON Schema is called *validation*.
