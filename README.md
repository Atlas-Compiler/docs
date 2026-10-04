<div align="center">
  <h1>atlas-docs-site</h1>
  <p><strong>Official Public Documentation for Atlas Compiler</strong></p>
  <p>Hosted at <a href="https://docs.atlas-compiler.com">docs.atlas-compiler.com</a></p>
</div>

---

## Overview

This repository contains the public documentation source for Atlas Compiler. All content is written in MDX and powered by [Mintlify](https://mintlify.com).

The public documentation is organized across five main developer sections:

1. **Getting Started** (`get-started/`)
   - Welcome & overview (`introduction.mdx`)
   - 5-Minute Quickstart (`quickstart.mdx`)
   - Authentication & API Keys (`authentication.mdx`)
   - Architecture & Request Lifecycle (`architecture.mdx`)

2. **Guides & Concepts** (`guides/` and `concepts/`)
   - Core guides: Single-Page Compile, Fast Scrape, Site Mapping, Recursive Crawl, Bounded Batch, Webhooks
   - Technical concepts: Compiler Pipeline, Deterministic Markdown, Intermediate Representation, Anti-Bot & Bypass, Execution Engine & Jobs

3. **API Reference** (`api-reference/`)
   - Overview, base URLs, headers, and authentication
   - Single-page endpoints (`compile.mdx`, `scrape.mdx`, `map.mdx`)
   - Async endpoints (`crawl.mdx`, `batch.mdx`, `get-job.mdx`, `cancel-job.mdx`, `job-results.mdx`, `job-errors.mdx`)
   - Workspace & account management
   - RFC 9457 Problem Details error code catalog (`errors.mdx`)

4. **SDKs & Integrations** (`sdk/` and `ai/`)
   - Official client libraries: TypeScript/JavaScript, Python, Go
   - AI & Agent tooling: Model Context Protocol (MCP 2026-07-28), Agent Skills, `llms.txt`

5. **Production & Trust** (`production/`, `benchmarks/`, `changelog/`)
   - Quotas, rate limits, and concurrency
   - Zero Data Retention (ZDR) & Security
   - Enterprise billing & credit ledger
   - Production readiness & reliability
   - Industry benchmarks & methodology
   - Changelog & API stability policies

## Development

```bash
# Validate local documentation files and links
mint validate
mint broken-links
mint a11y

# Start local preview server
mint dev
```

## Security & Export Pipeline

Public documentation is managed via a fail-closed export system. Only files explicitly allowlisted in `public-docs-manifest.json` are packaged for public deployment. Run the verification suite:

```bash
pnpm docs:check
node scripts/export-public-docs.mjs
```
