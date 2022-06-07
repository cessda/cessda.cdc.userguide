---
title: Basic search
parent: Home
has_children: false
is_hidden: false
nav_order: 020
---

# {{ page.title }}

Basic keyword search is provided in the search bar in the upper right.

The number of results is presented in the upper middle.
Results can be sorted by relevance, title, the date of data collection or the publication date of the dataset description.

The search language options are provided next to the search box.
If you want to browse study descriptions in German, for instance, choose German as the language.
Note: some service providers provide study descriptions only in English, regardless of country,
or both in English and in the local language.
Therefore, it is always good to do a search in English as well as in the local language.

Elasticsearch applies autocompletion in the search.
A simple search `discrimin` returns "discrimination", "discriminations", "discriminatory".
To test that you got all the documents, you can use the asterisk (*) after the search term,
e.g. `discrim*`.
Search terms are bolded in the results list.
Clicking on ‘Read more’ in the list opens up the full abstract for the study.

If you use two or more search terms, for example, by entering `equality pay` into the box,
the default between the terms is AND.
This means that datasets where both "equality" and "pay" appear in documentation come up on top in the results.

![Basic search](images/basic-search.png "Basic search")

The 'Clear search' button clears only the text in the search box.
It does not clear any existing filters applied in the left column,
see [Filtered Search]({% link filtered-search.md %}).

Users can change the number of results displayed on a page.
Results can be sorted by relevance, title or the date of data collection.
Users can also sort the results by latest (newest) published.
This allows them to keep track of what has been published on their subject of interest
since they last executed the search.
Note: If the study metadata does not contain the collection or publication date in a standardised format,
these studies come up last and are not sorted by date.

Search terms are bolded in the results list if they occur in the title or abstract.
There is no bolding in the detailed study view.
To get a quick overview of whether a study is relevant, click the abstracts open in the results list.
