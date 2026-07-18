# Feet on the Street — Lake Point Insurance Agency

Internal business-canvassing map & tracker for Lake Point Insurance Agency:
a single-page app (Leaflet map) backed by Supabase for sign-in, roles, and
shared data.

## Hosting (Cloudflare Pages)

This repo contains the built app as **`index.html`** at the root. It is served
as static content with **no build step** — in Cloudflare Pages use:

- **Framework preset:** None
- **Build command:** *(leave empty)*
- **Build output directory:** `/`

Cloudflare Pages redeploys automatically whenever a new `index.html` is pushed.

## Notes

- The build source (template + Python build script) is kept separately; only the
  compiled `index.html` is published here.
- No customer/business data lives in this repo — all of that is stored in the
  Supabase database and loaded at runtime for signed-in users only. The Supabase
  URL and anon key in `index.html` are public by design and protected by
  row-level security.
