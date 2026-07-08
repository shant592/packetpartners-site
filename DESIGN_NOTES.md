# Packet Partners — Website Redesign Notes

## Files
- `index.html` — page structure/copy
- `styles.css` — all styling (design tokens at the top of the file)
- `script.js` — mobile nav toggle, footer year, contact form UX
- `assets/icon.svg` — your existing icon mark, reused as favicon and in the header/footer lockup

Drop all four into your GitHub Pages repo root (keep the `assets` folder alongside `index.html`). No build step, no dependencies beyond two Google Fonts links already in `index.html`.

## Design approach

**Signature element:** the wavy dotted line from your existing logo is the literal shape of a packet route, so I built the hero background around it directly — three of those waves stretched full-width behind the headline, with small dots animated along each path (pure SVG `animateMotion`, no JS, and it respects `prefers-reduced-motion`). It's the one animated moment on the page; everything else is static and calm so it doesn't compete.

**Type:** Space Grotesk for headlines (a technical, geometric grotesque that echoes the angular "A" in your wordmark) paired with Inter for body copy (readable at small sizes for SMB owners on a phone). IBM Plex Mono shows up only for a couple of small technical touches — the "$ ping packetpartners.tech" status readout in the hero — a wink at the "packet" name without leaning on cliché cyber/hacker visuals.

**Color:** used your palette as-is (Navy, Deep Navy, Primary Blue, Light Blue, Dark Gray, White, light background). Dark navy anchors the hero, why-us, and footer; white/light sections carry the services, industries, and pricing content so the page doesn't feel like one long dark slab.

**Icons:** every service icon is a custom two-color line-icon drawn to match the logo's dot-and-line vocabulary (small circles at line joints), instead of generic stock icon-pack cloud/gear/shield glyphs.

**Copy:** rewritten in plain, active language aimed at a dealership GM or hotel manager, not an IT director — short benefit statements rather than jargon, and the "Why Us" section tells the actual two-founder story from your brand summary (systems/cloud partner + networking partner) since that's your real credibility story as a new company.

## Easy edits for a non-developer
- All page text lives directly in `index.html` in plain sentences — search for the words you want to change.
- Pricing lives in the three `.plan-card` blocks under `<!-- PLANS -->`.
- Swap the Formspree placeholder: in `index.html` find `action="https://formspree.io/f/yourFormID"` and replace with your real Formspree endpoint (or point it at a `mailto:` handler).
- Colors/fonts are all defined once at the top of `styles.css` under `:root` — change a hex there and it updates everywhere.

## What I didn't do
Kept animation to the single hero flourish, avoided a generic cloud/shield icon set, and didn't touch your logo files — the SVG icon is used as-is.
