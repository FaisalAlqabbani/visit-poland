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
Built for people glancing at a phone while standing at the booth: **minimal text, visuals first.**

Hero → scrolling name marquee (reacts to scroll speed) → 4 count-up stats → 10 full-screen photo moments (Kraków, Wieliczka, Warsaw, Gdańsk, Malbork, Wrocław, Tatras, Białowieża, Toruń, Masuria). Each shows only: name, a 2-word tag, one big count-up number + label, and a one-line fun fact → swipeable "Made in Poland" cards (one line each) → tap-to-hear Polish phrases (phone's speech voice) → outro with share button.

Place data lives in the `PLACES` array in `index.html` (`where`, `num`/`pre`/`suf`/`plain`, `label`, `em`, `fact`). Keep facts to one short line.

## Changelog
- 2026-10-14 — Initial build: page, images, credits, QR code, GitHub Pages deploy.
- 2026-10-14 — Fix fact-card text invisible in dark mode; guard against horizontal overflow on phones.
- 2026-10-14 — Sharper images: full-res sources, phone portrait crops + desktop WebP versions; gentler zoom on parallax. New photos for Wrocław (Cathedral Island at dusk), Malbork (river panorama), Morskie Oko (morning reflection).
- 2026-10-14 — Minimal-text redesign: removed paragraphs/chips; each place is now a full-screen photo with a big animated number and a one-line fact. Added scroll-reactive marquee, outline section numbers, 2-column phrase buttons. Replaced unverifiable stats (UNESCO count, population) with dated facts.
