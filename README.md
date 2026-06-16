# European Space Agency (ESA) (esa)

The European Space Agency (ESA) provides public REST and standards-based APIs spanning Copernicus Earth observation (OData, STAC, Sentinel Hub, openEO, OGC, S3, On-Demand Processing), space weather monitoring (HAPI), astronomical mission archives (Gaia TAP, ESASky Legacy TAP), scientific data labs (Datalabs GraphQL), and climate change initiative datasets (ESGF, THREDDS, OpenSearch). Data includes Sentinel satellite imagery, solar and heliospheric time-series, gamma-ray and stellar catalogues, and multi-mission Earth observation products from European space programs.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/esa/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/esa/refs/heads/main/apis.yml)

## Tags

- Earth Observation
- Copernicus
- Sentinel
- Space Weather
- Astronomy
- Satellite Data
- Climate
- Geospatial
- STAC
- OData

## Timestamps

- **Created:** 2026-06-13
- **Modified:** 2026-06-13

## APIs

### Copernicus Data Space OData Catalogue API

OData-based catalogue interface for searching and downloading Copernicus Earth observation products from the Copernicus Data Space Ecosystem. Supports querying by spatial footprint, acquisition date, product type, and collection name across Sentinel-1, Sentinel-2, Sentinel-3, Sentinel-5P, and other missions. Exposes OData query parameters including $filter, $orderby, $top, $skip, $count, $expand, and $select. A 30-day rolling monthly transfer limit of 12 TB applies under the free tier, with bandwidth per connection capped at 20 MB/s.

- **Human URL:** [https://documentation.dataspace.copernicus.eu/APIs/OData.html](https://documentation.dataspace.copernicus.eu/APIs/OData.html)
- **Base URL:** `https://catalogue.dataspace.copernicus.eu/odata/v1`

#### Tags

- Earth Observation
- Copernicus
- Sentinel
- OData
- Catalogue
- Product Download

#### Properties

- [Documentation](https://documentation.dataspace.copernicus.eu/APIs/OData.html)

### Copernicus Data Space STAC Catalogue API

SpatioTemporal Asset Catalogue (STAC) implementation for the Copernicus Data Space Ecosystem. Provides standardised metadata discovery for Earth Observation data including Sentinel missions. Follows the open STAC specification to enable interoperable access to asset-level metadata with spatial information, temporal coverage, and data specifications. Connects to the same underlying database as the OData interface, ensuring consistency across access methods.

- **Human URL:** [https://documentation.dataspace.copernicus.eu/APIs/STAC.html](https://documentation.dataspace.copernicus.eu/APIs/STAC.html)
- **Base URL:** `https://stac.dataspace.copernicus.eu/v1`

#### Tags

- Earth Observation
- Copernicus
- STAC
- Catalogue
- Geospatial
- Sentinel

#### Properties

- [Documentation](https://documentation.dataspace.copernicus.eu/APIs/STAC.html)
- [OpenAPI](openapi/esa-copernicus-stac-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Copernicus Sentinel Hub API

RESTful API interface providing access to various satellite imagery archives including raw data, rendered images, and statistical analysis without requiring local data downloads. Supports configurable processing expressions, multi-temporal analysis, and cloud-optimised access. Free tier allows 10,000 requests and 10,000 processing units per month, with a rate limit of 300 requests/minute and 300 processing units/minute.

- **Human URL:** [https://documentation.dataspace.copernicus.eu/APIs/SentinelHub.html](https://documentation.dataspace.copernicus.eu/APIs/SentinelHub.html)
- **Base URL:** `https://sh.dataspace.copernicus.eu`

#### Tags

- Earth Observation
- Sentinel
- Satellite Imagery
- Processing
- Copernicus

#### Properties

- [Documentation](https://documentation.dataspace.copernicus.eu/APIs/SentinelHub.html)

### Copernicus openEO API

Standardised openEO interface enabling programmatic access and cloud processing of Earth observation datasets without local data management. Supports automatic scaling on cloud infrastructure. The free tier provides 10,000 credits per user per month, a rate limit of 12 requests/minute (1 per 5 seconds), and a maximum of 2 concurrent API requests.

- **Human URL:** [https://dataspace.copernicus.eu/analyse/apis/openeo-api](https://dataspace.copernicus.eu/analyse/apis/openeo-api)
- **Base URL:** `https://openeo.dataspace.copernicus.eu`

#### Tags

- Earth Observation
- Copernicus
- openEO
- Processing
- Cloud

#### Properties

- [Documentation](https://dataspace.copernicus.eu/analyse/apis/openeo-api)

### Copernicus OGC API (WMS/WMTS/WFS/WCS)

OGC-compliant web services providing seamless satellite data access through standard GIS applications. Exposes WMS (Web Map Service), WMTS (Web Map Tile Service), WFS (Web Feature Service), and WCS (Web Coverage Service) endpoints for Copernicus mission data. Suitable for direct integration into GIS tools without downloading or local data processing.

- **Human URL:** [https://documentation.dataspace.copernicus.eu/APIs/SentinelHub/OGC.html](https://documentation.dataspace.copernicus.eu/APIs/SentinelHub/OGC.html)
- **Base URL:** `https://services.sentinel-hub.com/ogc`

#### Tags

- Earth Observation
- OGC
- WMS
- WFS
- WCS
- GIS
- Copernicus

#### Properties

- [Documentation](https://documentation.dataspace.copernicus.eu/APIs/SentinelHub/OGC.html)

### Copernicus On-Demand Processing (ODP) API

Serverless computation service for generating higher-level products from archived lower-level Copernicus data using ESA processors. Supports single-item and batch processing workflows including CARD-BS (Backscatter) and CARD-COH6/12 (Coherence) products from Sentinel-1 SAR data.

- **Human URL:** [https://documentation.dataspace.copernicus.eu/APIs/On-Demand%20Production%20API.html](https://documentation.dataspace.copernicus.eu/APIs/On-Demand%20Production%20API.html)
- **Base URL:** `https://odp.dataspace.copernicus.eu`

#### Tags

- Earth Observation
- Copernicus
- Sentinel-1
- SAR
- Processing
- On-Demand

#### Properties

- [Documentation](https://documentation.dataspace.copernicus.eu/APIs/On-Demand%20Production%20API.html)

### ESA Space Weather HAPI Server

Heliophysics Application Programmer's Interface (HAPI) server providing access to ESA Space Weather Service Network data. Implements the COSPAR-recommended HAPI standard for streaming heliophysics time-series data. Endpoints include catalog (dataset listing), info (parameter definitions), data (time-range streaming), capabilities, and about. Authentication requires an ESA SSO M2M client-id/secret pair exchanged for a short-lived Bearer token (expires 300 seconds) via https://sso.s2p.esa.int/realms/swe/protocol/openid-connect/token.

- **Human URL:** [https://swe.ssa.esa.int/swe-hapi-server](https://swe.ssa.esa.int/swe-hapi-server)
- **Base URL:** `https://swe.ssa.esa.int/hapi`

#### Tags

- Space Weather
- Heliophysics
- HAPI
- Solar
- Time Series

#### Properties

- [Documentation](https://swe.ssa.esa.int/swe-hapi-server)

### ESA Gaia Archive TAP API

Table Access Protocol (TAP) service for the ESA Gaia stellar catalogue, the most precise astrometric survey of the Milky Way. Enables ADQL (Astronomical Data Query Language) queries against Gaia Data Releases covering positions, parallaxes, proper motions, photometry, and radial velocities for over a billion stars. Accessible programmatically via the astroquery Python library.

- **Human URL:** [https://www.cosmos.esa.int/web/gaia-users/archive/programmatic-access](https://www.cosmos.esa.int/web/gaia-users/archive/programmatic-access)
- **Base URL:** `https://gea.esac.esa.int/tap-server/tap`

#### Tags

- Astronomy
- Gaia
- TAP
- Stellar Catalogue
- Astrometry

#### Properties

- [Documentation](https://www.cosmos.esa.int/web/gaia-users/archive/programmatic-access)

### ESASky Legacy TAP Service

IVOA Table Access Protocol (TAP) service providing access to ESA legacy mission archives including Hipparcos (~118,000 stars with milliarcsecond accuracy, 42 data products across 59 tables), Cos-B gamma-ray observations (252 high-level products across six energy ranges), and CoRoT exoplanet/asteroseismology data (177,382 faint-star observations and 171 bright-star light curves). Supports ADQL queries and DataLink services.

- **Human URL:** [https://www.cosmos.esa.int/web/esdc/legacy-tap-esa](https://www.cosmos.esa.int/web/esdc/legacy-tap-esa)
- **Base URL:** `http://esaskylegacy.esac.esa.int/esasky-legacy-sl-tap/tap`

#### Tags

- Astronomy
- TAP
- Hipparcos
- CoRoT
- Gaia
- Legacy Archives

#### Properties

- [Documentation](https://www.cosmos.esa.int/web/esdc/legacy-tap-esa)

### ESA Datalabs GraphQL API

GraphQL API for managing ESA Datalabs computational environments, data pipelines, data volumes, and user access controls. Provides 50+ query operations (datalab management, pipeline runs, user/role management, data centres) and 80+ mutations (build/create/destroy datalabs, access grants, pipeline execution, workspace management), plus 4 subscription endpoints for real-time monitoring of build progress and pipeline runs. Requires an ESA Cosmos CAS LDAP account with a Bearer token.

- **Human URL:** [https://datalabs.esa.int/api-docs/](https://datalabs.esa.int/api-docs/)
- **Base URL:** `https://datalabs.esa.int/graphql`

#### Tags

- GraphQL
- Data Labs
- Pipelines
- Scientific Computing
- ESA

#### Properties

- [Documentation](https://datalabs.esa.int/api-docs/)

### ESA CCI ESGF RESTful API

Earth System Grid Federation (ESGF) RESTful API providing access to ESA Climate Change Initiative (CCI) observational products aligned with CMIP climate model data through the Obs4MIPs framework. Enables search and retrieval of long-term satellite-derived Essential Climate Variables (ECVs) spanning sea level, sea ice, soil moisture, land cover, and more.

- **Human URL:** [https://climate.esa.int/en/data/apis/](https://climate.esa.int/en/data/apis/)
- **Base URL:** `https://esgf.ceda.ac.uk/esg-search/search`

#### Tags

- Climate
- CCI
- ESGF
- Essential Climate Variables
- Earth Observation

#### Properties

- [Documentation](https://climate.esa.int/en/data/apis/)

## Common Properties

- [Website](https://www.esa.int/)
- [Documentation](https://documentation.dataspace.copernicus.eu/)
- [Git Hub](https://github.com/esa)
- [LinkedIn](https://www.linkedin.com/company/european-space-agency)
- [Plans](plans/esa-plans-pricing.yml)
- [Rate Limits](rate-limits/esa-rate-limits.yml)
- [Fin Ops](finops/esa-finops.yml)
- [J S O N Ld](json-ld/esa-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Graph Q L](graphql/esa-graphql.md)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
