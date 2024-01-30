---
title: Advanced search
parent: CESSDA Data Catalogue User Guide
has_children: true
is_hidden: false
nav_order: 040
---

# {{ page.title }}

To support more complex searches, the CESSDA Data Catalogue provides an Advanced Search option
that includes a variety of Boolean and other search operators for enhanced searching capabilities.

## AND operation

To perform the AND operation, use  ‘+’ in the search box.
Entering `funding + education` in the search box will give you the same results as searching
`funding education` since the AND operation is the default in the system.

## OR operation

Use ‘|’ in the search box for OR operation.
 If you want to get results where any of the search terms appears, e.g.`sport` or `exercise`,
perform a search using: `sport | exercise`.

## NOT operation

Use both ‘+’ and ‘-’ in the search for the NOT operation.
This enables exclusion of studies containing specific words or phrases.
For example, to find datasets about elections but not presidential elections,
enter  `elections + -presidential`.
Note: it is important to avoid leaving an empty space before the `-` to ensure accurate exclusion of the word after `-`.

## Phrase search

To search for exact phrases, where specific words are in a particular order,
put the phrase in quotation marks. This will give results containing the exact phrase.
For instance: “covid-19” or “Angela Merkel”.

## Truncated search

To search for various endings of a root word, use the "`*`" sign at the point where the spelling of
the word could change. For example, `nurs*` will give you `nurse`, `nurses`, `nursing`, and so.
However, `nurse*` will not give “nursing”.
Note: Elastic search will carry out some stemming in the search automatically.

## Parenthesis search

Parentheses can be used to build a search with a combination of search operators.
They signify precedence, that is, the search within the parentheses is executed first.
This approach is valuable for performing searches where alternate phrasings of the same
topic may be included.

For instance, consider the search:
 `(“health care”) | (“health services”)`,
This will give results that contain either
 `health care` or `health services` as exact phrases.
If you search instead using `(“health care”) + (“health services”)`
(i.e. an AND search instead of an OR search),
you will get results that include both the phrases *health care* and *health services*.

## Examples

See [Advanced Search examples]({% link advanced-search-examples.md %}).
