---
title: OAI-PMH endpoint
parent: Machine access
grand_parent: CESSDA Data Catalogue User Guide
has_children: false
is_hidden: false
nav_order: 072
---

# {{ page.title }}

## OAI-PMH endpoint description

The [OAI-PMH compliant](https://www.openarchives.org/pmh/) endpoint is located at
[https://datacatalogue.cessda.eu/oai-pmh/v0/oai](https://datacatalogue.cessda.eu/oai-pmh/v0/oai).

Metadata is provided in the formats

- DublinCore -- `oai_dc`
- DataCite -- `oai_datacite`
- DDI 2.5 Codebook -- `oai_ddi25`

## Functionality

The endpoint offers common OAI-PMH functionality:

- Selective harvesting with Sets & Datestamps
- List request sequence with ResumptionTokens
- OAI-Identifiers
- Deleted records

The endpoint fully implements the specification for [Aggregation](https://www.openarchives.org/OAI/2.0/guidelines-aggregator.htm).

### Specific Sets

The endpoint provides sets specific to languages, the list is available from

  [https://datacatalogue.cessda.eu/oai-pmh/v0/oai?verb=ListSets](https://datacatalogue.cessda.eu/oai-pmh/v0/oai?verb=ListSets)

## Documentation

The endpoint is powered by [Kuha2](https://kuha2.readthedocs.io/en/latest/oai_pmh_repo_handler.html).
