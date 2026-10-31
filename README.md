# Predoc

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Predoc is an AI-native medical records platform that automates the retrieval, aggregation, normalization, de-duplication, and structured delivery of complete patient histories. It queries health information exchanges (HIEs) and initiates outreach to non-connected providers, ingests faxes, PDFs, and digital formats, and delivers clean, FHIR-compliant clinical data to healthcare organizations and clinical research teams via a REST Partner API, file exports, or direct EHR integration. The Predoc Partner API (v1.4.1) exposes patient management, record-retrieval requests, record uploads, granular clinical document endpoints (medications, labs, imaging, procedures, notes, vaccines, allergies), clinical summaries, and webhook event notifications, secured with short-lived JWT bearer tokens.

**Areas:** Company · Healthcare · Medical Records · Health Information Exchange · FHIR · Clinical Data · Artificial Intelligence · Interoperability · EHR Integration · Webhook · Clinical Research

## Predoc on APIs.io

Everything profiled for Predoc is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/predoc/](https://apis.io/providers/predoc/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [Predoc Authentication API](https://apis.io/apis/predoc/predoc-authentication-api/) — The Authentication API from Predoc — 1 operation(s) for authentication.
- [Predoc Documents API](https://apis.io/apis/predoc/predoc-documents-api/) — The Documents API from Predoc — 1 operation(s) for documents.
- [Predoc Events API](https://apis.io/apis/predoc/predoc-events-api/) — The Events API from Predoc — 2 operation(s) for events.
- [Predoc Patient API](https://apis.io/apis/predoc/predoc-patient-api/) — The Patient API from Predoc — 23 operation(s) for patient.
- [Predoc Record Request API](https://apis.io/apis/predoc/predoc-record-request-api/) — The Record Request API from Predoc — 3 operation(s) for record request.
- [Predoc Record Upload API](https://apis.io/apis/predoc/predoc-record-upload-api/) — The Record Upload API from Predoc — 3 operation(s) for record upload.
- [Predoc Retrieval API](https://apis.io/apis/predoc/predoc-retrieval-api/) — The Retrieval API from Predoc — 2 operation(s) for retrieval.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Predoc Webhooks](https://apis.io/asyncapis/predoc/predoc-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [predoc](https://apis.io/servers/predoc/predoc/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Predoc Agentic Access](https://apis.io/agentic-access/predoc/predoc-agentic-access/)

#### JSON Schema (6)

The data models the API reads and writes.

- [CreateCrrInpDto](https://apis.io/schemas/predoc/predoc-create-crr-inp-dto/)
- [CreatePatientV2InpDto](https://apis.io/schemas/predoc/predoc-create-patient-v2-inp-dto/)
- [CreatePatientWithCrrV2InpDto](https://apis.io/schemas/predoc/predoc-create-patient-with-crr-v2-inp-dto/)
- [ModifyCrrInpDto](https://apis.io/schemas/predoc/predoc-modify-crr-inp-dto/)
- [PatientInfoResponseDto](https://apis.io/schemas/predoc/predoc-patient-info-response-dto/)
- [UpdatePatientInformationInpDto](https://apis.io/schemas/predoc/predoc-update-patient-information-inp-dto/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Predoc Context](https://apis.io/jsonld/predoc/predoc-context/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Predoc API Rules](https://apis.io/rules/predoc/predoc-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Predoc Authentication](https://apis.io/security/predoc/predoc-authentication/)
- [Predoc Domain Security](https://apis.io/security/predoc/predoc-domain-security/)
- [Predoc Trust Center](https://apis.io/security/predoc/predoc-trust-center/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.predoc.ai)
- [Documentation](https://docs.predoc.ai)
- [Getting started](https://www.predoc.ai/get-started)
- [API reference](https://docs.predoc.ai/reference)
- [Support](https://www.predoc.ai/contact)
- [Changelog](https://docs.predoc.ai/changelog)
- [Blog](https://www.predoc.ai/blog)
- [Compliance](https://www.predoc.ai/security-compliance)
- [Terms of service](https://www.predoc.ai/terms-of-service)
- [Privacy policy](https://www.predoc.ai/privacy)
- [Status](https://predoc.statuspage.io)

## API Evangelist rating

**Kin Score 55.0** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 68.4 |
| Contract governance | 35.6 |
| Operational transparency | 39.5 |
| Developer ergonomics | 53.0 |
| Access clarity | 43.4 |

**Agent readiness 26.4** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 27.9** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/predoc/](https://apis.io/providers/predoc/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Predoc: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/predoc/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
