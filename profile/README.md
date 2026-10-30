<div align="center">

# mcpsmiths

**Small, focused MCP servers for observability and cost control.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/mcpsmiths/.github/blob/main/LICENSE)
[![Code of Conduct](https://img.shields.io/badge/code%20of%20conduct-contributor%20covenant-blueviolet.svg)](https://github.com/mcpsmiths/.github/blob/main/CODE_OF_CONDUCT.md)
[![MCP](https://img.shields.io/badge/protocol-MCP-orange.svg)](https://modelcontextprotocol.io)
[![PyPI - tracehub-mcp](https://img.shields.io/pypi/v/tracehub-mcp?label=tracehub-mcp)](https://pypi.org/project/tracehub-mcp/)
[![PyPI - cost-guard-mcp](https://img.shields.io/pypi/v/cost-guard-mcp?label=cost-guard-mcp)](https://pypi.org/project/cost-guard-mcp/)

</div>

---

mcpsmiths builds small, focused [Model Context Protocol](https://modelcontextprotocol.io) servers that give AI agents safer, cheaper access to production infrastructure. Each server does one job well, ships as a standalone PyPI package, and is designed to drop directly into an existing agent's tool belt — no framework lock-in, no bloated dependency tree.

## Servers

| Repo | What it does | Install | Docs |
|---|---|---|---|
| [**tracehub-mcp**](https://github.com/mcpsmiths/tracehub-mcp) | MCP server for querying OpenTelemetry traces across multiple observability backends (Jaeger, Tempo, Traceloop, Datadog, and more) for LLM application debugging. Fork of `traceloop/opentelemetry-mcp-server`. | `pip install tracehub-mcp` | [PyPI](https://pypi.org/project/tracehub-mcp/) |
| [**cost-guard-mcp**](https://github.com/mcpsmiths/cost-guard-mcp) | Pre-flight query cost & result-size guardrails for AI agents across BigQuery and Snowflake — stops a runaway query before it runs, not after the bill arrives. | `pip install cost-guard-mcp` | [PyPI](https://pypi.org/project/cost-guard-mcp/) |

## Why MCP servers, and why these two

Agents that can query your infra are only safe if they can (a) see what's actually happening in production and (b) be stopped from doing something expensive by accident. `tracehub-mcp` covers the first; `cost-guard-mcp` covers the second. Both are single-purpose on purpose: each server is a complete, well-tested implementation of a narrow job rather than a sprawling all-in-one platform.

## Adding your own MCP server here

This org is solo-maintained, but contributions are welcome in two forms:

1. **Improve an existing server** — open an issue or PR directly on [`tracehub-mcp`](https://github.com/mcpsmiths/tracehub-mcp) or [`cost-guard-mcp`](https://github.com/mcpsmiths/cost-guard-mcp). Both repos inherit this org's [Contributing guide](https://github.com/mcpsmiths/.github/blob/main/CONTRIBUTING.md), [Code of Conduct](https://github.com/mcpsmiths/.github/blob/main/CODE_OF_CONDUCT.md), and issue templates automatically.
2. **Propose a new server** — open a [discussion](https://github.com/orgs/mcpsmiths/discussions) describing the tool/backend you'd want an MCP server for. If it fits the "small, focused, one job" ethos above, it's a strong candidate to become the next repo in this org.

New repos in this org start from the same baseline: MIT-licensed, `mcp` + `mcp-server` + `model-context-protocol` topics, a `SECURITY.md`-backed vulnerability-reporting flow, and a listing in the [official MCP registry](https://registry.modelcontextprotocol.io/).

## Security

Both servers execute against real infrastructure (traces, warehouses) on behalf of an LLM agent — treat that access seriously. Report vulnerabilities privately per [SECURITY.md](https://github.com/mcpsmiths/.github/blob/main/SECURITY.md) rather than filing a public issue.

## Roadmap / what's next

- [ ] Publish both servers to the [official MCP Registry](https://registry.modelcontextprotocol.io/) (identity-verified via GitHub OAuth)
- [ ] Submit `cost-guard-mcp` to the [Docker MCP Registry](https://github.com/docker/mcp-registry) for signed/SBOM'd container distribution
- [ ] Enable org-wide Discussions, sourced from `tracehub-mcp`
- [ ] Submit to one well-targeted awesome-list (`punkpeye/awesome-mcp-servers`)
- [ ] Third MCP server — candidates tracked in Discussions

## About

mcpsmiths is an independent, solo-maintained collection of Model Context Protocol servers. Not affiliated with Anthropic, the MCP steering group, or any of the observability/data-warehouse vendors named above — just tools built to make agentic infra access safer.
