# Kyper Tech — Homepage

Static marketing homepage for Kyper Tech, a Data & AI services company
specializing in **Composable Customer Data Platforms for Consumer Businesses**,
activated with agentic AI.

Single self-contained file — no build step, no dependencies to install.

## Files
```
kyper-tech-site/
├── index.html               # the entire site (HTML + CSS + JS + inline SVG logo)
├── CLAUDE.md                # project context for Claude Code (positioning, design system, TODOs)
├── README.md                # this file
└── assets/
    └── logo-original.svg    # original brand logo (purple) — for reference / light-bg variants
```

## Preview locally
Open `index.html` directly in a browser, or serve it:
```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages
```bash
git init
git add .
git commit -m "Kyper Tech homepage"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo>.git
git push -u origin main
```
Then in the repo: **Settings → Pages → Source: Deploy from a branch →
Branch: `main` / `/ (root)`**. The site goes live at
`https://<your-username>.github.io/<repo>/`. For your own domain, set a custom
domain on the same Pages screen.

## Editing
- Colors and fonts are defined as CSS variables in `:root` near the top of
  `index.html` — change them there, not in individual rules.
- See `CLAUDE.md` for the design system, the positioning the copy must protect,
  and the list of open decisions to confirm before launch.

## Tech
Vanilla HTML/CSS/JS. Google Fonts (Bricolage Grotesque, Hanken Grotesk) loaded
via CDN. Scroll reveals via IntersectionObserver. Logo is an inline SVG.
