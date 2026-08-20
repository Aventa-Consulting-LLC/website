# aventaconsulting.com

Public website for **Aventa Consulting LLC** — Salesforce consulting for growing teams.

## How this site works

- Static site, single `index.html` (all CSS inline). No build step, no dependencies.
- Hosted free on **GitHub Pages**, deployed automatically from the `main` branch.
- Custom domain via the `CNAME` file + DNS records at Porkbun (4 A records on the apex, `www` CNAME to `aventa-consulting-llc.github.io`).
- Brand assets (Summit logo, favicons, lockups) live in `/assets`.
- Contact form posts to **Formspree** (free tier). The form `action` in `index.html` must contain the real Formspree form ID.

## Making changes

Edit `index.html`, commit, push to `main`. Live in ~1 minute.

## One-time setup checklist

- [ ] Repo Settings → Pages → deploy from `main` branch, root folder
- [ ] Repo Settings → Pages → Custom domain: `aventaconsulting.com` → Enforce HTTPS
- [ ] Create a free Formspree form pointing at hello@aventaconsulting.com and replace `YOUR_FORM_ID` in `index.html`
- [ ] Replace the headshot placeholder in the About section
- [ ] Update Krysten's certifications list in the About section

© Aventa Consulting LLC
