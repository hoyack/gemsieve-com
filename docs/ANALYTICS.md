# Analytics plan

## Events

`header_waitlist`, `hero_waitlist`, `hero_pilot`, `footer_waitlist`, `waitlist_submit`, and `pilot_submit`. Report conversion by landing path, source, device class, and offer. Never send free-text form fields to analytics.

## Funnel

Landing view → CTA click → form view → consented submit → qualified pilot → activated pilot. The north-star pre-product metric is qualified pilot requests, not raw traffic.

## Activation

The repository ships no analytics endpoint or secret. CTO may activate a privacy-minded provider after domain verification and consent/legal review, then update CSP and document the exact configuration. Retain aggregate data only as long as it remains decision-useful.
