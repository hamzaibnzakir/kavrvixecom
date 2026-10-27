# Kavrvix Experts (branch: experts)

Done-for-you ecommerce services marketplace. One static page, no build step.
The mentorship landing page lives on the `main` branch.

**Edit services:** everything is in the `SERVICES` list in the `<script>` of `index.html` (name, category, delivery time, revisions, what you get, what we need, best for, sample images).
**Sample images:** `samples/`. Static and native samples are set in the `STATIC` and `NATIVE` lists.
**Requests** post to the same Formspree endpoint with `request_type`, `services` and `budget` fields.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole site (HTML, CSS, JS). Uses anime.js from cdnjs and Archivo / JetBrains Mono from Google Fonts. |
| `samples/` | Ad creative samples used in the hero, service cards, drawers and the work reel. |
| `brand/` | Logo files: mark (SVG/PNG), full lockups for dark and light backgrounds, favicon. |

## Things to update

**Social links**: WhatsApp +1 (302) 563-7966, Instagram @Kavrix00_, TikTok @kavrix03, Facebook Kavrix00, Telegram @kavrix. Used in the footer, the floating WhatsApp button, the custom quote band and the form messages. Search `index.html` for a handle to change it.

**Application form** — submissions go to Formspree (`https://formspree.io/f/xrppeblq`). Change `FORM_ENDPOINT` in the script to switch it. The first real submission may ask you to confirm the form in your Formspree inbox.

## Deploy (production)

1. Vercel → Add New Project → import `hamzaibnzakir/kavrvixecom`, set the production branch to `experts`. Framework preset **Other**, no build command, output directory = root. (The mentorship site is a second Vercel project on `main`.)
2. Add the domain or subdomain (e.g. `experts.yourdomain.com`) in Vercel → Settings → Domains.
3. Once live, change `og-image.png` in the `og:image` and `twitter:image` tags to the full URL so link previews show on Facebook, WhatsApp and X.
4. Send one test request and confirm the form in the Formspree email (first submission only).

Included: `vercel.json`, `404.html`, `robots.txt`, `site.webmanifest`, favicons and `og-image.png` (1200×630).

## Brand

- Graphite `#14171B` · Panel `#1B1F25` · Line `#2B313A` · Chalk `#ECEEE6` · Steel `#8D949D` · Volt `#CFF462`
- Type: Archivo at wide width (wdth 125) for headlines, Archivo regular for body, JetBrains Mono for dashboard numbers.
- The mark: a K whose upper arm is a sales chart breaking upward.
