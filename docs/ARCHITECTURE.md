# Architecture

Static semantic HTML, shared CSS, and 621 bytes of progressive JavaScript. Netlify serves the repository root and detects two static forms. There is no client framework, application database, authentication, or committed runtime secret.

## Security and privacy

CSP defaults to self; inline scripts are prohibited. Headers deny framing, MIME sniffing, camera, microphone, and geolocation. Forms require explicit consent, use honeypots, collect only workflow-relevant fields, and preserve source/offer attribution. Netlify spam controls and delivery must be proven in production.

## Accessibility and performance

Semantic landmarks, one H1 per route, skip link, labeled controls, visible focus, 48px navigation controls, reduced-motion support, responsive layouts, no remote font dependency, and an original raster social card.
