# Deployment, monitoring, and rollback

## Preview

Push the feature branch and use a disposable review deployment. A preview proves rendering only; it does not prove Netlify form handling.

## Production runbook (CTO-owned)

1. Review and approve the open PR; do not bypass branch protections.
2. Snapshot existing A/AAAA/CNAME/MX/TXT/DKIM/DMARC and current TLS behavior.
3. Create/link the Netlify site from the approved repository; publish root with no build command.
4. Configure approved analytics names only if activated; update CSP deliberately.
5. Submit one tagged waitlist and pilot test; verify receipt, spam controls, consent fields, source, offer, and success route.
6. Change only required web DNS records. Preserve mail records. Verify apex and `www` HTTPS and redirects.
7. Run `BASE_URL=https://gemsieve.com npm test` and record results.

## Monitoring

Every five minutes: apex HTTPS, expected title, `/waitlist/`, and certificate validity. Daily: form delivery canary where policy permits. Alert the content owner on canonical/robots/sitemap drift.

## Rollback

Re-publish the last known-good Netlify deploy. If DNS changed, restore the recorded web records only. Do not alter MX/TXT/DKIM/DMARC. Re-run HTTPS, route, and form checks and record incident timing.
