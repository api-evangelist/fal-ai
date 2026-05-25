# fal (fal-ai)

fal (Features and Labels, Inc.) is a generative media platform providing the world's fastest API for running image, video, audio, and multimodal generative AI models. Through a unified queue-based REST API at `https://queue.fal.run`, plus realtime WebSocket and SSE streaming surfaces, fal serves 1,000+ production models — including FLUX, Veo 3, Kling, Wan, Seedream, Nano Banana, and Stable Diffusion — on autoscaling GPU infrastructure. fal Serverless lets developers ship custom models with `@fal.function` / `fal.App` / BYO containers, while fal Compute provides dedicated H100/H200/A100/B200 instances. Trusted by Canva, Perplexity, Poe, and 1.5M+ developers; Series D funded ($140M, Sequoia-led, December 2025); SOC 2 with 99.99% uptime.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/fal-ai/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- AI, Artificial Intelligence, Generative AI, Generative Media, Image Generation, Video Generation, Audio Generation, Inference, Serverless, GPU, MCP

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Surfaces

| Surface | Base URL | Pattern |
|---|---|---|
| Queue (Model APIs) | `https://queue.fal.run` | `POST /{model_owner}/{model_name}` → poll `/requests/{id}/status` + `/requests/{id}` |
| Streaming | `https://queue.fal.run` | `POST /{model_owner}/{model_name}/stream` → Server-Sent Events |
| Realtime | `wss://realtime.fal.run` | WebSocket, bi-directional JSON / binary frames |
| Storage / CDN | `https://rest.alpha.fal.ai` → `https://v3.fal.media` | `POST /storage/upload/initiate` then PUT bytes |
| Serverless Platform | `https://rest.alpha.fal.ai` | `/serverless/apps`, `/serverless/secrets`, `/serverless/files` |
| Compute | `https://rest.alpha.fal.ai` | `/compute/instances` |
| Keys | `https://rest.alpha.fal.ai` | `/keys` |
| Usage & Billing | `https://rest.alpha.fal.ai` | `/billing/usage`, `/billing/invoices` |

Authentication is uniform: `Authorization: Key $FAL_KEY`.

## APIs

### fal Model APIs
Unified queue-based REST API for invoking 1,000+ generative image, video, audio, and multimodal models. Submit a job, then poll status, fetch result, or subscribe via webhook.

**Human URL:** [https://fal.ai/docs/model-apis/quickstart](https://fal.ai/docs/model-apis/quickstart)

- [Documentation](https://fal.ai/docs/model-apis/quickstart)
- [Model Gallery](https://fal.ai/models)
- [OpenAPI](openapi/fal-model-apis-openapi.yml)
- [JSON Schema — Queue Request](json-schema/fal-queue-request-schema.json)
- [JSON Schema — Queue Status](json-schema/fal-queue-status-schema.json)
- [JSON Schema — Image Result](json-schema/fal-image-result-schema.json)
- [JSON-LD](json-ld/fal-ai-context.jsonld)
- [Naftiko Capability — Queue](capabilities/model-apis-queue.yaml)
- [Example — FLUX Schnell](examples/fal-flux-schnell-example.json)
- [Example — Veo 3 Video](examples/fal-veo3-video-example.json)

### fal Realtime API
WebSocket-based realtime inference at `wss://realtime.fal.run` for ultra-low-latency interactive generation (LCM SDXL, LivePortrait, BiRefNet).

**Human URL:** [https://fal.ai/docs/model-apis/real-time](https://fal.ai/docs/model-apis/real-time)

### fal Streaming API
Server-Sent Events stream of incremental output via `POST /{model_owner}/{model_name}/stream`.

**Human URL:** [https://fal.ai/docs/model-apis/streaming](https://fal.ai/docs/model-apis/streaming)

### fal Storage API
Initiate signed uploads of binary assets to the fal CDN so they can be passed by URL to model APIs.

**Human URL:** [https://fal.ai/docs/model-apis/file-uploads](https://fal.ai/docs/model-apis/file-uploads)

- [OpenAPI](openapi/fal-storage-api-openapi.yml)
- [Naftiko Capability — Files](capabilities/storage-files.yaml)
- [Example — Upload Flow](examples/fal-storage-upload-example.json)

### fal Serverless Platform API
Programmatic management of custom Serverless apps deployed with `@fal.function`, `fal.App`, or BYO containers.

**Human URL:** [https://fal.ai/docs/private-serverless-models](https://fal.ai/docs/private-serverless-models)

- [OpenAPI](openapi/fal-serverless-platform-api-openapi.yml)
- [Naftiko Capability — Apps](capabilities/serverless-apps.yaml)

### fal Models Catalog API
Read-only discovery endpoints for the 1,000+ model gallery, including pricing, parameters, and per-model schemas.

**Human URL:** [https://fal.ai/models](https://fal.ai/models)

- [Naftiko Capability — Catalog](capabilities/models-catalog.yaml)

### fal Compute API
Provision and manage dedicated GPU instances (H100, H200, A100, B200) with full SSH access.

**Human URL:** [https://fal.ai/compute](https://fal.ai/compute)

- [Naftiko Capability — Instances](capabilities/compute-instances.yaml)

### fal API Keys API
Create, list, scope, and revoke API keys used for `Authorization: Key $FAL_KEY`.

**Human URL:** [https://fal.ai/dashboard/keys](https://fal.ai/dashboard/keys)

- [Naftiko Capability — Keys](capabilities/keys-management.yaml)

### fal Usage and Billing API
Programmatic access to per-model spend, GPU-second consumption, and invoicing history.

**Human URL:** [https://fal.ai/dashboard/usage](https://fal.ai/dashboard/usage)

- [Naftiko Capability — Usage and Billing](capabilities/usage-billing.yaml)

## Featured Models

| Category | Examples |
|---|---|
| Image | FLUX (Schnell / Dev / Pro / Kontext Pro), Seedream V4, Nano Banana, Qwen, SDXL, SD3, Ideogram, Recraft |
| Video | Veo 3, Kling 2.5 Turbo Pro, Wan 2.5, Seedance 2.0, Ovi, Hunyuan, Sora-class |
| Audio / Voice | Inworld TTS-1.5, ElevenLabs, MMAudio, MusicGen, Stable Audio |
| 3D / Multimodal | TripoSR, Hunyuan3D, LivePortrait, FaceChain |
| Realtime | LCM SDXL, BiRefNet, LivePortrait |

## Pricing (selected)

| Item | Unit | Price |
|---|---|---|
| Seedream V4 | image | $0.03 (33 / $1) |
| FLUX Kontext Pro | image | $0.04 (25 / $1) |
| Nano Banana | image | $0.0398 |
| Qwen Image | megapixel | $0.02 (50 MP / $1) |
| Wan 2.5 | video second | $0.05 (20 s / $1) |
| Kling 2.5 Turbo Pro | video second | $0.07 (14 s / $1) |
| Veo 3 | video second | $0.40 (3 s / $1) |
| H100 80GB | GPU hour | $1.89 |
| H200 141GB | GPU hour | $2.10 |
| A100 40GB | GPU hour | $0.99 |
| B200 184GB | GPU hour | Custom |

See [plans/fal-ai-plans-pricing.yml](plans/fal-ai-plans-pricing.yml) for the full reconciled pricing surface.

## SDKs and Tools

| Language / Tool | Repo |
|---|---|
| Python (model client) | [fal-ai/fal-client-python](https://github.com/fal-ai/fal-client-python) |
| Python (serverless SDK + CLI) | [fal-ai/fal](https://github.com/fal-ai/fal) |
| JavaScript / TypeScript | [fal-ai/fal-js](https://github.com/fal-ai/fal-js) |
| Swift | [fal-ai/fal-swift](https://github.com/fal-ai/fal-swift) |
| Java / Kotlin | [fal-ai/fal-java](https://github.com/fal-ai/fal-java) |
| Dart / Flutter | [fal-ai/fal-dart](https://github.com/fal-ai/fal-dart) |
| Terraform Provider | [fal-ai/terraform-provider-fal](https://github.com/fal-ai/terraform-provider-fal) |
| Blender Extension | [fal-ai/fal-blender-extension](https://github.com/fal-ai/fal-blender-extension) |
| VS Code (Serverless) | [fal-ai/serverless-vscode](https://github.com/fal-ai/serverless-vscode) |
| MCP Server | https://fal.ai/docs/mcp-server |

## Operational Resources

- [Status Page](https://status.fal.ai) — Model API, Serverless API, Dashboard, Serverless Dashboard, Official Models
- [Pricing](https://fal.ai/pricing)
- [Blog](https://blog.fal.ai)
- [Trust Center](https://trust.fal.ai)
- [Discord](https://discord.gg/fal-ai)

## Standards Artifacts

- [Plans](plans/fal-ai-plans-pricing.yml) — API Commons Plans 0.1
- [Rate Limits](rate-limits/fal-ai-rate-limits.yml) — API Commons Rate Limits 0.1
- [FinOps](finops/fal-ai-finops.yml) — FOCUS-aligned billing definition
- [Spectral Rules](rules/fal-ai-rules.yml)
- [Vocabulary](vocabulary/fal-ai-vocabulary.yml)
- [JSON Structure](json-structure/fal-ai-structure.json)

## Maintainer

- Kin Lane — [API Evangelist](https://apievangelist.com) — `info@apievangelist.com`
