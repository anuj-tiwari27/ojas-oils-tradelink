# Ojas Oils & Tradelink — Website

Marketing website for **Ojas Oils & Tradelink**, a specialist oil trading &
brokerage firm in the soybean and mustard complex (Gwalior, Madhya Pradesh,
India). Trusted by the trade since 1993.

## Pages

| File | Page |
| --- | --- |
| `Ojas Oils & Tradelink - Home.html` | Home |
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
# then open http://localhost:8000/Ojas%20Oils%20%26%20Tradelink%20-%20Home.html
```
