# Introhive

Introhive is a relationship intelligence and CRM data automation platform used primarily by professional services firms — law, accounting, consulting and the built environment — to remove manual CRM data entry. It mines employee email and calendar systems to build a firm-wide relationship graph, then cleans, de-duplicates and enriches contact, company and activity records before writing them back into Salesforce, Microsoft Dynamics 365, HubSpot and practice systems.

- Website: https://www.introhive.com/
- Application: https://app.introhive.com/ (regional instances: `app.` US, `ca.` Canada, `uk.` UK)
- Help centre: https://help.introhive.com/en/
- Trust centre: https://trust.introhive.com/
- GitHub: https://github.com/Introhive

## API surface

Introhive publishes **no public developer portal, OpenAPI/Swagger description, GraphQL schema, AsyncAPI document, MCP server or A2A agent card.** The `developer.introhive.com` hostname asserted by third-party API directories does not resolve, and `docs.introhive.com` resolves to Document360 but has no provisioned TLS certificate.

The one machine-readable contract Introhive does serve anonymously is an **RFC 8414 OAuth 2.0 Authorization Server Metadata** document, published identically on each regional platform host — authorization-code and refresh-token grants, PKCE with `S256`, `client_secret_post`/`client_secret_basic` client authentication, and an in-product OAuth application registry behind tenant login. That surface is captured in `well-known/`, `authentication/` and `conformance/`.

## Artifacts

| Directory | Contents |
|---|---|
| `well-known/` | Probe index plus the three verbatim regional OAuth authorization-server metadata documents |
| `authentication/` | OAuth 2.0 profile derived from those discovery documents |
| `conformance/` | Protocol conformance (OAuth2, RFC 8414, PKCE) plus the published compliance programme |
| `security/` | Domain security probe, trust centre, vulnerability disclosure |
| `llms/` | Introhive's own `llms.txt`, saved verbatim |
