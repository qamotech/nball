# 🏀 Ne'ala Hoops #14

A basketball **training + education** app built for Ne'ala, 11 — a beginner learning the game with her dad as coach. Everything is built around her jersey number: the **14 for 14** driveway session, 14 shots to chase, #14 in the header on every screen.

**Live:** https://qamotech.github.io/nball/

## What's inside
- **Home** — today's plan from an editable weekly plan (tap any day to change it), editable weekly sessions/minutes goals with a progress bar, Drill of the Day, Make It Hers accent + mascot picker (defaults: orange, #14), Turkey Tip-Off countdown (Nov 21, 2026) with a First Game Ready packing checklist, streak, quick stats
- **Train** — 24 drills (Levels 1–3) by skill/level with form cues, ⭐ favorites + filter, drill search, featured **14 for 14** driveway session, practice timer (presets + custom, gentle beep), Dribble Beat metronome, and Challenge Modes: *Around the Driveway* (5 spots) and *Beat the Clock* (makes in 2 minutes)
- **Log** — practice sessions with makes/attempts, rebounds, assists, minutes and notes; earn-a-badge celebrations when a new badge unlocks; plus a Game Log for real games with auto-summed season totals
- **Learn** — Basketball IQ lessons (including "What Your First Game Feels Like"), school-through-basketball (FG% & averages math, Box Score Math, vocabulary flashcards, a story with comprehension questions), **Legends: Cheryl & Reggie Miller** plus Basketball Beginnings (Naismith, peach baskets, how the WNBA started in 1997), 5 quizzes with best scores saved, lesson/quiz search, and a 10-question Quiz Championship with a printable certificate at 8+
- **Progress** — charts, per-practice averages, a practice calendar, and 12 badges earned from real logged data
- **Dad's Corner** (in Progress) — backup export/import (with a preview before anything is replaced), CSV practice-history export, Share the Week copyable summary, Data Safety (storage used + backup-age reminder), gear checklist, a private Coach's Notebook, and a printable weekly summary
- **Comfort** — text-size toggle (Normal/Big), Calm Mode reduced-animation toggle, 44px+ tap targets, aria labels, and visible focus — all saved on-device

## How to open it
- **Easiest:** open the live link above on any phone or computer browser.
- **From a file:** open `index.html` in any modern browser — no server, no install, no build step. (The practice timer beep and offline install work best from the live link.)

## How to install it (like an app)
- **Android (Chrome):** open the live link → tap the ⋮ menu → **Add to Home screen** / **Install app**. It then opens full-screen and works offline.
- **iPhone/iPad (Safari):** open the live link → tap **Share** → **Add to Home Screen**.

## Privacy — local only, always
- **No accounts, no sign-ups, no posting, no tracking, no ads.**
- Every practice, lesson, quiz score, and coach note is saved **only on the device** (browser localStorage, key `nealaHoops_v1`). Nothing is sent anywhere.
- The only way data moves is if Dad deliberately exports a backup file from Dad's Corner — and importing one always shows a preview first.
- Clearing the browser's site data erases the app's data, so export a backup now and then.

## Tech
- One self-contained `index.html` — HTML/CSS/JS, **zero dependencies**, dark mode + high contrast, phone-first
- `manifest.json` + `sw.js` + `icon.svg` sit next to it in this repo to make the live site installable and offline-capable; the single file still works fine on its own
- Automated checks: `test_neala.py` and `test_millers.py` (Playwright) click through the whole app and require zero page errors
- Built in 32 upgrade-loop cycles, Oct 25–26, 2026 — see `PLAN.md` for the full roadmap

Made with 💛 by Dad.
