# Introhive

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
