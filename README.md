# 🚀 Unlimited Codex + GPT-6 Astra Sales Landing Page

A high-converting, cyber-styled landing page and Cloudflare Edge Worker built to sell **Unlimited Codex + GPT-6 Astra** developer access ($15.00 USDT via Binance Pay).

---

## ✨ Features

- **⚡ Zero External Dependencies:** Pure HTML5, modern CSS3, and vanilla JavaScript. No React, Vue, or heavy node frameworks required.
- **🎨 Cyber Dark-Mode UI:** Clean dark aesthetic featuring deep charcoal backgrounds, neon cyan/blue glow accents, and responsive glassmorphism cards.
- **📱 100% Mobile & Desktop Responsive:** Pixel-perfect layout across smartphones, tablets, laptops, and ultra-wide monitors.
- **💳 Binance Pay Integration:** Dedicated instant checkout card featuring a 1-click copy button for Binance ID (`1268420191`) with interactive clipboard feedback.
- **💬 Direct Telegram Dispatch:** Pre-configured Telegram action links directing buyers to [`@mrmasterlk`](https://t.me/mrmasterlk) with a pre-filled confirmation message.
- **🖼️ Self-Contained Assets:** Inlined base64 branding and pure CSS cyberpunk promotional billboards—no external image hosting needed.
- **🌐 Cloudflare Edge Worker:** Ready-to-deploy `codexsale-worker.js` script with edge caching headers (`cache-control: public, max-age=3600`).

---

## 📁 Repository Structure

```text
├── index.html            # Standalone sales landing page
├── codexsale-worker.js   # Cloudflare Worker script serving the landing page
├── wrangler.toml         # Cloudflare Wrangler deployment configuration
├── .gitignore            # Git ignore file
└── README.md             # Project documentation
```

---

## 🚀 Deployment Options

### 1. Cloudflare Pages (Recommended for custom domains)
1. In the **Cloudflare Dashboard**, navigate to **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
2. Select this repository (`codex-astra-sales`).
3. Set build configuration:
   - **Framework preset:** `None`
   - **Build command:** *(leave empty)*
   - **Build output directory:** `/`
4. Click **Save and Deploy**.

### 2. Cloudflare Worker (Instant CLI Deployment)
Deploy directly to Cloudflare's global edge network using Wrangler:

```bash
# Login to Cloudflare
npx wrangler login

# Deploy edge worker
npx wrangler deploy
```

### 3. GitHub Pages
1. Go to your repository **Settings** → **Pages**.
2. Under **Build and deployment** > **Source**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/ (root)`.
4. Click **Save**. Your site will be live at `https://<username>.github.io/codex-astra-sales/`.

### 4. Any Static Web Host
Deploy `index.html` to any static hosting provider (Vercel, Netlify, Render, AWS S3, Apache, Nginx, Caddy).

---

## ⚙️ Configuration & Customization

### Updating the Binance Pay ID
In `index.html` and `codexsale-worker.js`, search and update the Binance ID:
```javascript
// Located inside the copy Binance ID script:
const payId = '1268420191';
```
And update the HTML text inside the checkout card:
```html
<div class="pay-id-number" id="binancePayId">1268420191</div>
```

### Updating the Telegram Contact
Update the Telegram username in the pre-filled payment dispatch buttons:
```html
<a href="https://t.me/mrmasterlk?text=Hello%20I%20have%20sent%2015%20USDT%20via%20Binance%20Pay%20(ID:%201268420191)" target="_blank">
```

---

## 📄 License
MIT License. Created for MRMASTERLK Digital Transformation & Innovation.

