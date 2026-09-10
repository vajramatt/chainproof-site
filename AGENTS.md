# ChainProof marketing site

This repository contains only the public marketing website for ChainProof. It
is a small static site deployed as an assets-only Cloudflare Worker.

## Repository boundary

- The OSS CLI, TUI, local web explorer, proof format, integrations, and releases
  live in `../chainproof` and at `github.com/vajramatt/chainproof`.
- Do not move application code, the embedded local explorer, accounts,
  billing, tenancy, hosted storage, or product data into this repository.

## Structure and conventions

- `web/index.html` is the site entry point.
- Static assets belong in `web/`; keep the site usable without an application
  backend.
- `wrangler.jsonc` owns the Worker name, asset directory, and custom domains.
- Keep links, install commands, metadata, Open Graph assets, `robots.txt`, and
  `sitemap.xml` consistent when public URLs or product positioning change.
- Keep `web/llms.txt`, visible FAQ answers, and JSON-LD factual, mutually
  consistent, and linked to canonical first-party sources.
- Avoid analytics, remote scripts, third-party fonts, or new build tooling
  unless explicitly requested.

## Development and validation

```sh
npm install
npm run dev
npx wrangler deploy --dry-run --env production
```

The local site runs at `http://localhost:8787`. A production deployment changes
`chainproof.ai` and `www.chainproof.ai`; never run `npm run deploy` without
explicit approval for that specific deployment.
