---
title: Basic search
parent: Home
has_children: false
is_hidden: false
nav_order: 020
---

# {{ page.title }}

Basic keyword search is provided in the search bar in the upper right.

The number of results is presented in the upper left.
Results can be sorted by relevance, title, and date of the data collection.

The search language options are provided next to the search box.
If you want to browse study descriptions in German, for instance, choose German as the language.
Note: some service providers provide study descriptions only in English, regardless of country,
or both in English and in the local language.
It is advised to always do a search in English as well as in the local language.

A simple search ‘*environment*’ returns documents containing that term.
Note that Elasticsearch applies synonyms and stemming in the search.
If you use two search terms, for example, by entering ‘*equality pay*’ into the box,
the default is AND, that is, both “equality” and “pay” should appear in the resulting documents.

![Basic search](images/basic-search.png "Basic search")

The “Clear search” button clears only the text in the search box.
It does not clear any existing filters applied in the left column,
see [Filtered Search]({% link filtered-search.md %}).

You can change the number of results displayed on a page.
Results can be sorted by relevance, title or the date of data collection.
Note: If the study metadata did not contain the date in a standardised format,
these studies come up last and are not sorted by date.
