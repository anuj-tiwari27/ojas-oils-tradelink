# Ojas Oils & Tradelink — Website

Marketing website for **Ojas Oils & Tradelink**, a specialist oil trading &
brokerage firm in the soybean and mustard complex (Gwalior, Madhya Pradesh,
India). Trusted by the trade since 1993.

## Pages

| File | Page |
| --- | --- |
| `Home.dc.html` | Home (served at `/`) |
| `About.dc.html` | About |
| `Commodities.dc.html` | Commodities |
| `Why-Us.dc.html` | Why Us |
| `Contact.dc.html` | Contact (enquiry form) |

## Tech

The pages are static HTML that render through a small client-side runtime
(`support.js`) which mounts React-style "Design Components" (`<x-dc>` templates
with `data-dc-script` logic). React and ReactDOM are loaded from a CDN at
runtime, so no build step is required.

## Running locally

Because the pages fetch sibling `.dc.html` files, serve the folder over HTTP
rather than opening files directly:

```bash
# Python 3
python -m http.server 8000
# then open http://localhost:8000/Home.dc.html
```

## Deploying (Vercel / static hosts)

This is a plain static site — no build step. `vercel.json` rewrites `/` to
`/Home.dc.html` so the root URL serves the home page. The other pages are
reachable directly (e.g. `/About.dc.html`).
