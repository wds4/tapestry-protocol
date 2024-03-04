back to the [grapevine main page](https://github.com/wds4/tapestry-protocol/blob/main/tips/grapevine/README.md)

input
=====

## Synopsis

The `input` is the sum of the weights of each of the terms used to calculate an `average score`.

## Discussion

There are several classifications of `input`, depending on whether or not to include the default score term(s) and the inherited term(s), if any exist, and whether to use the adjusted or unadjusted versions of those terms.

- core input: the input of the main terms only
- default input: the unadjusted input of the default score
- inherited score input: the unadjusted inputs of the inherited scores, if any
