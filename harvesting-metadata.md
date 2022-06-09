---
title: Extracting metadata from the CDC
parent: Home
has_children: false
is_hidden: false
nav_order: 070
---

# {{ page.title }}

## Audience

### Search API

Service Provider staff that want to offer local catalogue users the opportunity to run their search queries against CDC,
to provide them with additional results.

### OAI-PMH endpoint

Data aggregators (such as OpenAIRE, B2Find, GoTriple) can easily harvest the entire contents of the data catalogue.
Record identifiers are unified with those used in the User Interface.

## Purpose

To describe the use of the CDC OAI-PMH endpoint and provide a link to CDC SearchAPI documentation.

## OAI-PMH endpoint description

The [OAI-PMH compliant](https://www.openarchives.org/pmh/) endpoint is located at
[https://datacatalogue.cessda.eu/oai-pmh/v0/oai](https://datacatalogue.cessda.eu/oai-pmh/v0/oai).
It exposes the metadata in DublinCore, DataCite and DDI 2.5 Codebook formats.

Use the standard OAI-PMH verbs to query the endpoint.
For example, to list all the record identifiers and return the results in DDI 2.5 XML format, use
[?verb=ListIdentifiers&metadataPrefix=oai_ddi25](https://datacatalogue.cessda.eu/oai-pmh/v0/oai?verb=ListIdentifiers&metadataPrefix=oai_ddi25)

## Search API description

The CDC Search API documentation is part of the [CESSDA REST API](https://api.tech.cessda.eu/) collection.
It is based on the OpenAPI standard, and as such it is possible to run test queries from within the page.
