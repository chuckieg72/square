
[README.md](https://github.com/user-attachments/files/22185664/README.md)
# Athena Payment Portal — Square (GitHub Pages)

A minimal, mobile‑friendly landing page that links directly to your **Square Checkout**. Designed for fast deploys on **GitHub Pages**.

---

## What’s in this repo
- `index.html` – the landing page with the **Pay with Square** button.
- `CNAME` *(optional)* – add this file to use a **custom domain** (e.g., `todaysmarketingsolutionsllc.org`).

---

## Quick start (≈60 seconds)
1. **Create a new repository** on GitHub (public or private).
2. **Add** `index.html` (paste or upload) and **Commit**.
3. Go to **Settings → Pages**.
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` and **Folder:** `/ (root)`
   - Click **Save**.
4. Wait a minute and visit your site at:  
   `https://<your-username>.github.io/<your-repo>/`

> ✅ Make sure the file is named exactly **`index.html`** (lowercase).

---

## Update your Square link
1. Open `index.html` and find the button link:
   ```html
   <a class="btn" href="https://square.link/u/pkZSuTqf" target="_blank" rel="noopener">Pay with Square</a>
   ```
2. Replace the `href` with **your** Square payment link if needed.
3. Commit the change. Done.

---

## Optional: custom domain (e.g., todaysmarketingsolutionsllc.org)
1. In the **repo root**, create a file named **`CNAME`** (no extension) with just your domain:
   ```
   todaysmarketingsolutionsllc.org
   ```
2. In your DNS (IONOS or your registrar), set:
   - **A (apex)** records to GitHub Pages IPs (add all four):
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - **CNAME** for `www` → `<your-username>.github.io`
3. Back in **Settings → Pages**, confirm the **Custom domain** is set to your domain and enable **Enforce HTTPS**.
4. DNS/SSL can take a few minutes to issue a certificate.

---

## Verify it’s live
- Visit your GitHub Pages URL (or your custom domain).
- Click **Pay with Square** and confirm it opens the Square checkout page.
- If you see a 404 or the old page, try a **hard refresh** (Ctrl/Cmd+Shift+R).

---

## Troubleshooting
- **404 / Not found:** Ensure **Pages** is enabled for the **main** branch and the **root** folder. Confirm the file is **index.html** (lowercase).
- **HTTPS not available:** Wait for SSL to provision, then toggle **Enforce HTTPS** in **Settings → Pages**.
- **Custom domain not working:** Double‑check DNS. Apex uses the **four A records** above; `www` uses **CNAME** to `<your-username>.github.io`.
- **Button doesn’t open checkout:** Verify your `href` is a valid **https://square.link/...** URL.

---

## Next steps (optional)
- Add a simple **thank‑you/return page** if you want a branded return path.
- Later we can wire payment status to a Google Sheet via a webhook/Zapier when you’re ready.

---

**Support:** todaysmarketingsollutions1@gmail.com
