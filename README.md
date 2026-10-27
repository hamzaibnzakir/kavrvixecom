# Kavrvix Ecom

Landing page for the Kavrvix ecommerce mentorship. One static page — no build step.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole site (HTML, CSS, JS). Uses anime.js from cdnjs and Archivo / JetBrains Mono from Google Fonts. |
| `proof/` | Student sales screenshots + the student video shown in the "Student sales" wall. |
| `brand/` | Logo files: mark (SVG/PNG), full lockups for dark and light backgrounds, favicon. |

## Things to update

**Social links**: WhatsApp +1 (302) 563-7966, Instagram @Kavrix00_, TikTok @kavrix03, Facebook Kavrix00, Telegram @kavrix. They appear in the footer, the floating WhatsApp button, the "Ask a question first" button and the form success/error messages. To change one, search `index.html` for the old handle.

**Sales proof** — drop new screenshots into `proof/`, then add a line to the `PROOF` list near the top of the `<script>` in `index.html`:

```js
{ src: "proof/sale-17.jpg", caption: "$2,400 first week" },
```

Videos use `{ video: "proof/file.mp4", poster: "proof/poster.jpg", caption: "..." }`.

**Application form** — submissions go to Formspree (`https://formspree.io/f/xrppeblq`). Change `FORM_ENDPOINT` in the script to switch it. The first real submission may ask you to confirm the form in your Formspree inbox.

## Deploy (production)

1. Vercel → Add New Project → import `hamzaibnzakir/kavrvixecom`, branch `main`. Framework preset **Other**, no build command, output directory = root.
2. Add your domain in Vercel → Settings → Domains.
3. After the domain is live, change `og-image.png` in the `og:image` and `twitter:image` tags to the full URL (e.g. `https://kavrvix.com/og-image.png`) so Facebook, WhatsApp and X show the preview card.
4. Submit one test application and confirm the form in the Formspree email (first submission only).

Included: `vercel.json` (clean URLs, caching, security headers), `404.html`, `robots.txt`, `site.webmanifest`, favicons and `og-image.png` (1200×630).

## Brand

- Graphite `#14171B` · Panel `#1B1F25` · Line `#2B313A` · Chalk `#ECEEE6` · Steel `#8D949D` · Volt `#CFF462`
- Type: Archivo at wide width (wdth 125) for headlines, Archivo regular for body, JetBrains Mono for dashboard numbers.
- The mark: a K whose upper arm is a sales chart breaking upward.
