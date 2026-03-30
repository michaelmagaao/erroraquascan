# 🐟 AquaScan – AI Fish Identifier

AquaScan uses TensorFlow.js + MobileNet to identify fish species directly in your browser — no server required. Point your camera at a fish or upload a photo, and instantly get species info, habitat, conservation status, and fun facts.

## ✨ Features

- 📷 **Live camera scanning** – real-time fish identification via webcam/phone camera
- 📂 **Image upload** – scan any fish photo from your device
- 🧠 **On-device AI** – TensorFlow.js + MobileNet runs entirely in the browser (no data sent to servers)
- 🐠 **Rich species info** – family, habitat, size, lifespan, conservation status, fun facts
- 📤 **Social sharing** – share to Twitter/X, Facebook, copy info, or download a shareable card
- 🌊 **Beautiful oceanic UI** – bioluminescent design with animated particles

## 🚀 Quick Start (Local)

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/aquascan.git
cd aquascan

# Install dependencies
npm install

# Start dev server
npm run dev
```

Open http://localhost:5173 in your browser.

## 📦 Deploy to Vercel

### Option 1: One-click Vercel Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/aquascan)

### Option 2: Vercel CLI

```bash
npm install -g vercel
vercel login
vercel --prod
```

### Option 3: GitHub Actions (CI/CD)

1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com) → Import Project → select your repo
3. Get your Vercel credentials:
   - `VERCEL_TOKEN`: Settings → Tokens → Create
   - `VERCEL_ORG_ID`: Settings → General → Team ID
   - `VERCEL_PROJECT_ID`: Project Settings → General → Project ID
4. Add these as **GitHub Secrets** (Repo → Settings → Secrets → Actions)
5. Every push to `main` auto-deploys to production!

## 🐙 Deploy to GitHub Pages

```bash
npm run build
# Copy contents of /dist to your gh-pages branch
```

Or use the `gh-pages` package:

```bash
npm install --save-dev gh-pages
# Add to package.json scripts:
# "deploy": "gh-pages -d dist"
npm run deploy
```

## 🧠 How the AI Works

AquaScan uses:
- **TensorFlow.js** – runs ML models in the browser via WebGL acceleration
- **MobileNet v2** – a lightweight image classification model pre-trained on ImageNet
- **Fish keyword matching** – maps MobileNet labels to a curated fish species database

The model identifies 10+ fish species: goldfish, shark, clownfish, tuna, salmon, trout, tilapia, carp, angelfish, bass, and more.

## 🗂 Project Structure

```
aquascan/
├── index.html          # Main app (all-in-one)
├── src/
│   └── fishData.js     # Fish species database
├── package.json
├── vite.config.js
├── vercel.json
└── .github/
    └── workflows/
        └── deploy.yml  # CI/CD pipeline
```

## 📱 Browser Support

- Chrome / Edge 88+ ✅
- Firefox 85+ ✅
- Safari 15+ ✅
- Mobile browsers (iOS Safari, Chrome Android) ✅

**Requires HTTPS for camera access** (Vercel provides this automatically).

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| TensorFlow.js | In-browser ML inference |
| MobileNet v2 | Image classification model |
| Vite | Build tool & dev server |
| Vanilla JS | App logic (no framework needed) |
| CSS3 | Animations & glassmorphism UI |

## 📄 License

MIT — free to use, modify, and distribute.
