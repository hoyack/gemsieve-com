# QA evidence

Verified on feature branch `feat/production-mvp` on July 12, 2026.

## Automated checks

- `npm run test:all`: PASS.
- HTML validation: PASS for 9 routes.
- Static checks: PASS for local links, canonical/OG metadata, sitemap, forms, policies, concept boundaries, and 1200×630 raster social card.
- Playwright: PASS for all 9 routes at 1440×900 and 390×844, mobile navigation, both form schemas, horizontal overflow, and console/page errors.
- `npm audit --audit-level=moderate`: 0 vulnerabilities.

## Preview

- URL: `https://gemsieve-com-preview.warp-paradox.workers.dev`
- `BASE_URL=https://gemsieve-com-preview.warp-paradox.workers.dev npm test`: PASS.
- All 9 routes and `/assets/og-card.png`: HTTPS 200.
- Caveat: the temporary Workers preview proves rendering only. It cannot prove Netlify form detection, spam controls, notification delivery, production headers, DNS, or analytics.

## Visual review

Desktop and mobile screenshots are in `docs/screenshots/`. No clipping, horizontal overflow, unreadable control, or broken responsive composition was observed. The primary surface is Decide/Learn: the hero explains one proposition and the instrument panel demonstrates the product without pretending to show customer data.

Slop diagnostic: **0/10**. No tech gradient, default indigo, equal feature-tile grid, accent rail, unearned blur, monument stat, icon toppers, indiscriminate center stack, default Inter, or wrong-surface composition. The acid-green signal-lab vocabulary is tied to the sieve concept and remains consistent.

## Production gate

CTO must still verify the approved Netlify deploy, real form receipt for both forms, privacy/analytics configuration, preserved mail DNS, apex and `www` HTTPS, monitoring, and rollback evidence.
