# VaultDrive — Biometric Encrypted SSD Website

[![Status](https://img.shields.io/badge/status-production--ready-00AED5)](https://facrypt.com)
[![Languages](https://img.shields.io/badge/i18n-EN%20%C2%B7%20JA%20%C2%B7%20DE-0085B2)]()
[![Single File](https://img.shields.io/badge/deploy-single--file%20HTML-03558E)]()

Official product website for **VaultDrive** — a 1TB biometric encrypted portable SSD from **DSCC 数安 / Facrypt**. Your face generates the AES-256 key. Your face erases it. No password. No stored key.

**Live slogan:** *Your Face. Your Key. Your Data.*

---

## 🚀 Quick Deploy

This is a **single-file** static site. Zero build step, zero dependencies at deploy time.

### Option 1: GitHub Pages (free, 2 minutes)

1. Push this repo to GitHub
2. Settings → Pages → Branch: `main` / `(root)` → Save
3. Visit `https://qianjianshui.github.io/SSD-website/`

### Option 2: Any static host

Drop `index.html` on Netlify, Vercel, Cloudflare Pages, or your own Nginx — done.

### Option 3: Custom domain (facrypt.com)

Add a `CNAME` file containing `facrypt.com`, then configure DNS:
```
A     @     185.199.108.153
A     @     185.199.109.153
A     @     185.199.110.153
A     @     185.199.111.153
CNAME www   qianjianshui.github.io
```

---

## 📦 What's Inside

**One HTML file. 6200+ lines. 14 sections. 3 languages.**

### Sections
| # | Section | Purpose |
|---|---------|---------|
| 1 | Navigation | Brand + 5 anchors + language switcher |
| 2 | Hero | Main headline + production-grade drive render |
| 3 | Social Proof | Security community endorsements |
| 4 | Problem | $4.88M breach cost framing |
| 5 | Solution | "Your face. Your key. Your data." |
| 6 | How It Works | 3-step cryptographic flow |
| 7 | Product Showcase | Top / Side / Internal views |
| 8 | Scenarios | 6 worst-case situations |
| 9 | Compare Table | vs BitLocker, vs password SSDs |
| 10 | Colors | 3 variants (Gray / Silver / Orange) |
| 11 | App Scenarios | 6-card bento grid, Samsung T7-style |
| 12 | Specs | 4 hero stats + 14-row detail table |
| 13 | Audience (Pro) | Lawyers / Journalists / Travelers / Healthcare |
| 14 | Everyday Privacy | First-person quotes — freelancers, families, students |
| 15 | FAQ | 8 questions with JSON-LD schema |
| 16 | Enterprise Teaser | FaceAuth cross-sell |
| 17 | Final CTA | Scarcity bar: 138 of 500 remaining |
| 18 | Footer | 5-column with legal, certs, languages |

### Internationalization
- **English** — direct, product-launch tone
- **日本語** — humble, trust-oriented, culturally adapted
- **Deutsch** — technically precise, DSGVO-focused

Auto-detects browser language, stores user preference in `localStorage`, updates `<title>` per language, 309 translation hooks wired.

### SEO Stack
- `FAQPage` JSON-LD schema (eligible for Google Featured Snippets)
- `Product` schema with pricing, availability
- `Organization` schema with DSCC company info
- `hreflang` tags for EN/JA/DE
- Open Graph + Twitter Card meta
- Semantic HTML throughout

---

## 🎨 Design System

- **Brand palette** extracted from actual DSCC logo:
  - `#00B5DB` bright cyan
  - `#00AED5` sky blue (primary)
  - `#0085B2` mid blue
  - `#03558E` navy
  - `#013F6E` deep indigo
- **Fonts**: Inter · Noto Sans JP · DM Mono · Lora (italic quotes)
- **Max width**: 1240px
- **Breakpoints**: desktop / 1024px tablet / 768px mobile / 480px small
- **Animation ease**: `cubic-bezier(.16,1,.3,1)`

---

## 🛠️ Tech Stack

- **HTML5** — semantic, accessible
- **CSS3** — custom properties, Grid, Flexbox, no framework
- **Vanilla JS** — IntersectionObserver, localStorage, zero dependencies
- **SVG** — all product renders and illustrations inline (no raster images)

No build pipeline. No npm. Open `index.html` in a browser — it works.

---

## 📝 Update Workflow

```bash
# After editing index.html
git add index.html
git commit -m "Update: [describe changes]"
git push
```

GitHub Pages redeploys automatically within ~30 seconds.

---

## 🏢 About DSCC

**DSCC 数安商用密码技术（广州）有限公司**
Guangzhou, China · Data security infrastructure for the post-password era.

- Product 1: **VaultDrive** — biometric encrypted portable SSD (consumer)
- Product 2: **FaceAuth** — passwordless enterprise identity platform (B2B)

Compliance: GDPR · CCPA · HIPAA-ready · FIPS 140-3 · 等保2.0 · 个人信息保护法

---

## 📄 License

© 2026 DSCC 数安商用密码技术（广州）有限公司. All rights reserved.

This repository contains proprietary product marketing materials. The code structure is provided for transparency but all brand assets, copywriting, and design are trademark of DSCC.
