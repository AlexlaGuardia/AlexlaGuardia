# Hi, I'm Alex.

Most AI agent audit logs say "the bot did it." I build the layer that says who, and whether they should've been allowed to.

## Agent governance

**Warden**: a governed MCP server you can actually point an agent at without crossing your fingers. Per-tool RBAC enforced outside the model, not a prompt asking nicely. LLM-as-judge eval harness, OpenTelemetry tracing on every call.
Live demo, click around: warden.alexlaguardia.dev

**Crumb**: attribution for AI agent tool calls, across MCP and OpenAI function-calling. Tamper-evident flight recorder: Ed25519 chain + Merkle tree anchored to Sigstore Rekor. An operator holding the signing key can rewrite a record and re-sign the whole chain, and per-entry verify still passes.. the public anchor is what catches it anyway. Real RFC 8693 token exchange against a genuine IdP, not a gateway signing its own tokens with a dev key.
Live: crumb.alexlaguardia.dev · verify it yourself: `pip install git+https://github.com/AlexlaGuardia/crumb` then `crumb verify`

**Siege**: runtime MCP red-team harness, the offense leg. It attacks Warden to prove the governance actually holds, not just that it compiles.
github.com/AlexlaGuardia/siege

## Also built

**Guardia Content**: full-stack multi-agent SaaS, designed and built solo. Python/FastAPI backend, Next.js frontend, Stripe billing, an agent pipeline handling styling, captions, QC, and scheduling.

**Supra Engine**: 3D game engine from scratch in Rust. Custom ECS, a wgpu renderer, physics via rapier3d. ~85K lines, 8 crates. Off-thesis for the job hunt, on-thesis for whether I can hold a big system in my head.

**Akatskii**: cognitive layer that routes calls across LLMs by complexity, semantic/vector memory, agentic tool loops. There's a trading system and an MCP server with 70+ tools under here too, if you keep scrolling my repos.

Started building Dec 2025. Self-taught, no CS background. Merged a fix into fastmcp's CodeMode sandbox (the e2e test path had zero coverage) a few months in, which is the part I actually point people to.

## Stack
Python · Rust · TypeScript · FastAPI · Next.js · React · MCP · wgpu · SQLite · OpenTelemetry · Cloudflare · PM2

## Links
[Portfolio](https://alexlaguardia.dev) · [LinkedIn](https://www.linkedin.com/in/alex-laguardia-a28a37216/) · [Crumb](https://crumb.alexlaguardia.dev) · [Warden](https://warden.alexlaguardia.dev)
