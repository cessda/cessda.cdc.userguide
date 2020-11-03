---
title: Advanced Search
layout: page
nav_order: 004
---

# Advanced Search

To support more complex searches, the CDC provides an Advanced Search option.
A number of Boolean and other search operators are enabled.

- `+` signifies **AND** operation
- `|` signifies **OR** operation
- `-` **negates** a single token
- `"` wraps a number of tokens to signify a **phrase** for searching
- `*` at the end of a term signifies a **prefix** query
- `(` and `)` signify **precedence**
- `~N` after a word signifies edit **distance** (fuzziness)
- `~N` after a phrase signifies **slop** amount

## Example

The example below searches for ``CONCEPTUAL + METHODOL* + -Sleep + -psycho*``
and includes all hits for Conceptual, any word starting with methodol,
but excludes records containing Sleep or anything starting with psycho.

![Advanced search](images/advanced-search.png "Advanced search")
