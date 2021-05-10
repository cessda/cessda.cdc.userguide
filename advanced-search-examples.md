---
title: Advanced search examples
parent: Advanced search
has_children: false
grand_parent: Home
is_hidden: false
nav_order: 045
---

# {{ page.title }}

All examples were run against the production instance of the [CESSDA Data Catalogue](https://datacatalogue.cessda.eu)
at a point in time when total records in English = 20272

## Simple search

[`house`](https://datacatalogue.cessda.eu/?q=house) [1506 results]

[`garden`](https://datacatalogue.cessda.eu/?q=garden) [264 results]

## AND search

[`house + garden`](https://datacatalogue.cessda.eu/?q=house%20%2B%20garden) [1947 results]

which is equivalent to `house garden`, as searching for multiple terms uses AND by default.

## OR search

[`house | garden`](https://datacatalogue.cessda.eu/?q=house%20OR%20garden) [1946 results]

which of course is equivalent to `garden | house`.

## Phrase search

[`"garden house"`](https://datacatalogue.cessda.eu/?q="garden%20house") [0 results]

[`"house garden"`](https://datacatalogue.cessda.eu/?q="house%20garden") [22 results]

## Truncated search

[`ho*`](https://datacatalogue.cessda.eu/?q=ho%2A) [16060 results]

[`hou*`](https://datacatalogue.cessda.eu/?q=hou%2A) [11048 results]

[`hous*`](https://datacatalogue.cessda.eu/?q=hous%2A) [10454 results]

## Parenthesis search

[`(garden room) | (garden house)`](https://datacatalogue.cessda.eu/?q=%28garden%20room%29%20%7C%20%28garden%20house%29)
 [2321 results]

[`((garden room) | (garden house) | house)`](https://datacatalogue.cessda.eu/?q=%28%28garden%20room%29%20%7C%20%28garden%20house%29%20%7C%20house%29)
 [2325 results]

[`((garden room) | (garden house) | social)`](<https://datacatalogue.cessda.eu/?q=%28%28garden%20room%29%20OR%20%28garden%20house%29%20OR%20social%29>)
[12757 results]
