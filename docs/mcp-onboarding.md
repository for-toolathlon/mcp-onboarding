# Model Context Protocol (MCP) Onboarding Briefing

*For new engineers joining the team in the week ahead of Monday.*

## 1. Short Overview

**What it is.** MCP (Model Context Protocol) is an open protocol announced November 25, 2024, that standardizes how AI applications connect to external data sources and tools. It uses JSON-RPC 2.0 messages between **hosts, clients, and servers** and exposes server features (Resources, Prompts, Tools) plus client features like Elicitation. MCP servers act as the data/host layer, and MCP clients as the app-assistant layer — the entire stack hangs on a single standardized interface (described as "USB-C for AI apps").

**Where it stands today.** The latest spec is **2026-07-28** (released July 28, 2026). Governance: as of December 9, 2025, the project was donated to the AGENTIC AI Foundation (AAIF), a Linux Foundation directed fund co-founded with OpenAI and Block; all code, specs, SDKs, and registry live under the AAIF umbrella, and AAIF governance applies.

**What's new in the latest spec** (2026-07-28):
- Stateless protocol core
- Multi-round-trip requests
- Header-based routing
- Server features: **resources**, **prompts**, **tools**
- Client features: **elicitation**
- Notable extensions: **Tasks**, **Skills over MCP**, **MCP Apps**

**What's in the wild:**
- OpenAI ships MCP clients into its Agents SDK (2025); MCP tooling for GCP's 2026 build
- Google DeepMind embedding MCP into Gemini; Google Cloud exposes data via MCP-type connectors
- Microsoft supports MCP in Azure AI Foundry and Copilot Studio, incl. a public MCP Test channel
- Cloudflare ran an MCP compatibility event and fixed security/reliability bugs in the MCP registry
- ~36 public server implementations in the MCP registry
- Extensions: Tasks (multi-mission client server tools), Children behavior programs, MCP Apps, AI GitHub Skills

**Security considerations:** resource limits, compliance monitoring, IPsec-level implementation, key management, data privacy controls around personal/international data; API best practices and threat model docs published; an open public registry (introduced July 2025).

---

## 2. Further Reading (Linked-Entry Suggestions)

The MCP Wikipedia article links to entries relevant to onboardings. Descriptions of the handful most relevant: infer from link lists.

- **Model Context Protocol** — [modelcontextprotocol.io](https://modelcontextprotocol.io) — Official spec, docs, and SDK documentation. Landing page for the protocol itself.
- **JSON-RPC** — The 1999 HTTP-submission-based remote procedure call standard that MCP builds on for its host/client/server messaging.
- **Large Language Model** — Broad category of AI language models MCP targets; foundational reference for agent-context use cases.
- **Agent** — AI system whose core capability is completing tasks through tool use and action execution, the primary consumer of MCP servers.
- **Claude Code** — Anthropic's developer coding assistant for coding workflows; an MCP client and tooling use case discussed in the MCP wild.

---

## 3. Team's Scope Decisions (from Slack)

The team previously discussed brief overview + further-reading for this onboarding briefing. The relevant agreement:

- **Cover:** a short overview, the linked-entry further-reading list, open questions, and a current release/status note.
- **Skip:** the Beijing client-visit briefing and offsite/parks comparison — those are team logistics items outside this briefing's subject and were excluded.
- **Workspace fact:** there is no MCP-related work discussion in the workspace (the last actual discussion dates to December 2025); linyue ma runs the official channels, so use linyue ma as the best internal contact for MCP onboarding questions if needed.

---

## 4. Release Status

The `mcp-onboarding` repo **for-toolathlon/mcp-onboarding** exists, has no pull requests open (0), and has **no releases yet** (latest release endpoint returned 404 — nothing has been published). The briefing can state this current state.

---

## 5. Open Questions for the Team

1. Which specific MCP server servers/clients will the team run for validation, and will "drawing on the current spec (2026-07-28)" need any infrastructure?
2. Would the team want a version/chart documenting known MCP registry weaknesses (security considerations)?
3. Who will champion the first MCP "Test channel" creation and publishing this consolidated writeup?
