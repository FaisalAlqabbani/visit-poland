# Visit Poland — HTU International Week booth

Mobile-first, scroll-animated page about the best places to visit in Poland, opened from a QR code at the Poland booth.

- **Live:** https://faisalalqabbani.github.io/visit-poland/
- **QR code:** `qr/visit-poland-qr.png` (print) and `qr/visit-poland-qr.svg` (vector)

## Stack
Single static `index.html` — no build step, so it loads fast on phones over busy event Wi-Fi.
- GSAP 3 + ScrollTrigger (cdnjs) for scroll animations; page still works fully if the CDN fails or the visitor prefers reduced motion.
- Fonts: Fraunces (display) + Manrope (body) from Google Fonts.
- Photos from Wikimedia Commons (3–4K originals), in `img/` as two WebP versions each: `*-m.webp` = portrait phone crop (~1230×2200) and `*-d.webp` = landscape desktop (2400px wide). A `<picture>` tag picks one by screen shape. `img/og.jpg` = link-preview image. Credits in the page footer and `img/credits.json`.
- Hosted on GitHub Pages from the `main` branch root.

## Content
Hero → intro stats → 10 places (Kraków, Wieliczka, Warsaw, Gdańsk, Malbork, Wrocław, Tatras, Białowieża, Toruń, Masuria), each with *why visit* + a *Did you know?* historical fact → swipeable "Made in Poland" cards → tap-to-hear Polish phrases (uses the phone's speech voice) → outro with share button.

Place data lives in the `PLACES` array in `index.html` — edit text there.

## Changelog
- 2026-10-14 — Initial build: page, images, credits, QR code, GitHub Pages deploy.
- 2026-10-14 — Fix fact-card text invisible in dark mode; guard against horizontal overflow on phones.
- 2026-10-14 — Sharper images: full-res sources, phone portrait crops + desktop WebP versions; gentler zoom on parallax. New photos for Wrocław (Cathedral Island at dusk), Malbork (river panorama), Morskie Oko (morning reflection).
