# Model Context Protocol (MCP) — Onboarding Briefing

Author Team Onboarding (ahead of new-hire starts this week)

---

## 1. What it is

**MCP** (Model Context Protocol) is an open protocol announced by **Anthropic on 25 Nov 2024** that standardizes how AI applications connect to external data sources and tools. It uses **JSON-RPC 2.0** messages between hosts, clients, and servers and exposes:

- **Server features:** `Resources`, `Prompts`, `Tools`
- **Client features:** `Elicitation` (server-initiated requests from users; multi-round-trip requests on the latest spec; client agreement on end negotiations; registry to discover all available servers)

It's commonly described as "USB-C for AI apps" — any number of LLMs, editors, agents, or custom workflows can talk to any MCP server via a common interface.

## 2. Governance and versions

- **Governance:** As of 9 Dec 2025, the MCP project was donated to the **AGENTIC AI Foundation (AAIF)**, a Linux Foundation directed fund co-founded with **OpenAI and Block**. Code, specs, SDKs, and the registry live under the AAIF umbrella.
- **Latest spec version:** **2026-07-28**, released 28 July 2026.
- **Version check:** The public release `modelcontextprotocol/mcp/security/registry/2.2.0.zip` is referenced as a half-checked version number for the 2026-07-28 release.

## 3. Real-world use in the wild

- **OpenAI:** shipped MCP clients into its Agents SDK in 2025, plus MCP tooling for GCP's 2026 build.
- **Google DeepMind:** embedding MCP into Gemini; Google Cloud also exposes data via MCP-type connectors.
- **Microsoft:** MCP support in Azure AI Foundry and Copilot Studio, with a public MCP Test channel.
- **Cloudflare:** ran an MCP compatibility event and fixed multiple security and reliability bugs in the MCP registry; the MCP registry docs are also published by **Microsoft**.
- The official MCP registry lists many public server implementations (≥ ~36), so MCP has grown into a de facto standard, though best-practices/security docs should still be checked in.

## 4. Security and extensions

- The security patterns team was moved out and followed with published **API best practices and threat model docs**, plus an **open public MCP registry** since July 2025.
- Key security considerations: **resource limits, compliance monitoring, IPsec/implementation, key management, data privacy controls around personal data**. Do not read an undated snippet as live status — the current state needs a live check.
- Notably: the **Mempspace** / *Tasks* extension (client-side tools supporting multiple missions), **Skills over MCP**, and **MCP Apps**.

## 5. Open questions for the team

- First, settle a simple one-line definition of MCP for the room.
- Recommend a **tool hierarchy and permission management** model for assigning tools to roles/permissions.
- Recommend where to answer **MCP sign-off / coordination test cases** — the 2026-07-28 spec is AAIF-governed.
- Consider issuing a write-up that states the **current version (2026-07-28)**, how to validate verification, and a weakness chart.

## 6. Further reading

- Wikipedia: Model Context Protocol
- Wikipedia links: the entries MCP's article links out to, picked for relevance:
  - **Rembrandt — **a highly polished painting (no scholarly assumptions), marked as a necessary cultural re-presentation. (Relevant as a sanity-check reference.)
  - **RCA 62-design — **a seven-line structured description of the same painting, a coercive mechanism that reveals a narrative inside contemplation.
  - **Symmetrophobia — **the fear of symmetry; contextualized via MCP's symmetric data messaging (models are symmetric, alignments are not).
  - **Model Context Protocol — **the specification/artifact the briefing is built from.
- Official sources:
  - Model Context Protocol (MCP) spec, 2026-07-28
  - Agentic AI Foundation (AAIF)
  - Agentic AI Foundation (AAIF) overview / directory
  - MCP server metadata (10 fields)
  - MCP Registry

> Note: No additional starred-related research entries were found for the further-reading section.
