# Vita Bandet 2027 — public site

Public trip blog for a winter White Ribbon ski: Grövelsjön → Treriksröset, 10 Feb – 15 Apr 2027.

**Live:** [https://vitabandet.maak-t.com](https://vitabandet.maak-t.com)

Planning notes stay in a private repo. This repo is only what should be on the internet: summary pages plus the daily log.

Hugo (Blowfish + GPX maps) · GitHub Pages via Actions · GitHub Free (public repo).

## Phone: post a day

Clone **this** repo on the phone (Working Copy / GitHub). Do not clone the private planning repo.

1. Create a folder `content/posts/YYYY-MM-DD-day-N/` (example: `2027-02-10-day-01`).
2. Add `index.md` using the template below.
3. Optional: drop `day.gpx` and photos in the same folder; uncomment the map shortcode.
4. Commit and **push `main`**.
5. Wait a few minutes — the Action rebuilds the site.

### `index.md` template

```markdown
---
title: "Day 1 — Klacken"
date: 2027-02-10
draft: false
---

**Planned:** Klacken · 15 km  
**Actual:**  
**Weather:**

<!-- Uncomment when day.gpx is in this folder:
{{</* gpx-map file="day.gpx" */>}}
-->

What happened today.
```

No Hugo on the phone. Pushing `main` is enough.

## DNS

On `maak-t.com`:

| Record | Name | Target |
|--------|------|--------|
| CNAME | `vitabandet` | `philipsen.github.io` |

Then in this GitHub repo: **Settings → Pages → Custom domain** `vitabandet.maak-t.com` → enforce HTTPS.

GitHub Pages source must be **GitHub Actions** (not “Deploy from a branch”).

## Local preview

Needs Hugo extended ≥ 0.162:

```bash
hugo mod get
hugo server
```
