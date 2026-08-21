# chainproof.ai

The static public website for [ChainProof](https://github.com/vajramatt/chainproof), a local-first provenance ledger for AI agents.

The site is deliberately small: one HTML page, a few static assets, and no application backend. It is served by Cloudflare as an assets-only Worker.

## Develop

```sh
npm install
npm run dev
```

The site opens at `http://localhost:8787`.

## Deploy

```sh
npm run deploy
```

Deployment binds `chainproof.ai` and `www.chainproof.ai`. Production deployment requires an explicit review and approval.

## Relationship to ChainProof

The application, CLI, TUI, provenance specification, and releases live in the [main ChainProof repository](https://github.com/vajramatt/chainproof). This repository contains only the website.

MIT licensed.
