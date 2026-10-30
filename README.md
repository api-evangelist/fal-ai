# fal

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

fal (Features and Labels, Inc.) is a generative media platform providing the world's fastest API for running image, video, audio, and multimodal generative AI models. Through a unified queue-based REST API at https://queue.fal.run, plus realtime WebSocket and SSE streaming surfaces, fal serves 1,000+ production models — including FLUX, Veo 3, Kling, Wan, Seedream, Nano Banana, and Stable Diffusion — on autoscaling GPU infrastructure. fal Serverless lets developers ship custom models with `@fal.function` / `fal.App` / BYO containers, while fal Compute provides dedicated H100/H200/A100/B200 instances. Trusted by Canva, Perplexity, Poe, and 1.5M+ developers; Series D funded ($140M, Sequoia-led, December 2025); SOC 2 with 99.99% uptime.

**Areas:** Artificial Intelligence · Generative AI · Generative Media · Image Generation · Video Generation · Audio Generation · Inference · Serverless · GPU · MCP · Real-Time

## fal on APIs.io

Everything profiled for fal is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/fal-ai/](https://apis.io/providers/fal-ai/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [fal Realtime API](https://apis.io/apis/fal-ai/fal-realtime-api/) — WebSocket-based realtime inference for ultra-low latency interactive generative experiences such as LCM/SDXL sketch-to-image, live-portrait, and realtime…
- [fal Streaming API](https://apis.io/apis/fal-ai/fal-streaming-api/) — HTTP streaming endpoint (`/{model-id}/stream`) that emits progressive partial outputs as a model runs — used for LLM/VLM token streams, incremental video…
- [fal Models Catalog API](https://apis.io/apis/fal-ai/fal-models-catalog-api/) — Read-only discovery endpoints for browsing fal's 1,000+ production model catalog, including model metadata, capability tags, pricing per output, supported…
- [fal Compute API](https://apis.io/apis/fal-ai/fal-compute-api/) — Provision and manage dedicated GPU instances (H100, H200, A100, B200) with full SSH access for training, fine-tuning, and persistent workloads. Hourly or…
- [fal API Keys API](https://apis.io/apis/fal-ai/fal-keys-api/) — Manage fal API keys — create, list, scope, and revoke keys used to authenticate against the Model, Storage, Serverless, and Compute APIs via the…
- [fal Usage and Billing API](https://apis.io/apis/fal-ai/fal-usage-billing-api/) — Programmatic access to usage metrics, per-model spend, GPU-second consumption, and invoicing history. Surfaces the same data shown on the fal dashboard so…
- [fal Apps API](https://apis.io/apis/fal-ai/fal-ai-apps-api/) — List and inspect deployed Serverless apps.
- [fal Files API](https://apis.io/apis/fal-ai/fal-ai-files-api/) — Manage files on persistent Serverless `/data` volumes.
- [fal Queue API](https://apis.io/apis/fal-ai/fal-ai-queue-api/) — Submit, inspect, and cancel model inference jobs.
- [fal Secrets API](https://apis.io/apis/fal-ai/fal-ai-secrets-api/) — Manage per-org secrets injected into Serverless runs.
- [fal Storage API](https://apis.io/apis/fal-ai/fal-ai-storage-api/) — Upload binary assets to the fal CDN.
- [fal Streaming API](https://apis.io/apis/fal-ai/fal-ai-streaming-api/) — Server-sent streaming of incremental model output.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (9)

Multi-step workflows that chain operations into a business task.

- [fal Upload, Run Image-To-Image With Webhook](https://apis.io/arazzos/fal-ai/fal-ai-image-to-image-result-workflow/)
- [fal Queue Inference](https://apis.io/arazzos/fal-ai/fal-ai-queue-inference-workflow/)
- [fal Serverless App Discovery](https://apis.io/arazzos/fal-ai/fal-ai-serverless-app-discovery-workflow/)
- [fal Serverless App Files Inspection](https://apis.io/arazzos/fal-ai/fal-ai-serverless-app-files-workflow/)
- [fal Set And Verify Serverless Secret](https://apis.io/arazzos/fal-ai/fal-ai-set-and-verify-secret-workflow/)
- [fal Streaming Inference](https://apis.io/arazzos/fal-ai/fal-ai-stream-inference-workflow/)
- [fal Submit And Conditionally Cancel](https://apis.io/arazzos/fal-ai/fal-ai-submit-and-cancel-workflow/)
- [fal Upload Asset Then Run Inference](https://apis.io/arazzos/fal-ai/fal-ai-upload-then-inference-workflow/)
- [fal Webhook-Backed Submission](https://apis.io/arazzos/fal-ai/fal-ai-webhook-submission-workflow/)

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [fal Event-Driven APIs](https://apis.io/asyncapis/fal-ai/fal-ai-asyncapi/)

#### Event channels (2)

Individual events and webhooks the provider emits.

- [{app_id}/realtime](https://apis.io/channels/fal-ai/app-id-realtime/)
- [{model_id}/requests/{request_id}/status/stream](https://apis.io/channels/fal-ai/model-id-requests-request-id-status-stream/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/fal-ai/](https://apis.io/graphqls/fal-ai/fal-ai-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [fal-ai](https://apis.io/servers/fal-ai/fal-ai/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Fal Ai Agentic Access](https://apis.io/agentic-access/fal-ai/fal-ai-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [fal Image Model Result](https://apis.io/schemas/fal-ai/fal-image-result/)
- [fal Queue Inference Request](https://apis.io/schemas/fal-ai/fal-queue-request/)
- [fal Queue Status Response](https://apis.io/schemas/fal-ai/fal-queue-status/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Fal Ai Structure](https://apis.io/json-structure/fal-ai/fal-ai-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Fal Ai Context](https://apis.io/jsonld/fal-ai/fal-ai-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Fal Ai Vocabulary](https://apis.io/vocabularies/fal-ai/fal-ai-vocabulary/)

#### Examples (3)

Example requests and responses.

- [Fal Flux Schnell Example](https://apis.io/examples/fal-ai/fal-flux-schnell-example/)
- [Fal Storage Upload Example](https://apis.io/examples/fal-ai/fal-storage-upload-example/)
- [Fal Veo3 Video Example](https://apis.io/examples/fal-ai/fal-veo3-video-example/)

#### Collections (12)

Postman and Open Collection request collections.

- [fal Model APIs Apps API](https://apis.io/collections/fal-ai/open-fal-ai-apps-api/)
- [fal Model APIs Apps Files API](https://apis.io/collections/fal-ai/open-fal-ai-files-api/)
- [fal Model APIs Apps Queue API](https://apis.io/collections/fal-ai/open-fal-ai-queue-api/)
- [fal Model APIs Apps Secrets API](https://apis.io/collections/fal-ai/open-fal-ai-secrets-api/)
- [fal Model APIs Apps Storage API](https://apis.io/collections/fal-ai/open-fal-ai-storage-api/)
- [fal Model APIs Apps Streaming API](https://apis.io/collections/fal-ai/open-fal-ai-streaming-api/)
- [fal Model APIs](https://apis.io/collections/fal-ai/open-fal-model-apis/)
- [fal Serverless Platform API](https://apis.io/collections/fal-ai/open-fal-serverless-platform-api/)
- [fal Storage API](https://apis.io/collections/fal-ai/open-fal-storage-api/)
- [fal Model APIs](https://apis.io/collections/fal-ai/postman-fal-model-apis/)
- [fal Serverless Platform API](https://apis.io/collections/fal-ai/postman-fal-serverless-platform-api/)
- [fal Storage API](https://apis.io/collections/fal-ai/postman-fal-storage-api/)

#### Overlays (9)

OpenAPI overlays, including conversational phrasing for each operation.

- [Fal Ai Apps Api Phrasing Overlay](https://apis.io/overlays/fal-ai/fal-ai-apps-api-phrasing-overlay/)
- [Fal Ai Files Api Phrasing Overlay](https://apis.io/overlays/fal-ai/fal-ai-files-api-phrasing-overlay/)
- [Fal Ai Model Apis Overlay](https://apis.io/overlays/fal-ai/fal-ai-model-apis-overlay/)
- [Fal Ai Queue Api Phrasing Overlay](https://apis.io/overlays/fal-ai/fal-ai-queue-api-phrasing-overlay/)
- [Fal Ai Secrets Api Phrasing Overlay](https://apis.io/overlays/fal-ai/fal-ai-secrets-api-phrasing-overlay/)
- [Fal Ai Serverless Platform Api Overlay](https://apis.io/overlays/fal-ai/fal-ai-serverless-platform-api-overlay/)
- [Fal Ai Storage Api Overlay](https://apis.io/overlays/fal-ai/fal-ai-storage-api-overlay/)
- [Fal Ai Storage Api Phrasing Overlay](https://apis.io/overlays/fal-ai/fal-ai-storage-api-phrasing-overlay/)
- [Fal Ai Streaming Api Phrasing Overlay](https://apis.io/overlays/fal-ai/fal-ai-streaming-api-phrasing-overlay/)

#### Governance rules (3)

Spectral rulesets for the provider's contracts.

- [fal — asyncapi rules](https://apis.io/rules/fal-ai/fal-ai-asyncapi-spectral-rules/)
- [fal — jsonschema rules](https://apis.io/rules/fal-ai/fal-ai-jsonschema-spectral-rules/)
- [fal API Rules](https://apis.io/rules/fal-ai/fal-ai-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Fal Ai Authentication](https://apis.io/security/fal-ai/fal-ai-authentication/)
- [Fal Ai Domain Security](https://apis.io/security/fal-ai/fal-ai-domain-security/)
- [Fal Ai Trust Center](https://apis.io/security/fal-ai/fal-ai-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Fal Ai Plans Pricing](https://apis.io/plans/fal-ai/fal-ai-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Fal Ai Rate Limits](https://apis.io/rate-limits/fal-ai/fal-ai-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Fal Ai Finops](https://apis.io/finops/fal-ai/fal-ai-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.fal.ai/)
- [Documentation](https://fal.ai/docs)
- [Getting started](https://fal.ai/docs/model-apis/quickstart)
- [Pricing](https://fal.ai/pricing)
- [Support](https://discord.gg/fal-ai)
- [Blog](https://blog.fal.ai)
- [Trust centre](https://trust.fal.ai)
- [Terms of service](https://fal.ai/legal/terms-of-service)
- [Privacy policy](https://fal.ai/legal/privacy-policy)
- [GitHub](https://github.com/fal-ai)
- [Status](https://status.fal.ai)

## API Evangelist rating

**Kin Score 65.6** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 71.7 |
| Contract quality | 70.7 |
| Contract governance | 18.2 |
| Operational transparency | 34.2 |
| Developer ergonomics | 75.0 |
| Access clarity | 92.1 |

**Agent readiness 48.1** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 27.3** — AI & Biometrics

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/fal-ai/](https://apis.io/providers/fal-ai/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for fal: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/fal-ai/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
