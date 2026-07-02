# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

One-page static site for Moana Management OÜ (moana.management), a boutique management consultancy. The entire site is `public/index.html` — self-contained HTML with inline CSS, no build step, no dependencies.

## Deploy

Served as a Cloudflare Worker with static assets (`wrangler.jsonc`, Worker name `moanamanagement`).

- Manual deploy: `npx wrangler deploy`
- Pushes to `main` also auto-deploy via Cloudflare Workers Builds (build command empty, deploy command `npx wrangler deploy`).
- Domain `moana.management` is registered at Gandi; DNS is on Cloudflare.

## Design System
Always read DESIGN.md before making any visual or UI decisions.
All font choices, colors, spacing, and aesthetic direction are defined there.
Do not deviate without explicit user approval.
In QA mode, flag any code that doesn't match DESIGN.md.

## Skill routing

When the user's request matches an available skill, invoke it via the Skill tool. When in doubt, invoke the skill.

Key routing rules:
- Product ideas/brainstorming → invoke /office-hours
- Strategy/scope → invoke /plan-ceo-review
- Architecture → invoke /plan-eng-review
- Design system/plan review → invoke /design-consultation or /plan-design-review
- Full review pipeline → invoke /autoplan
- Bugs/errors → invoke /investigate
- QA/testing site behavior → invoke /qa or /qa-only
- Code review/diff check → invoke /review
- Visual polish → invoke /design-review
- Ship/deploy/PR → invoke /ship or /land-and-deploy
- Save progress → invoke /context-save
- Resume context → invoke /context-restore
- Author a backlog-ready spec/issue → invoke /spec
