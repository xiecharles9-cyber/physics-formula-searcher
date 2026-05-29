# Connecting a custom domain + enabling AdSense

Your site is live at: https://xiecharles9-cyber.github.io/physics-formula-searcher/

## 1. Buy a domain
Get a domain from any registrar (Namecheap, Cloudflare, Porkbun, Google Domains, etc.).
Example: `physicsformulas.com`. Cost is usually ~$10–15/year.

## 2. Point the domain at GitHub Pages

### Option A — apex domain (e.g. `physicsformulas.com`)
At your registrar, create four **A records** pointing to GitHub's IPs:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```
(Optional but recommended: also add four AAAA records — see GitHub's docs.)

### Option B — www subdomain (e.g. `www.physicsformulas.com`)
Create one **CNAME record**:
```
www  ->  xiecharles9-cyber.github.io
```

## 3. Tell GitHub about the domain
Either:
- In the repo: **Settings → Pages → Custom domain**, enter your domain, Save. GitHub
  will create a `CNAME` file in the repo automatically; or
- Add a file named `CNAME` (no extension) to this repo whose only contents are your
  domain, e.g. `physicsformulas.com`, then push.

Wait for DNS to propagate (minutes to a few hours), then tick **Enforce HTTPS** in
Settings → Pages.

## 4. Apply to Google AdSense
1. Once the custom domain is live, sign up at https://adsense.google.com with that domain.
2. AdSense will review the site (this can take days to weeks). They expect real content
   and a Privacy Policy — both are already included (`privacy.html`).
3. After approval, create an **ad unit** to get a slot ID.
4. Open `index.html`, find the AdSense section near the bottom of the `<script>`, and set:
   ```js
   const ADSENSE_PUB_ID  = "ca-pub-XXXXXXXXXXXXXXXX"; // your publisher ID
   const ADSENSE_SLOT_ID = "XXXXXXXXXX";              // your ad-unit slot ID
   ```
5. Commit and push. Ads will then appear in the two ad slots (above and below the formula grid).

## Notes
- AdSense generally will **not** approve a `*.github.io` subdomain — the custom domain
  in steps 1–3 is required.
- Update the contact email placeholder in `privacy.html`.
