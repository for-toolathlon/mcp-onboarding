# Model Context Protocol (MCP) Onboarding Briefing

## Overview

**Model Context Protocol (MCP)** is an open protocol standardizing how AI applications connect to external data sources and tools. Announced by Anthropic on 25 November 2024, MCP uses JSON-RPC 2.0 messages between hosts, clients, and servers. It exposes server features — **Resources**, **Prompts**, and **Tools** — plus client features such as **Elicitation** (server-initiated requests from users), **multi-round-trip requests**, client **Agreement**, and the **Registry** for discovering available servers. As of 2026-07-28 the latest release introduced a stateless protocol core, multi-round-trip requests, and header-based routing. As of 2025-09 (registry open public), the latest standard version is 2026-07-28; governance passed to the AGENTIC AI foundation (AAIF), a Linux Foundation directed fund co-founded with OpenAI and Block, in December 2025, where all code, specs, SDKs, and registry live.

**What's in the wild:** OpenAI ships MCP clients in its Agents SDK (2025) and MCP tooling for Google Cloud builds; Google DeepMind embeds MCP into Gemini; Microsoft exposes MCP support in Azure AI Foundry and Copilot Studio; Cloudflare ran an MCP compatibility event; the MCP registry lists many public server implementations, having grown into a de facto standard.

## Further Reading (Linked Wikipedia Entries)

- **Model Context Protocol (MCP)** — article page, https://modelcontextprotocol.io
- **JSON-RPC 2.0** — open standard for remote procedure call; MCP relies on it for host, client, and server communication.
- **AGENTIC AI foundation** — Linux Foundation directed fund under which MCP spec, code, SDKs, and registry reside; co-founded with OpenAI and Block.
- **Agent** (AI agent) — umbrella term for applications that use MCP to automate tasks with tools.
- **Prompt injection** — risk of a prompt being tampered with; relevant to MCP security considerations.
- **Restricted CData** (CData) — data representation standard referenced in MCP registry documentation.
- **Instrumenting enterprise data integration** (DG Container) — could provide context for MCP server architecture adoption.
- **Extension model** (extension) — reference implementation for MCP extensions.
- **Computer vision** (CV) — example domain where MCP servers apply to tools and data.
- **Multimodal chat** (LLM Engineering) — reference textbook appendix for AI agent skills.
- **Model Context Protocol registry** — public registry of MCP servers, e.g. https://registry.modelcontextprotocol.io
- **MCP specification versions** — format spec v1.0 and the 2026-07-28 release notes.
- **Adaface** — hiring company referenced in "at least two angles covered" style.
- **Bedrock ecosystem** — Google service context for MCP server ecosystems.
- **Prompt, retrieval, and tool use** (article) — agent architecture context.

## Team Scope Decisions (from Slack)

- The conversation with the team that defined the onboarding briefing and what to cover/skip was **not found in the Slack workspace**. The most relevant historical evidence is via linyue ma's own MCP project-status briefings (2026-07-28 spec donation to AGENTIC AI foundation) and an unspecified LLM-generated MCP briefing draft — see further reading section.
- The team-wide, threaded Slack discussion that documents decisions on scope — **no such discussion exists in the workspace**.

## Release Status

No releases are present in the repository (list returns empty).

## Open Questions

- Should the MCP registry include the sample CVE reference? (registry referencing a CVE ID)
- Which Azure connector namespace to host MCP servers? *(explicitly scoped out: registry only, no candidate chosen)*
- Which pilot team gets MCP support first? (from the scope notes)
