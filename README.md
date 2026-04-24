# Delivery Empire — Web

Marketing + legal site for the **Delivery Empire** mobile game (iOS / Android).

Static HTML/CSS, no build step. Hosted on GitHub Pages.

## Pages

- `index.html` — landing page
- `privacy.html` — Privacy Policy (required for App Store & Google Play)
- `terms.html` — Terms of Service
- `support.html` — Support / contact page

## Local preview

Just open `index.html` in a browser, or run a tiny local server:

```bash
cd web-usinggithub
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new repository on GitHub, e.g. `delivery-empire-web`.
2. From this folder, initialize and push:

   ```bash
   git init
   git add .
   git commit -m "Initial site: landing, privacy, terms, support"
   git branch -M main
   git remote add origin https://github.com/<your-username>/delivery-empire-web.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main**, folder: **/ (root)**
   - Save.

4. After ~1 minute, the site is live at:
   `https://<your-username>.github.io/delivery-empire-web/`

   Your URLs to submit to the App Store / Google Play:
   - Privacy Policy URL: `https://<your-username>.github.io/delivery-empire-web/privacy.html`
   - Support URL: `https://<your-username>.github.io/delivery-empire-web/support.html`

## Custom domain (optional)

If you own e.g. `deliveryempire.app`:

1. Add a `CNAME` file to this folder containing just the domain:
   ```
   deliveryempire.app
   ```
2. At your DNS provider, point the domain to GitHub Pages (CNAME to
   `<your-username>.github.io` for apex use A records per GitHub docs).
3. In GitHub **Settings → Pages**, set the custom domain and enable
   "Enforce HTTPS".

## Things to review before publishing

- Contact email: currently `ertansoftwaresolutions@gmail.com` in `privacy.html`,
  `terms.html`, `support.html`. Change if you'd prefer a different address.
- Company name: currently `Ertan Apps` in the footer and Terms.
  Change if you operate under a different legal name.
- "Last updated" date in `privacy.html` and `terms.html` is set to
  2026-04-24. Bump it whenever you edit those pages.
