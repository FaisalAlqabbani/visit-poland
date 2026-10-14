# Visit Poland — HTU International Week booth

Mobile-first, scroll-animated page about the best places to visit in Poland, opened from a QR code at the Poland booth.

- **Live:** https://faisalalqabbani.github.io/visit-poland/
- **QR code:** `qr/visit-poland-qr.png` (print) and `qr/visit-poland-qr.svg` (vector)

## Stack
Single static `index.html` — no build step, so it loads fast on phones over busy event Wi-Fi.
- GSAP 3 + ScrollTrigger (cdnjs) for scroll animations; page still works fully if the CDN fails or the visitor prefers reduced motion.
- Fonts: Fraunces (display) + Manrope (body) from Google Fonts.
- Photos from Wikimedia Commons, resized to ≤1100px (~100–190 KB each) in `img/`. Credits listed in the page footer and `img/credits.json`.
- Hosted on GitHub Pages from the `main` branch root.

## Content
Hero → intro stats → 10 places (Kraków, Wieliczka, Warsaw, Gdańsk, Malbork, Wrocław, Tatras, Białowieża, Toruń, Masuria), each with *why visit* + a *Did you know?* historical fact → swipeable "Made in Poland" cards → tap-to-hear Polish phrases (uses the phone's speech voice) → outro with share button.

Place data lives in the `PLACES` array in `index.html` — edit text there.

## Changelog
- 2026-10-14 — Initial build: page, images, credits, QR code, GitHub Pages deploy.
