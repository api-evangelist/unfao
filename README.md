# FAO FAOSTAT

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

APIs.json 0.19 provider profile for the Food and Agriculture Organization (FAO) of the United Nations — FAOSTAT statistical database.

## Overview

FAOSTAT is the world's largest freely accessible database for food and agriculture statistics, maintained by the UN Food and Agriculture Organization. It covers 180+ countries with data from 1961 to the present across 70+ thematic domains.

## APIs

### FAOSTAT Data API

Base URL: `https://fenixservices.fao.org/faostat/api/v1`

No authentication required. Returns JSON or CSV.

Key endpoint patterns:
- `GET /en/groupsanddomains` — list all domain groups and datasets
- `GET /en/definitions/domain/{domain_code}` — metadata for a specific domain
- `GET /en/data/{domain_code}?area=...&item=...&element=...&year=...` — query data
- `GET /en/definitions/types` — list available dimension types

Example domains:
| Code | Description |
|------|-------------|
| QCL | Production: Crops and livestock products |
| FBS | Food Balances (2010-) |
| FS | Food Security and Nutrition Indicators |
| TCL | Trade: Crops and livestock products |
| RL | Land Use |
| EI | Agri-Environmental Indicators: Emissions |
| BE | Bioenergy |
| CP | Consumer Price Indices |
| CAHD | Cost and Affordability of a Healthy Diet |

### FAOSTAT Bulk Download API

Base URL: `https://bulks-faostat.fao.org/production`

- `GET /datasets_E.json` — catalog of all datasets with download URLs and update dates
- `GET /{DatasetName}_E_All_Data_(Normalized).zip` — full normalized dataset download

## Developer Portal

https://www.fao.org/faostat/en/#developer-portal

## Contact

- Email: faostat@fao.org
- Twitter: @FAOstatistics

## License

Data provided under FAO's open data license. No cost. No API key required.
