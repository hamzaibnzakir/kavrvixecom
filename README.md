# Kavrvix Ecom

Landing page for the Kavrvix ecommerce mentorship. One static page — no build step.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole site (HTML, CSS, JS). Uses anime.js from cdnjs and Archivo / JetBrains Mono from Google Fonts. |
| `proof/` | Student sales screenshots + the student video shown in the "Student sales" wall. |
| `brand/` | Logo files: mark (SVG/PNG), full lockups for dark and light backgrounds, favicon. |

## Things to update

**Social links** — in `index.html`, search for `SOCIALS:`. Replace each `href="#"` with the real profile URL and delete the `<span class="soon">Soon</span>` next to it.

**Sales proof** — drop new screenshots into `proof/`, then add a line to the `PROOF` list near the top of the `<script>` in `index.html`:

```js
{ src: "proof/sale-17.jpg", caption: "$2,400 first week" },
```

Videos use `{ video: "proof/file.mp4", poster: "proof/poster.jpg", caption: "..." }`.

**Application form** — submissions go to Formspree (`https://formspree.io/f/xrppeblq`). Change `FORM_ENDPOINT` in the script to switch it. The first real submission may ask you to confirm the form in your Formspree inbox.

## Deploy

Import the repo into Vercel (Framework: *Other*, no build command, output = root) or enable GitHub Pages on the `main` branch. Any static host works.

## Brand

- Graphite `#14171B` · Panel `#1B1F25` · Line `#2B313A` · Chalk `#ECEEE6` · Steel `#8D949D` · Volt `#CFF462`
- Type: Archivo at wide width (wdth 125) for headlines, Archivo regular for body, JetBrains Mono for dashboard numbers.
- The mark: a K whose upper arm is a sales chart breaking upward.
