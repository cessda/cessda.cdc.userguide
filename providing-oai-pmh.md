---
title: Providing metadata
parent: Machine access
grand_parent: Home
has_children: false
is_hidden: false
nav_order: 071
---

# {{ page.title }}

CESSDA DC metadata is based on [DDI Codebook](https://ddialliance.org/Specification/DDI-Codebook/2.5/) and exchanged using [OAI-PMH](https://www.openarchives.org/pmh/).

The metadata is expected to be compliant with the [CESSDA Metadata Model v1.0](https://zenodo.org/record/3543756).
Specifically, the [CESSDA Metadata Profiles](https://cmv.cessda.eu/documentation/profiles.html) must be adopted.

DDI XML file format compliance with CMM can be checked using the [CESSDA Metadata Validator](https://cmv.cessda.eu).

## Compliance

Data Providers must provide an endpoint supporting

- CESSDA compliant metadata in DDI
- Regular updates of the metadata provided
- Persistence of identifiers and endpoint identifier (see [CESSDA Identifers](https://docs.tech.cessda.eu/metadata/oai-pmh-identifiers.html))
- Deletion of records marked as updates
- Provenance records for any records not originating, i.e. aggregated from other sources

## Submitting endpoints to CESSDA

CESSDA Service Providers can contact Main Office to connect their expert with the CESSDA Platform Team.

Required information are

- URL of the OAI-PMH endpoint (e.g. `https://xxx.xxx.xxx/oai-pmh`)
- Metadata prefix (e.g. `oai_ddi25`)
- Set specification, if relevant (e.g. `subject:social-sciences`)
- Name and email address of the person responsible for the endpoint.

## Further reading

Documentation and recommendations for setting up an OAI-PMH endpiont can be found in the [CESSDA Technical Guidelines](https://docs.tech.cessda.eu/metadata/oai-pmh-provider-guidelines.html).

