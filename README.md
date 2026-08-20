# aventaconsulting.com

Public website for **Aventa Consulting LLC**. Salesforce consulting for growing teams.

## How this site works

- Static site, single `index.html` (all CSS inline). No build step, no dependencies.
- Hosted free on **GitHub Pages**, deployed automatically from the `main` branch.
- Custom domain via the `CNAME` file + DNS records at Porkbun (4 A records on the apex, `www` CNAME to `aventa-consulting-llc.github.io`).
- Brand follows **Aventa Consulting Brand Guidelines v1.0 (Aug 2026)**. Keep changes inside that system.
- Brand assets in `/assets`, all derived from Krysten's master logo files:
  - `logo-horizontal.png` / `-light`: mark left, wordmark right. Nav (desktop) and footer.
  - `logo-lockup.png` / `-light`: primary stacked lockup. 404 page, social card.
  - `logo-mark.png` / `-light`: A/mountain only. Compact nav (mobile), icons.
  - `logo-wordmark.png`: wordmark + rules only, for low-height spaces.
  - `favicon-16/32.png`, `apple-touch-icon.png`, `icon-512.png`: reverse mark on navy.
  - `og-image.png`: 1200x630 social card on Warm White.
  - `cert-*.png`: Salesforce credential badges shown in the About section. These are
    Salesforce trademarks. Display them as issued, never recolored or altered.
- Light and dark themes are driven entirely by the CSS custom properties in `:root`.
  Component rules reference roles (`--bg`, `--surface`, `--accent`) and never raw hex,
  so a palette change means editing only the two `:root` blocks. A small inline script
  in `<head>` sets `data-theme` before first paint, honoring a saved choice in
  `localStorage` and falling back to the visitor's system preference.
- Copy comes from Krysten's `Website_Copy.docx`. Treat that document as the source of
  truth for wording and re-sync from it rather than editing prose in place.
- Copy style: plain sentences and no em-dashes anywhere. Krysten doesn't use them, so
  the site shouldn't either.
- Colors (guidelines section 04): Aventa Navy `#173F58`, Aventa Sage `#8A9B78` (accent only),
  Ink `#26343D`, Mist `#F3F5F4`, Warm White `#F7F4EE`. Working tones derived for hover
  (`#0F2C40`), secondary text (`#5E6E77`), and dividers (`#E4E9EA`).
- Type (section 05): Montserrat SemiBold headlines / Medium subheads, Inter body. The logo
  lettering is artwork and must never be retyped.
- Logo rules (section 03-04): full lockup stays at least 180px wide; below that use the
  standalone mark. White reverse logo only on navy or another sufficiently dark field.
  No stretching, rotating, recoloring facets, or altering letter spacing.
- Contact form posts to **Formspree** (free tier). The form `action` in `index.html` must contain the real Formspree form ID.

## Making changes

Edit `index.html`, commit, push to `main`. Live in ~1 minute.

## One-time setup checklist

- [ ] Repo Settings → Pages → deploy from `main` branch, root folder
- [ ] Repo Settings → Pages → Custom domain: `aventaconsulting.com` → Enforce HTTPS
- [ ] Create a free Formspree form pointing at krysten@aventaconsulting.com and replace `YOUR_FORM_ID` in `index.html`
- [ ] Replace the headshot placeholder in the About section
- [ ] Update Krysten's certifications list in the About section

© Aventa Consulting LLC
