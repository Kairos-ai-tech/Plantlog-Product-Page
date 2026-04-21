# PlantLog — Product Page

Static marketing site for **PlantLog**, a plant-care companion app by [Kairos.ai](https://www.kairosaitech.com/). An editorial-style landing page plus legal pages (Terms of Use and Privacy Policy) in 7 locales.

Live app: PlantLog · iOS · `com.kairosai.plantlog`

---

## Structure

```
.
├── index.html              → /              (zh-Hant, default)
├── terms/index.html        → /terms
├── privacy/index.html      → /privacy
├── en/                     → /en/, /en/terms/, /en/privacy/
├── fr/                     → /fr/, /fr/terms/, /fr/privacy/
├── es/                     → /es/, /es/terms/, /es/privacy/
├── ja/                     → /ja/, /ja/terms/, /ja/privacy/
├── it/                     → /it/, /it/terms/, /it/privacy/
├── de/                     → /de/, /de/terms/, /de/privacy/
└── assets/
    ├── home.css            (shared landing-page styles)
    ├── legal.css           (shared terms/privacy styles)
    └── app-icon.png
```

Each locale folder contains three pages with the same three paths, served through a folder/`index.html` pattern so clean URLs work on any static host with no rewrites.

## Locales

| Code | Language | Active at |
|---|---|---|
| `zh-Hant` | 中文（繁體） | `/` (default) |
| `en` | English | `/en/` |
| `fr` | Français | `/fr/` |
| `es` | Español | `/es/` |
| `ja` | 日本語 | `/ja/` |
| `it` | Italiano | `/it/` |
| `de` | Deutsch | `/de/` |

The masthead on every page carries a language selector that navigates to the same page type (home ↔ home, terms ↔ terms, privacy ↔ privacy) across locales.

## Design

Editorial field-guide aesthetic — warm paper palette, deep moss green and terracotta accents, Fraunces (variable serif) paired with Noto Serif TC / Noto Serif JP and Instrument Sans, paper grain + radial vignette, staggered scroll reveal.

## Legal

- **Terms of Use** — End User License Agreement compliant with Apple App Store requirements (Apple as third-party beneficiary, scope of license, warranty, product claims, IP, legal compliance clauses, etc.).
- **Privacy Policy** — aligned with GDPR, CCPA, and Taiwan's Personal Data Protection Act. Discloses third-party processors (Firebase, Apple, Google, Plant.id), retention, user rights, and international transfers.

## Local preview

Pure static HTML + CSS, no build step. Serve from the project root:

```bash
python3 -m http.server 4173
# visit http://localhost:4173/
```

Or any static server (Vite, `npx serve`, `caddy file-server`, etc.).

## Deploy

Works out of the box on any static host that supports folder/`index.html` clean URLs:

- **Vercel** — drop the repo in, no config
- **Netlify** — same
- **Cloudflare Pages** — same
- **GitHub Pages** — same

No framework, no build, no runtime.

## Contact

- Email: [kairos.ai.tech@gmail.com](mailto:kairos.ai.tech@gmail.com)
- Web: [kairosaitech.com](https://www.kairosaitech.com/)

© 2026 Kairos.ai
