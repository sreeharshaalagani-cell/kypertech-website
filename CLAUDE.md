# Kyper Tech — Marketing Homepage

Context for working on this project with Claude Code.

## What this is
A single-file, static marketing homepage for **Kyper Tech**, a Data & AI
**services** company. Everything lives in `index.html` — no build step, no
framework, no package install. Open it in a browser and it runs.

## Positioning (the message the site must protect)
- Kyper Tech is a **Data & AI services company** — NOT a product/CDP vendor.
- **Specialization:** building **Composable Customer Data Platforms (CDPs)**
  for **Retail & CPG** brands, on the client's own data foundation.
- **Engagement model:** four phases — **Consult → Strategize → Build → Activate**.
- The **System of Engagement** is driven by BOTH agentic AI AND partnerships/
  integration with off-the-shelf CDP platforms. Do not frame Kyper Tech as
  anti-packaged-CDP; the composable stance applies to the *data foundation*,
  while best-of-breed (including packaged CDPs) is used for *activation*.
- Cross-cutting capabilities that bracket everything: **Consulting & Strategy**
  (ideate + architect) and **Data Governance & Compliance** (trust throughout).
- Always write the company name as **"Kyper Tech"**, never "Kyper" alone.
- Use **"Customer 360"** only to mean the unified customer *view* (a capability),
  never as the platform name. The platform is the "Composable Customer Data Platform".

## Page structure (section ids)
`#about` → `#how` (How We Work) → `#platform` (abstracted 3-layer architecture)
→ `#capabilities` (Consulting & Strategy + Governance/Compliance framing cards,
then System of Insight / System of Engagement, then a quiet supporting-capabilities
strip) → `#accelerators` → `#resources` → `#contact` (CTA) → footer.

## Design system (defined as CSS variables in `:root` in index.html)
- **Colors:** `--ink` #0d0f12 (dark sections), `--paper` #f5f2ea (light sections).
  Brand accent is a two-tone VIOLET system — **accent-deep #5654CE (deep) /
  accent #9B9BFF (bright) — Neon Periwinkle**:
  - `--accent-deep` #5654CE — the deep brand violet. Used for elements where text
    sits ON the color (buttons, CTA band) paired with light text, and for kickers/
    borders on light backgrounds.
  - `--accent` #9B9BFF — a brighter violet (same hue, lifted). Used for text-level
    accents on DARK backgrounds (headline highlight, eyebrows, links, logo icon,
    hover states) because #5654CE is too dark to read on near-black.
  - `--warm` #f0a48c — peach tint, used only to distinguish the "Foundational"
    layer in the platform diagram. (Open style choice: could be swapped to a violet
    tint to keep the section fully monochrome-brand.)
  - **Contrast rule to preserve:** deep purple background → light text; bright
    violet → text on dark only. Don't put dark text on either purple.
- **Fonts (Google Fonts CDN):** `Bricolage Grotesque` (display/headings),
  `Hanken Grotesk` (body).
- **Logo:** inline SVG `<symbol id="kyperLogo">` defined once after `<body>`,
  reused via `<use>` in nav and footer. Icon = bright violet (#8273c9), wordmark =
  off-white (#f5f2ea). This version is built for DARK backgrounds. Original brand
  logo (purple) is in `assets/logo-original.svg` if a light-bg variant is needed.
- **Motion:** CSS transitions + a small IntersectionObserver in the inline `<script>`
  that adds `.in` to `.reveal` elements on scroll. Plus a basic mobile menu toggle.

## Conventions
- Keep it a single self-contained file unless there's a strong reason to split.
- Change colors via the `:root` variables, not scattered literals.
- No localStorage/sessionStorage, no external JS frameworks.
- Contact email: `info@kypertech.com` (used in CTA button + footer).

## Open decisions / TODO (confirm before going fully public)
1. **Accelerator names** (`#accelerators`: Integration Framework, Data Quality
   Framework, Infra Abstraction, Workflow Blueprint, Canned Reports, plus the
   "best practices" chips) came from a **MathCo reference deck**, not confirmed as
   Kyper Tech's own IP. Confirm or replace. (HTML comment flags this in the file.)
2. **"CDP Platform Partnerships"** wording (`#capabilities`, System of Engagement):
   says "partner with." Only keep "Partnerships" if Kyper Tech holds formal vendor
   partnerships/certifications; otherwise change to "CDP Platform Integration".
3. **Proof:** no client logos, certifications, metrics, or testimonials yet. The
   hero stat strip uses qualitative tiles instead of numbers by design — swap in
   real proof when available (highest-value spot).
4. **Partner/stack chips** were removed (placeholder). Add back a real list of
   warehouses/CDP platforms worked with, if desired.
5. **Logo light-background variant** not yet made (current one is dark-bg only).

## Deploy
- Local preview: open `index.html` in a browser (or `python3 -m http.server`).
- GitHub Pages: push repo, Settings → Pages → Deploy from branch → main / root.
  `index.html` at the root is served automatically. See README.md.
