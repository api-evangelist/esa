# ESA Datalabs GraphQL API

## Title
European Space Agency (ESA) Datalabs GraphQL API

## Description
The ESA Datalabs GraphQL API provides programmatic management of ESA Datalabs computational environments, scientific data pipelines, data volumes, Docker images, workspaces, user access controls, roles, and permissions. It exposes 50+ query operations and 80+ mutation operations covering the full lifecycle of Datalabs instances: build, deploy, start, stop, destroy, monitor, and share. Four subscription endpoints enable real-time streaming of build progress and pipeline run events. The API is rendered using Spectaql and uses standard Bearer token authentication via ESA Cosmos CAS LDAP accounts.

## Endpoint
- **GraphQL endpoint:** `https://datalabs.esa.int/graphql`
- **API documentation (Spectaql):** https://datalabs.esa.int/api-docs/
- **Datalabs platform:** https://datalabs.esa.int/

## Authentication
Requires an ESA Cosmos CAS LDAP account. After login, a Bearer token must be included in the `Authorization` header of each request:
```
Authorization: Bearer <token>
```

## GraphQL Support
ESA Datalabs has a **native GraphQL API** served at `https://datalabs.esa.int/graphql`. The API documentation is auto-generated via Spectaql and publicly available at https://datalabs.esa.int/api-docs/. The schema covers:

- **Queries (50+):** Datalab listing and metadata, pipeline runs and logs, build status, workspace management, user/role/permission lookups, Docker registry inspection, quota retrieval, data centre and data volume queries, announcement and bookmark retrieval.
- **Mutations (80+):** Create/build/start/stop/destroy Datalabs, grant/revoke access, create/run/stop/delete pipelines, manage Docker images and registries, user and role management, workspace operations, announcement administration.
- **Subscriptions (4):** Real-time monitoring of Datalab build progress, pipeline run progress, build log streaming, and deployment monitoring events.

## Notes
- No public introspection may be available without authentication; the schema in `esa-schema.graphql` is reconstructed from the published Spectaql documentation at https://datalabs.esa.int/api-docs/.
- Additional ESA science data services (Gaia Archive, ESASky, Copernicus) use TAP/ADQL, OData, STAC, and OGC protocols rather than GraphQL, and are documented separately in this repository.
- The schema file `esa-schema.graphql` models the Datalabs management domain. Astronomical observation and Earth observation data models are represented as conceptual SDL types drawn from ESA TAP table schemas (Gaia DR3, Hipparcos, STAC, Copernicus OData).
