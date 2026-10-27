# Kavrvix Ecom (mentorship site, branch `main`)

Landing page for the Kavrvix ecommerce mentorship. Static site, no build step. The Kavrvix Experts services site lives on the `experts` branch of this same repo.

## Go live in 10 minutes

### 1. Fork the repo
On GitHub, open `hamzaibnzakir/kavrvixecom` → **Fork**.
**Untick "Copy the main branch only"** so both sites come with it (`main` = mentorship, `experts` = services).

### 2. Deploy on Vercel
Create **one Vercel project per site**, both from your fork:

| Site | Vercel project | Production branch |
| --- | --- | --- |
| Mentorship | e.g. `kavrvix` | `main` |
| Experts | e.g. `kavrvix-experts` | `experts` |

For each: Vercel → **Add New → Project** → import your fork → Framework preset **Other** → leave Build Command and Output Directory empty → **Deploy**.
Then **Settings → Git → Production Branch** → set `main` or `experts` and redeploy.

### 3. Connect your domain
Vercel project → **Settings → Domains** → add e.g. `kavrvix.com` (mentorship) and `experts.kavrvix.com` (experts) and follow the DNS steps.

### 4. Turn on full SEO for that domain (one command)
On the branch for that site, run:

```bash
node scripts/seo.mjs https://kavrvix.com          # on main
node scripts/seo.mjs https://experts.kavrvix.com  # on experts
```

Commit and push. This adds the canonical URL, full-URL share images (so WhatsApp, Facebook and X show the preview card), `sitemap.xml` and the sitemap line in `robots.txt`.
No Node? Send the domain to whoever maintains the site; it's a 10-second job.

### 5. Test the form
Send one test entry. Formspree emails you a confirmation link on the very first submission; click it, then submissions arrive normally.

### 6. Tell Google
Add the domain in [Google Search Console](https://search.google.com/search-console), then submit `https://yourdomain/sitemap.xml`.

## Ad tracking (Meta + TikTok pixels)

Off by default. In `index.html`, search for `TRACKING` and paste your IDs:

```js
var TRACKING = { metaPixelId: "123456789012345", tiktokPixelId: "C1AB2CD3EF..." };
```

Events sent automatically: `PageView`, `Lead` (form sent), `Contact` (WhatsApp/socials tap). Use `Lead` as the conversion event for your ad campaigns.

## What's included

| Path | What it is |
| --- | --- |
| `index.html` | The whole site (HTML, CSS, JS). anime.js from cdnjs, Archivo font from Google Fonts. |
| `proof/` | Student sales screenshots and video for the "Student sales" wall. Add more in the `PROOF` list in `index.html`. |
| `brand/` | Logo files (mark, lockups), favicons and app icons. |
| `og-image.png` | 1200×630 link preview image. |
| `privacy.html`, `terms.html` | Privacy Policy and Terms (templates, have them reviewed for your countries). Required for running Meta/TikTok ads with a pixel. |
| `404.html` | Branded not-found page. |
| `vercel.json` | Clean URLs (`/privacy`), caching for images, security headers. |
| `robots.txt`, `sitemap.xml` | Search engine files (`sitemap.xml` appears after step 4). |
| `site.webmanifest` | App name and icons for "Add to Home Screen". |
| `scripts/seo.mjs`, `site.config.json` | SEO generator and its settings (not deployed, see `.vercelignore`). |

SEO already in the page: title, meta description, Open Graph + Twitter cards, theme color, favicons, structured data (Organization, WebSite, Service, FAQPage) generated from the page content.

## Editing

- **Social links**: WhatsApp +1 (302) 563-7966, Instagram @Kavrix00_, TikTok @kavrix03, Facebook Kavrix00, Telegram @kavrix. Search `index.html` for a handle to change it, and update `socials` in `site.config.json`.
- **Form endpoint**: `FORM_ENDPOINT` in the script (Formspree `xrppeblq`).
- **Descriptions** for Google/link previews: the `description` and `og:` tags at the top of `index.html`, and `site.config.json`.

## Brand

- White `#FFFFFF` · Soft panel `#F3F5EF` · Line `#E2E6DC` · Ink `#14171B` · Volt `#CFF462` (lime as text on white: `#4A7300`)
- Type: Archivo, wide (wdth 125) for headlines, regular for body.
- The mark: a K whose upper arm is a sales chart breaking upward.
