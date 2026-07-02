# Design System — Moana Management

> Status: approved and applied to `public/index.html` on 2026-07-02. Preview:
> `~/.gstack/projects/lobsterist-moana.management/designs/design-system-20260702/preview.html`.

## Product Context
- **What this is:** One-page brochure site for Moana Management OÜ, a boutique one-person strategic consultancy.
- **Who it's for:** Credibility checks (Apple developer program review) and occasional prospects. It must read "real, established, senior" at a glance.
- **Space/industry:** Management consulting for professional services companies in IT, and SaaS.
- **Project type:** Marketing site (single static page).
- **The memorable thing:** "Quiet money" — understated, expensive-feeling, senior. Every choice below serves this.

## Aesthetic Direction
- **Direction:** Nordic prospectus — the page reads as one beautifully typeset document (a private memorandum), not a landing page. Notarized, not marketed.
- **Decoration level:** minimal-intentional — thin hairline rules, mono metadata (ref number, date, coordinates), optional faint engraved bathymetric sea-chart etching near the footer. No photography, no illustration, no gradients, no icons.
- **Mood:** A heavy sheet of paper handed across a desk. Mild intimidation, immediate trust: "this is a real person, and he doesn't need me."

## Typography
- **Display/Hero:** Newsreader (500) — editorial old-style serif with optical sizing; reads as print, not word processor.
- **Body:** Newsreader (400) — same voice, 1.1rem, ~58–62ch measure.
- **UI/Labels:** IBM Plex Mono (500), uppercase, letter-spacing 0.18em, 11–12px — metadata, section numerals, legal lines. The serif speaks; the mono certifies.
- **Data/Tables:** IBM Plex Mono (tabular by nature).
- **Code:** IBM Plex Mono.
- **Loading:** Google Fonts (`Newsreader:ital,opsz,wght` + `IBM+Plex+Mono:400;500`); self-host later if desired.
- **Licensed upgrade path:** GT Alpina (Grilli Type) + Berkeley Mono (U.S. Graphics Company) — same roles, drop-in.
- **Scale:** display clamp(2.6rem–4.6rem) / headline 1.5rem / body 1.1rem / secondary 1rem / mono meta 11–12px.
- **Never:** system-ui/Palatino stacks as primary, Inter/Roboto/Space Grotesk, any sans for headings.

## Color
- **Approach:** restrained monochrome plus one wound.
- **Background — Oat paper:** `#F3F0E7` — warmer than the old `#f7f5f0`; laid paper, not off-white theme.
- **Primary text — Sea-black ink:** `#191C1A` — black with a green cast ("deep water", "in the black"). Replaces navy `#0b2239`.
- **Secondary text — Graphite:** `#70746B`.
- **Rules/borders — Hairline:** `#DAD5C6`.
- **Accent — Ledger red:** `#A63A2B` — **appears at most twice per page**: the wave logomark in the signature block, and one underline (under "Profitable growth"). Nowhere else. Replaces gold. The discipline is the brand: we deal in red ink so you stay in the black.
- **Optional — Deep water:** `#21332C` — one full-bleed dark footer band, paper text reversed.
- **Semantic:** not needed on this page; if ever required: success `#3D6B4F`, warning `#9A7B2F`, error `#A63A2B`, info `#4A5D6B` (all desaturated to match).
- **Dark mode:** optional; invert to `#1B1E1C` paper / `#E9E5DA` ink, red lightened to `#C05A48`, hairlines `#33372F`.

## Spacing
- **Base unit:** 8px
- **Density:** spacious — whitespace is the luxury signal.
- **Scale:** 2xs(2) xs(4) sm(8) md(16) lg(24) xl(32) 2xl(48) 3xl(64) 4xl(96)

## Layout
- **Approach:** creative-editorial, single-column document.
- **Grid:** one column; max text measure ~58–62ch; document block max-width 720px.
- **Structure:** mono metadata line → firm name set huge → headline (red underline on the key phrase) → body that begins like a letter → hairline rule → numbered service entries (I. II. III.) → correspondence line (typeset mailto, no button) → signature block footer (name set large + title + legal line + red wave mark + chart etching).
- **No navigation, no buttons, no cards.** Contact is a typeset line.
- **Border radius:** 0 everywhere — documents don't have rounded corners.

## Motion
- **Approach:** none — stillness is the luxury signal.
- **Allowed maximum:** one 300ms ease-out fade on page load. No scroll reveals, no parallax, no hover choreography beyond underline color.

## Voice (copy rules)
- First person singular ("I"), signed — the firm is one senior person and says so.
- Candour over comfort; no "we help clients unlock value" costume plural.
- Registry-grade facts typeset prominently: Reg. 16681278, VAT EE102591132, Maakri tn 23a, 10145 Tallinn, Estonia.

## Decisions Log
| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-07-02 | Initial design system created | /design-consultation; synthesis of lead proposal + independent subagent voice ("Nordic prospectus") |
| 2026-07-02 | Replace navy+gold with ink+ledger-red | Navy/gold is the category default of wealth management; red-once carries a story. AUTO-DECIDED — user was away; confirm before applying to the live site |
| 2026-07-02 | First-person singular copy | One-person firm; "I" is more credible than costume "we". AUTO-DECIDED — confirm |
