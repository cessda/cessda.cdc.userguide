---
title: Advanced search
parent: Home
has_children: true
is_hidden: false
nav_order: 040
---

# {{ page.title }}

To support more complex searches, the CDC provides an Advanced Search option.
A number of Boolean and other search operators are enabled.

## AND operation

If you enter `funding + education`,
you get the same results as with the search `funding education` since AND operation is the default in the system.
 Use ‘+’ in the search box for AND operation.

## OR operation

If you are happy to get results with any of the terms entered, e.g.`sport` or `exercise`,
search with: `sport | exercise`.
Use ‘|’ in the search box for OR operation.

## NOT operation

Allows you to exclude studies where a word or a phrase appears.
For instance, for elections other than presidential elections, enter in the search box `elections + -presidential`.
Or if you want to exclude a publisher, for instance, use `elections + -GESIS`.
Use both ‘+’ and ‘-’ in the search for the NOT operation.
Note, no empty space before the ‘-’ for the word not to be included.

## Phrase search

To search for exact phrases (where exact words are in a particular order),
put the phrase in quotation marks.
Only documents with this exact phrase come up. E.g.: `covid-19` or `Angela Merkel`.

## Truncated search

To search any ending of a root word, use the "`*`" sign at the point where the spelling of the word could change.
For example, `nurs*` will give you `nurse`, `nurses`, `nursing` etc whereas `nurse*` will not give `nursing`.
Note: Elasticsearch will carry out some stemming in the search automatically.

## Parenthesis search

Parenthesis can be used to build a search with a combination of search operators.
Parenthesis signify precedence, that is, the search inside the parentheses is done first.
This is a good way to make a search where alternate phrasings of the same issue may have been used.

For instance, if you enter the search: `(“health care”) | (“health services”)`,
you will get only those documents that have either `health care` or `health services` as exact phrases.
If you search instead using `(“health care”) + (“health services”)` (i.e. an AND search instead of OR search),
you would get only the documents with both *health care* and *health services*.

## Examples

See [Advanced Search examples]({% link advanced-search-examples.md %}).
