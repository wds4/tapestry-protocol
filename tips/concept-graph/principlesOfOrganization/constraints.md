back to [TIPs for the Concept Graph main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/concept-graph/README.md)

TIP 1.1.1
=====

constraints
-----

Concepts are formatted according to constraint nodes.
-----

<span style="display:inline-block" >
  <img
    align="top"
    width="45%"
    src="../../../images/aFormattedConcept.png"
  />
</span>

The purple square is a *constraint node*. It specifies formatting rules that must be follwed by each instance of that concept (red circles). In the figure, each node represents a JSON file. The constraint node specifies that each instance must have two properties, name and breed, the values of which must be strings. The file for Spot follows this format, as expected.
