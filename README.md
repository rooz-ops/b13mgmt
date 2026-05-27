# B13 Management — Marketing Site

Static marketing website for [b13mgmt.com](https://b13mgmt.com).  
Sister site to [b13solutions.com](https://b13solutions.com).

## Project structure

```
b13mgmt/
├── index.html          # Entire site — CSS + JS all inline
├── b13mgmt-logo.png    # Logo asset
└── README.md           # This file
```

No build step. No framework. No npm. Just HTML.

---

## Preview locally

Open `index.html` directly in any browser:

```bash
# macOS / Linux
open index.html

# Windows
start index.html
```

Or use VS Code's Live Server extension, or Python's built-in server:

```bash
python -m http.server 8080
# then visit http://localhost:8080
```

---

## Deploy to Vercel

### Option A — Vercel CLI (recommended)

```bash
npm i -g vercel     # install CLI once
vercel              # run from the b13mgmt/ directory
```

Follow the prompts. On subsequent deploys:

```bash
vercel --prod
```

### Option B — GitHub import

1. Push this folder to a GitHub repository.
2. Go to [vercel.com/new](https://vercel.com/new).
3. Import the repository.
4. Framework preset: **Other** (no framework).
5. Output directory: leave blank (serves from root).
6. Click **Deploy**.

### Custom domain

In the Vercel project → **Settings → Domains**, add `b13mgmt.com` and follow the DNS instructions.

---

## Contact form

The form uses `mailto:` — it opens the visitor's default email client with a pre-filled message to `rooz@b13mgmt.com`. No server required, no form-handling service needed.

If you later want server-side form handling (e.g. Resend, Formspree, or a Vercel serverless function), the form `id="contact-form"` is ready to wire up.

---

## Fonts

Loaded from Google Fonts (CDN, no self-hosting needed):

- **Instrument Serif** — headlines
- **Geist** (300–600) — body / UI
- **Geist Mono** (400–500) — labels / mono elements

---

_Built May 2026._
