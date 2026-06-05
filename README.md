# fal (fal-ai)

fal (Features and Labels, Inc.) is a generative media platform providing the world's fastest API for running image, video, audio, and multimodal generative AI models. Through a unified queue-based REST API at https://queue.fal.run, plus realtime WebSocket and SSE streaming surfaces, fal serves 1,000+ production models — including FLUX, Veo 3, Kling, Wan, Seedream, Nano Banana, and Stable Diffusion — on autoscaling GPU infrastructure. fal Serverless lets developers ship custom models with `@fal.function` / `fal.App` / BYO containers, while fal Compute provides dedicated H100/H200/A100/B200 instances. Trusted by Canva, Perplexity, Poe, and 1.5M+ developers; Series D funded ($140M, Sequoia-led, December 2025); SOC 2 with 99.99% uptime.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/fal-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fal-ai/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI
- Artificial Intelligence
- Generative AI
- Generative Media
- Image Generation
- Video Generation
- Audio Generation
- Inference
- Serverless
- GPU
- MCP

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### fal Model APIs

Unified queue-based REST API for invoking 1,000+ generative image, video, audio, and multimodal models hosted on fal's inference infrastructure. Submit a request to `https://queue.fal.run/{model-id}`, poll `/requests/{request_id}/status` or `/requests/{request_id}` for progress and results, or subscribe to webhook callbacks. Supports synchronous responses, asynchronous queueing, server-sent streaming progress, and request cancellation. Powers flagship models including FLUX, Veo 3, Kling 2.5, Wan 2.5, Seedream, Nano Banana, Qwen, SDXL, and Stable Diffusion variants.

- **Human URL:** [https://fal.ai/docs/model-apis/quickstart](https://fal.ai/docs/model-apis/quickstart)
- **Base URL:** `https://queue.fal.run`

#### Tags

- AI
- Generative AI
- Image Generation
- Video Generation
- Audio Generation
- Multimodal
- Inference

#### Properties

- [Documentation](https://fal.ai/docs/model-apis/quickstart)
- [Documentation](https://fal.ai/models)
- [OpenAPI](openapi/fal-model-apis-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fal-model-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-model-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/fal-queue-request-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/fal-queue-status-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/fal-ai-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### fal Realtime API

WebSocket-based realtime inference for ultra-low latency interactive generative experiences such as LCM/SDXL sketch-to-image, live-portrait, and realtime upscaling. Bi-directional binary/JSON messaging keeps a persistent connection open so each frame, prompt, or pose adjustment is processed in milliseconds. Powers fal.realtime client utilities used in canvas apps, drawing tools, AR experiences, and live video pipelines.

- **Human URL:** [https://fal.ai/docs/model-apis/real-time](https://fal.ai/docs/model-apis/real-time)
- **Base URL:** `wss://realtime.fal.run`

#### Tags

- AI
- Generative AI
- Realtime
- WebSocket
- Streaming
- Inference

#### Properties

- [Documentation](https://fal.ai/docs/model-apis/real-time)
- [Code Examples](https://github.com/fal-ai/real-time-demo-app)
- [AsyncAPI](asyncapi/fal-ai-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/fal-model-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-model-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-serverless-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-serverless-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-storage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-storage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fal Streaming API

HTTP streaming endpoint (`/{model-id}/stream`) that emits progressive partial outputs as a model runs — used for LLM/VLM token streams, incremental video frames, and step-by-step image diffusion previews. Compatible with Server-Sent Events parsers in the official fal-client SDKs.

- **Human URL:** [https://fal.ai/docs/model-apis/streaming](https://fal.ai/docs/model-apis/streaming)
- **Base URL:** `https://queue.fal.run`

#### Tags

- AI
- Generative AI
- Streaming
- Server-Sent Events
- Inference

#### Properties

- [Documentation](https://fal.ai/docs/model-apis/streaming)
- [AsyncAPI](asyncapi/fal-ai-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/fal-model-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-model-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-serverless-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-serverless-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-storage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-storage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fal Storage API

REST endpoints for uploading binary inputs (images, audio clips, reference frames, control maps) to fal's CDN so they can be referenced by URL when invoking model APIs. Issues short-lived signed upload URLs via `/storage/upload/initiate` and serves the resulting assets from `https://v3.fal.media`.

- **Human URL:** [https://fal.ai/docs/model-apis/file-uploads](https://fal.ai/docs/model-apis/file-uploads)
- **Base URL:** `https://rest.alpha.fal.ai`

#### Tags

- AI
- Generative AI
- File Upload
- Storage
- CDN

#### Properties

- [Documentation](https://fal.ai/docs/model-apis/file-uploads)
- [OpenAPI](openapi/fal-storage-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fal-storage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-storage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fal Serverless Platform API

Programmatic management of custom fal Serverless applications — list, inspect, deploy, scale, and monitor user-defined GPU functions deployed with `@fal.function`, `fal.App`, or BYO containers. Covers app metadata, secrets, file volumes, scaling parameters (`keep_alive`, `min_concurrency`), and execution analytics.

- **Human URL:** [https://fal.ai/docs/private-serverless-models](https://fal.ai/docs/private-serverless-models)
- **Base URL:** `https://rest.alpha.fal.ai`

#### Tags

- AI
- Serverless
- GPU
- Deployments
- Platform

#### Properties

- [Documentation](https://fal.ai/docs/private-serverless-models)
- [SDK](https://github.com/fal-ai/fal)
- [OpenAPI](openapi/fal-serverless-platform-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fal-serverless-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-serverless-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fal Models Catalog API

Read-only discovery endpoints for browsing fal's 1,000+ production model catalog, including model metadata, capability tags, pricing per output, supported parameters, example inputs, and OpenAPI schemas per model. Backs the model gallery, search, and SDK tooling.

- **Human URL:** [https://fal.ai/models](https://fal.ai/models)
- **Base URL:** `https://fal.ai`

#### Tags

- AI
- Generative AI
- Catalog
- Discovery

#### Properties

- [Documentation](https://fal.ai/models)
- [Postman Collection](collections/fal-model-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-model-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-serverless-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-serverless-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-storage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-storage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fal Compute API

Provision and manage dedicated GPU instances (H100, H200, A100, B200) with full SSH access for training, fine-tuning, and persistent workloads. Hourly or per-second billing with no lock-in.

- **Human URL:** [https://fal.ai/compute](https://fal.ai/compute)
- **Base URL:** `https://rest.alpha.fal.ai`

#### Tags

- AI
- GPU
- Compute
- Infrastructure
- Dedicated

#### Properties

- [Documentation](https://fal.ai/compute)
- [Postman Collection](collections/fal-model-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-model-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-serverless-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-serverless-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-storage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-storage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fal API Keys API

Manage fal API keys — create, list, scope, and revoke keys used to authenticate against the Model, Storage, Serverless, and Compute APIs via the Authorization: Key $FAL_KEY header.

- **Human URL:** [https://fal.ai/dashboard/keys](https://fal.ai/dashboard/keys)
- **Base URL:** `https://rest.alpha.fal.ai`

#### Tags

- AI
- Administration
- Authentication
- API Keys

#### Properties

- [Documentation](https://fal.ai/dashboard/keys)
- [Postman Collection](collections/fal-model-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-model-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-serverless-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-serverless-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-storage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-storage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fal Usage and Billing API

Programmatic access to usage metrics, per-model spend, GPU-second consumption, and invoicing history. Surfaces the same data shown on the fal dashboard so platform teams can pipe inference cost into internal FinOps tooling.

- **Human URL:** [https://fal.ai/dashboard/usage](https://fal.ai/dashboard/usage)
- **Base URL:** `https://rest.alpha.fal.ai`

#### Tags

- AI
- Administration
- Usage
- Billing
- FinOps

#### Properties

- [Documentation](https://fal.ai/dashboard/usage)
- [Postman Collection](collections/fal-model-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-model-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-serverless-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-serverless-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fal-storage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fal-storage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://fal.ai)
- [Documentation](https://fal.ai/docs)
- [Documentation](https://fal.ai/docs/model-apis/quickstart)
- [Documentation](https://fal.ai/models)
- [Documentation](https://fal.ai/docs/authentication)
- [Documentation](https://fal.ai/docs/model-apis/webhooks)
- [Documentation](https://fal.ai/docs/model-apis/real-time)
- [Documentation](https://fal.ai/docs/model-apis/streaming)
- [Documentation](https://fal.ai/docs/model-apis/file-uploads)
- [Documentation](https://fal.ai/docs/private-serverless-models)
- [Getting Started](https://fal.ai/docs/model-apis/quickstart)
- [Status Page](https://status.fal.ai)
- [Blog](https://blog.fal.ai)
- [Sign Up](https://fal.ai/login)
- [Pricing](https://fal.ai/pricing)
- [Support](https://discord.gg/fal-ai)
- [Forum](https://discord.gg/fal-ai)
- [Terms of Service](https://fal.ai/legal/terms-of-service)
- [Privacy Policy](https://fal.ai/legal/privacy-policy)
- [Trust Center](https://trust.fal.ai)
- [LinkedIn](https://www.linkedin.com/company/featuresandlabels)
- [Twitter](https://twitter.com/fal)
- [GitHub Organization](https://github.com/fal-ai)
- [SDK](https://github.com/fal-ai/fal-client-python)
- [SDK](https://github.com/fal-ai/fal-js)
- [SDK](https://github.com/fal-ai/fal-swift)
- [SDK](https://github.com/fal-ai/fal-java)
- [SDK](https://github.com/fal-ai/fal-dart)
- [SDK](https://github.com/fal-ai/fal)
- [Tool](https://github.com/fal-ai/terraform-provider-fal)
- [Tool](https://github.com/fal-ai/fal-blender-extension)
- [Tool](https://github.com/fal-ai/serverless-vscode)
- [Code Examples](https://github.com/fal-ai/awesome)
- [Code Examples](https://github.com/fal-ai/real-time-demo-app)
- [Code Examples](https://github.com/fal-ai/fal-nextjs-template)
- [Documentation](https://fal.ai/docs/mcp-server)
- [Documentation](https://fal.ai/docs/comfyui)
- [Plans](plans/fal-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/fal-ai-rate-limits.yml)
- [Fin Ops](finops/fal-ai-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
