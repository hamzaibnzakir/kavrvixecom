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

**Social links** — in `index.html`, search for `SOCIALS:`. Replace each `href="#"` with the real profile URL and delete the `<span class="soon">Soon</span>` next to it.

**Application form** — submissions go to Formspree (`https://formspree.io/f/xrppeblq`). Change `FORM_ENDPOINT` in the script to switch it. The first real submission may ask you to confirm the form in your Formspree inbox.

## Deploy

Import the repo into Vercel (Framework: *Other*, no build command, output = root) or enable GitHub Pages on the `main` branch. Any static host works.

## Brand

- Graphite `#14171B` · Panel `#1B1F25` · Line `#2B313A` · Chalk `#ECEEE6` · Steel `#8D949D` · Volt `#CFF462`
- Type: Archivo at wide width (wdth 125) for headlines, Archivo regular for body, JetBrains Mono for dashboard numbers.
- The mark: a K whose upper arm is a sales chart breaking upward.
