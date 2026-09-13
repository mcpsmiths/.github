# Security Policy

## Reporting a Vulnerability

Both `tracehub-mcp` and `cost-guard-mcp` execute against real infrastructure
(observability backends, data warehouses) on behalf of an LLM agent, so we
take security reports seriously.

**Please do not open a public issue for a security vulnerability.**

Instead, report it privately using GitHub's built-in flow:

1. Go to the affected repository's **Security** tab.
2. Click **"Report a vulnerability"** to open a private security advisory.

If the affected repo doesn't have Security Advisories enabled, use the
[private advisory form on this `.github` repo](https://github.com/mcpsmiths/.github/security/advisories/new)
instead and mention which repo/server it affects.

## Response Time

We aim to acknowledge new reports within **48 hours** and to provide a
remediation timeline once the issue is confirmed.

## Supported Versions

Only the latest published version of each server on PyPI is supported with
security fixes.
