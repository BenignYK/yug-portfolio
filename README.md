# Yug Khambholja — Portfolio

Personal digital portfolio for Yug Hiteshkumar Khambholja, B.Tech ECE student at PDEU.

## 🚀 Live Site

Deployed via GitHub Pages: `https://BenignYK.github.io/yug-portfolio/`

---

## 🗂 Structure

```
yug-portfolio/
├── index.html         # Main HTML
├── css/
│   └── style.css      # All styles + dark/light theme
├── js/
│   └── main.js        # Interactivity: cursor, theme, animations
└── README.md
```

---

## 🌐 Deploy to GitHub Pages

### Option 1 — New Repo (Recommended)

1. Create a new repository on GitHub: `yug-portfolio`
2. Clone and push:
```bash
git init
git add .
git commit -m "Initial portfolio commit"
git branch -M main
git remote add origin https://github.com/<your-username>/yug-portfolio.git
git push -u origin main
```
3. Go to **Settings → Pages** → Source: **Deploy from branch** → Branch: `main` → Folder: `/ (root)`
4. Wait ~60 seconds. Your site is live at `https://<your-username>.github.io/yug-portfolio/`

### Option 2 — Existing Repo with GitHub Actions

Create `.github/workflows/deploy.yml`:
```yaml
name: Deploy to Pages
on:
  push:
    branches: [main]
jobs:
  deploy:
    runs-on: ubuntu-latest
    permissions:
      contents: read
      pages: write
      id-token: write
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    steps:
      - uses: actions/checkout@v4
      - uses: actions/configure-pages@v5
      - uses: actions/upload-pages-artifact@v3
        with:
          path: '.'
      - id: deployment
        uses: actions/deploy-pages@v4
```

---

## ✨ Features

- **Dark / Light Theme** with localStorage persistence
- **Custom cursor** with magnetic hover effect
- **Scroll reveal** animations with staggered entrances
- **Fully responsive** (mobile, tablet, desktop)
- **Grid + orb hero** with noise texture overlay
- **No frameworks** — pure HTML/CSS/JS, zero dependencies, instant load

---

## 🎨 Design Tokens

Edit `css/style.css` `:root` and `[data-theme]` blocks to customize colors, fonts, and spacing.

---

## 📝 Updating Content

All content lives in `index.html`. Edit the relevant `<section>` blocks to update:
- Education, Experience, Projects, Skills, Achievements, Certificates, Contact

---

Built with ❤ by Yug Khambholja · Gandhinagar, Gujarat
