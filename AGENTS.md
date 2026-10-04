# Atlas Public Documentation Instructions

## About this project

- This is the public documentation site for Atlas Compiler, deployed at `docs.atlas-compiler.com`.
- Built on [Mintlify](https://mintlify.com) with MDX pages and YAML frontmatter.
- Configuration lives in `docs.json`.
- Navigation follows a 5-tab developer hierarchy: **Getting Started**, **Guides & Concepts**, **API Reference**, **SDKs & MCP**, and **Production & Trust**.

## Terminology

- Use **workspace** (never project) for the top-level tenancy boundary.
- Use **compiler** or **compilation pipeline** when describing DOM distillation and layout analysis.
- Use **scraper** or **scrape** when referring to raw markdown extraction without visual layout graph analysis.
- Use **crawl** for multi-page automated recursive exploration.
- Use **map** for fast URL and sitemap discovery without content extraction.
- Use **batch** for processing explicit, bounded URL lists.
- Use **RFC 9457 Problem Details** when referencing HTTP error responses.
- Use **Zero Data Retention (ZDR)** when discussing data residency and privacy guarantees.

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise and technically precise.
- Use sentence case for headings.
- Format all code, endpoints, methods, headers, and parameter names in inline code blocks (`POST /v1/compile`, `Authorization`, `x-request-id`).
- All code examples must be executable, copy-paste ready, and use realistic parameters.

## Confidentiality & Content boundaries

- **Public docs site only**: Never include internal cluster topology, private IP addresses, database schemas, internal worker queues, or internal credentials.
- All exported pages must be explicitly registered in `public-docs-manifest.json` and pass the fail-closed airgap export audit (`node scripts/export-public-docs.mjs`).
