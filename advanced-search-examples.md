---
title: Advanced search examples
parent: Advanced search
has_children: false
grand_parent: Home
is_hidden: false
nav_order: 045
---

# {{ page.title }}

All examples were run against the [CESSDA Data Catalogue](https://datacatalogue.cessda.eu)
at a point in time when there were 27,968 English records present in the catalogue.

## Simple search

[`house`](https://datacatalogue.cessda.eu/?q=house) - 9,067 results

[`garden`](https://datacatalogue.cessda.eu/?q=garden) - 322 results

## AND search

[`house + garden`](https://datacatalogue.cessda.eu/?q=house%20%2B%20garden) - 165 results

which is equivalent to `house garden`, as searching for multiple terms uses AND by default.

## OR search

[`house | garden`](https://datacatalogue.cessda.eu/?q=house%20%7C%20garden) - 9105 results

which of course is equivalent to `garden | house`.

## NOT search

[`elections + -presidential`](https://datacatalogue.cessda.eu/?q=elections%20%2B%20-presidential) - 139 results

## Phrase search

[`"garden house"`](https://datacatalogue.cessda.eu/?q="garden%20house") - 3 results

[`"house garden"`](https://datacatalogue.cessda.eu/?q="house%20garden") - 26 results

## Truncated search

[`ho*`](https://datacatalogue.cessda.eu/?q=ho%2A) - 19,547 results

[`hou*`](https://datacatalogue.cessda.eu/?q=hou%2A) - 13,444 results

[`hous*`](https://datacatalogue.cessda.eu/?q=hous%2A) - 12,698 results

## Parenthesis search

[`(garden room) | (garden house)`](https://datacatalogue.cessda.eu/?q=%28garden%20room%29%20%7C%20%28garden%20house%29) - 0 results

[`((garden room) | (garden house) | house)`](https://datacatalogue.cessda.eu/?q=%28%28garden%20room%29%20%7C%20%28garden%20house%29%20%7C%20house%29)
\- 9,068 results

[`((garden room) | (garden house) | social)`](<https://datacatalogue.cessda.eu/?q=%28%28garden%20room%29%20%7C%20%28garden%20house%29%20%7C%20social%29>)
\- 23,166 results
