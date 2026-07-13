# GemSieve

Production-ready static MVP for [gemsieve.com](https://gemsieve.com): filter intelligence for explainable, defensible shortlists.

## Product boundary

GemSieve helps teams filter noisy research, deal flow, content, and vendor inputs. “Gem” is a metaphor. This is not jewelry commerce, appraisal, certification, or a physical-gem marketplace.

## Routes

- `/` positioning and workflow
- `/product/` sieve anatomy
- `/use-cases/` research, deal flow, vendor, and content examples
- `/waitlist/` early-access Netlify form
- `/pilot/` pilot discovery Netlify form
- `/privacy/`, `/terms/`, `/disclosure/`

## Local development

```bash
npm ci
npm run serve
# open http://localhost:4173
```

## Verification

```bash
npx playwright install chromium
npm run test:all
npm audit --audit-level=moderate
```

## Deployment

Netlify publishes the repository root with no build command. The CTO owns merge, production site linkage, environment configuration, DNS snapshots and changes, HTTPS, form-delivery proof, analytics activation, monitoring, and rollback. See `docs/DEPLOYMENT.md`. No secrets belong in this repository.
