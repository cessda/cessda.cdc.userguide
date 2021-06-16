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
at a point in time when total records in English = 30627.

## Simple search

[`house`](https://datacatalogue.cessda.eu/?q=house) [8311 results]

[`garden`](https://datacatalogue.cessda.eu/?q=garden) [327 results]

## AND search

[`house + garden`](https://datacatalogue.cessda.eu/?q=house%20%2B%20garden) [296 results]

which is equivalent to `house garden`, as searching for multiple terms uses AND by default.

## OR search

[`house | garden`](https://datacatalogue.cessda.eu/?q=house%20%7C%20garden) [8342 results]

which of course is equivalent to `garden | house`.

## NOT search

[`elections + -presidential`](https://datacatalogue.cessda.eu/?q=elections%20%2B%20-presidential) [2811 results]

## Phrase search

[`"garden house"`](https://datacatalogue.cessda.eu/?q="garden%20house") [3 results]

[`"house garden"`](https://datacatalogue.cessda.eu/?q="house%20garden") [26 results]

## Truncated search

[`ho*`](https://datacatalogue.cessda.eu/?q=ho%2A) [17484 results]

[`hou*`](https://datacatalogue.cessda.eu/?q=hou%2A) [12064 results]

[`hous*`](https://datacatalogue.cessda.eu/?q=hous%2A) [11411 results]

## Parenthesis search

[`(garden room) | (garden house)`](https://datacatalogue.cessda.eu/?q=%28garden%20room%29%20%7C%20%28garden%20house%29)
 [297 results]

[`((garden room) | (garden house) | house)`](https://datacatalogue.cessda.eu/?q=%28%28garden%20room%29%20%7C%20%28garden%20house%29%20%7C%20house%29)
 [8312 results]

[`((garden room) | (garden house) | social)`](<https://datacatalogue.cessda.eu/?q=%28%28garden%20room%29%20%7C%20%28garden%20house%29%20%7C%20social%29>)
[18626 results]
