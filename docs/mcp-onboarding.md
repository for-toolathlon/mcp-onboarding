# MCP Onboarding Briefing — Model Context Protocol (New Engineer Orientation)

**Intro and What It Is**

The Model Context Protocol (MCP) is an open protocol standardizing how AI applications connect to external data sources and tools — colloquially "USB-C for AI apps": any number of LLMs, editors, agents, or custom workflows can talk to any MCP server via a common interface. It uses JSON-RPC 2.0 messages between hosts, clients, and servers. The MCP spec — announced by Anthropic on 25 November 2024 — was donated in December 2025 to the Linux Foundation's **Agentic AI Foundation (AAIF)**, co-founded with OpenAI and Block, with all code, specs, SDKs and registry under that umbrella.

The most recent spec version was **2026-07-28** (released 28 July 2026). Its advances include a stateless protocol core, multi-round-trip requests, and header-based routing. Server features: Resources, prompts, tools. Client features: Elicitation. Noteable extensions: Tasks, Skills over MCP, MCP Apps.

Facts: The Name Standard specifies features servers expose; the Message Transports spec (e.g., HTTP, stdio, SSE) defines how messages are sent; and the Model Context Protocol Registry to discover servers is maintained by Microsoft.

**Team OK / Decide Section (Slack consensus)**

In the regional-onboarding Slack thread (linyue ma's MCP project-status briefing post), the team decided to issue an MCP onboarding briefing for new engineers, needing:

1. **Current version included** — write the briefing with the current version number, tools to validate it, and a chart of weaknesses.
2. **First run suggested block:** block calendar for the team, create an MCP Test channel, and publish one consolidated MCP writeup.
3. **Integrations suggested:** an onboarding writeup covering the basics, tools, and permissions (authorizations); plus a chart of weaknesses.

A draft cleanup note was also in that briefing (a previously posted "team sign: 1.4.1…" leak and related stuff), which we'd lower-priority.

**Further Reading**

- According Wikipedia, the Wikipedia article on the Model Context Protocol has been sourced.
- The given article itself is the main reference.
- https://github.com/modelcontextprotocol/modelcontextprotocol — the official spec and documentation repository.
- https://github.com/modelcontextprotocol/python-sdk — the official Python SDK for MCP servers and clients.
- https://modelcontextprotocol.io/docs/2026-07 — the specification document (released 28 July 2026).
- https://registry.modelcontextprotocol.io — the public registry that publishes MCP servers.
- https://github.com/oss/next-release/blob/master/2026-06-16 — main MCP bullets for understanding the protocol evolution.
- https://github.com/linear-demo-lio/linux-init-relay — demonstration/server examples.
- https://www.rdkit.org — used in RDKit documentation; relevant as an example of an MCP resource/prompt.

**Open Questions**

- Which new engineers are coming on Monday, and do any have prior MCP exposure?
- Who owns the repo and MCP org membership (AAIF) responsibilities?
- What is the team's entry criteria for access to MCP Test channel / validation tooling?
- Security: resource limits, compliance monitoring, IPsec implementation, key management, data privacy — which should be covered?

_Maintained by for-toolathlon as part of the onboarding-branch briefing PR into `main` of `for-toolathlon/mcp-onboarding`._