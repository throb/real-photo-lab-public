# REAL PHOTO LAB Public Site

Static marketing site for REAL PHOTO LAB.

Current build: `marketing-v1-launch-pricing`

- Price: `$24.99` per listing
- Limit: up to `30` images per listing
- Allowance: `90` total generations per listing
- Email capture: EmailOctopus embed
- Hosting: Vercel
- DNS and object storage: Cloudflare
- Analytics: Vercel Web Analytics and Vercel Speed Insights

Run locally with any static server, for example:

```sh
python -m http.server 4173
```

## Production setup

Use this repo as a static Vercel project:

- Build command: leave blank
- Output directory: `.`
- Production branch: `main`
- Custom domain: `realphotolab.com`

Cloudflare remains the DNS provider:

- Apex/root record: use the record Vercel recommends for the project, commonly `A` -> `76.76.21.21`.
- `www`: use the CNAME Vercel recommends, commonly `cname.vercel-dns.com`.
- Keep records DNS-only unless there is a specific Cloudflare proxy/WAF requirement.

Enable analytics in Vercel:

- Project > Analytics > Enable Web Analytics.
- Project > Speed Insights > Enable Speed Insights.

The HTML loads Vercel analytics scripts only on non-local hosts. Cloudflare Web Analytics is not used by default; if we ever want it, add the manual Cloudflare snippet intentionally instead of switching the site to Cloudflare Pages.
