# REAL PHOTO LAB Public Site

Static marketing site for REAL PHOTO LAB.

Current build: `marketing-v1-launch-pricing`

- Price: `$24.99` per listing
- Limit: up to `30` images per listing
- Allowance: `90` total generations per listing
- Email capture: EmailOctopus embed
- Analytics: Cloudflare Web Analytics, enabled from the Cloudflare dashboard
- Cloudflare Pages support: `_headers` and `_redirects`

Run locally with any static server, for example:

```sh
python -m http.server 4173
```

## Cloudflare setup

Use this repo as a static Cloudflare Pages project:

- Build command: leave blank
- Build output directory: `/`
- Production branch: `main`
- Custom domain: `realphotolab.com`

Enable Web Analytics in Cloudflare instead of adding analytics scripts to the HTML:

1. Cloudflare dashboard > Workers & Pages > REAL PHOTO LAB project.
2. Metrics > Web Analytics > Enable.
3. Redeploy the Pages project so Cloudflare injects the beacon.

Recommended domain redirects live in Cloudflare Bulk Redirects:

- `www.realphotolab.com` -> `https://realphotolab.com` with `301`, preserve query string, subpath matching, and preserve path suffix.
- `<project>.pages.dev` -> `https://realphotolab.com` with `301`, preserve query string, subpath matching, and preserve path suffix.
