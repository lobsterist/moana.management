# moana.management

One-page static site for Moana Management OÜ, a boutique management consultancy.

- Single self-contained `public/index.html` — no build step, no dependencies.
- Served as a Cloudflare Worker with static assets (`wrangler.jsonc`), deployed from this repository via Workers Builds.
  - Build command: *(empty)*
  - Deploy command: `npx wrangler deploy`
- Domain `moana.management` is registered at Gandi.
