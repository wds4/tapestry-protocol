DCoG-categories
=====

## Synopsis

DCoG-categories is a special type of graph that is used to organize them items on a list (or the instances of a concept) into 

## Discussion

Same rules as DCoG, but with added restrictions:
- Only two node types are allowed:
  - a category-type node
  - an item-type node
- Oonly two types of relationships are allowed:
  - category B is a subset of category A
  - item A is a specific instance of category B
- There must be one node that is the superset of all categories
- There is an option of requiring that the resulting graph must be a DAG: directed acyclic graph
