# FAO FAOSTAT

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
