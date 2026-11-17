# 🏀 Ne'ala Hoops #14

A basketball **training + education** app built for Ne'ala, 11 — a beginner learning the game with her dad as coach. Everything is built around her jersey number: the **14 for 14** driveway session, 14 shots to chase, #14 in the header on every screen.

**Live:** https://qamotech.github.io/nball/

## What's inside
- **Home** — today's plan from an editable weekly plan (tap any day to change it), editable weekly sessions/minutes goals with a progress bar, Drill of the Day, **Daily Affirmation** (14 rotating, one per day), **Coach's Pick** (the app notices your least-practiced skill and suggests a drill for it), Make It Hers accent + mascot picker (defaults: orange, #14) — now with **Kitty Blue 💙**, 🐱 Kitty and 🎀 Bow mascots, and one-tap **Kitty Bow Mode** (her favorite: blue + kitty + pink bows everywhere), Turkey Tip-Off countdown (Nov 21, 2026) with a First Game Ready packing checklist, streak, quick stats
- **Train** — 24 drills (Levels 1–3) by skill/level with form cues, ⭐ favorites + filter, drill search, **🎲 Surprise Drill** random picker (Levels 1–2), featured **14 for 14** driveway session, practice timer (presets + custom, gentle beep), Dribble Beat metronome, and Challenge Modes: *Around the Driveway* (5 spots) and *Beat the Clock* (makes in 2 minutes)
- **Pictures** — an original hand-drawn (SVG) kitty teammate in a blue #14 jersey illustrates all five tabs: shooting on Home, training on Train, a clipboard on Log, reading on Learn, and holding a trophy on Progress
- **Log** — practice sessions with makes/attempts, rebounds, assists, minutes and notes; earn-a-badge celebrations when a new badge unlocks; plus a Game Log for real games with auto-summed season totals
- **Learn** — Basketball IQ lessons (including "What Your First Game Feels Like"), school-through-basketball (FG% & averages math, Box Score Math, vocabulary flashcards, a story with comprehension questions), **Legends: Cheryl & Reggie Miller** plus Basketball Beginnings (Naismith, peach baskets, how the WNBA started in 1997), 5 quizzes with best scores saved, lesson/quiz search, and a 10-question Quiz Championship with a printable certificate at 8+
- **Progress** — charts, per-practice averages, a practice calendar, **🏆 Personal Records** (most makes, best shooting day, longest practice, best game points/rebounds/assists), and 12 badges earned from real logged data
- **Dad's Corner** (in Progress) — backup export/import (with a preview before anything is replaced), CSV practice-history export, Share the Week copyable summary, Data Safety (storage used + backup-age reminder), gear checklist, a private Coach's Notebook, and a printable weekly summary
- **Comfort** — BIG text all the time (no toggles — removed by request, along with Calm Mode), 44px+ tap targets, aria labels, and visible focus
- **Vibes update** — animated kitty artwork on all 5 tabs plus 3 new scenes (Game Log scoreboard, Badges medals, Story moonlight), 🎊 confetti celebrations for badges and perfect quizzes, **🏀 Swish Shot** tap-to-shoot timing game (best streak saved), 🎡 spinning Surprise Drill wheel, **🍩 Shooting Ring** donut on Progress, ⛶ Fullscreen button in the header, floating ⬆️⬇️ scroll-to-top/bottom buttons, and a 📲 Install card on Home
- **Installable PWA** — manifest with real PNG icons (192/512 + maskable + apple-touch), service worker v3 offline cache; install from the Home install card or the browser menu

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

## Places Update (2026-10-30, per Nathan)
- **What's New popup** on open (once per update, version `places-2026-10`; reopen anytime from the Places card) announcing the map with a confetti burst.
- **Places to Play & Train** card (Home): a hand-drawn SVG map of **14 real places within ~10 straight-line miles of the 21206 neighborhood** — Herring Run, Bocek, Clifton, Baker/Patterson, Coldstream, Weinberg Y, Cecil-Kirk, Greenmount, Carter, UA House, Marshall, Druid Hill, Parkville Y, Back River (Lady Lions) — with 2½/5/10-mile rings. The exact home address is **not** stored anywhere in the app; the map is centered on the neighborhood only.
- **4 effects:** animated golden route line + pulsing selected pin + distance count-up; 🎡 Spin-for-a-Place; 🧳 Places Passport stamps (`placesVisited`, MAP MASTER celebration at 14/14); popup party (bouncing ball + confetti).
- State additions (optional/defaulted): `placesVisited` [], `seenUpdate` null. SW cache v4. Tests: `test_places.py` 29 checks, all prior suites PASS.

## Dashboard + Games Update (2026-11-01, per Nathan)
- **Dashboard popup on EVERY visit** (`#dashModal`): greeting, animated hoop-shot scene, mascot buddy with tap-for-tips, count-up stats (streak, week practices, minutes, shooting %, badges, passport), weekly goal bars, next-badge + last-practice lines, What's New list, and Start Today / Play a Game / Places Map actions. Reopen anytime via "📊 See My Dashboard" on Home. The once-per-update What's New popup (now version `games-2026-11`) still fires first on update day, then hands off to the dashboard.
- **Shorter pages:** long lists now scroll inside their own boxes (`#drillList`, `#lessonList` 560px; `#placesList`, `#historyList`, `#gameList` 330px; `#coachNotesList` 300px) + a sticky **jump-chip bar** under the header that zips to any card on the current page.
- **8 additions:** dashboard count-up stats • animated hoop-shot scene • mascot buddy tips • 🎯 Hot Spot Challenge • 🧠 Memory Moves • ⚡ Quiz Blitz • 🎲 Daily Challenge Dice (stars) • 🏆 Trophy Shelf. New state (optional/defaulted): `hotspotBest`, `blitzBest`, `memoryBest`, `diceStars`, `diceDay`. SW cache v5. Tests: `test_games.py` 29 checks; all prior suites PASS.

## Menus + Cards + Caitlin Clark Update (2026-11-15, per Nathan)
- **Shorter pages via menus:** every view now opens with a grid of **menu cards**; tapping one shows only that part of the page (everything else tucks away). Home: Today / My Week / Picks & Style / Places & Game Day. Train: Games & Fun / Session & Tools / Drill Library. Log: Practice Log / Game Log. Learn: Lessons & Stories / Quizzes & Championship. Progress: My Stats / Charts & Shot Map / Trophies & Badges / Dad's Corner. Implemented with `data-panel` attributes + `.panel-off` show/hide (`openPanel()`, `MENU_DEFAULTS`); the jump-chip bar only lists cards in the open panel, and Dashboard actions (Play a Game / Places Map) open the right panel first.
- **Caitlin Clark (verified facts):** two Legends lessons — "Caitlin Clark — The Record Breaker" (3,951 NCAA points, 548 threes, 1,144 assists, 49-pt record game Feb 15 2024, #1 pick Indiana Fever 2024, Rookie of the Year, 19-assist WNBA record game) and "Caitlin's Superpower — Logo Threes & Super Passing". New **Caitlin Clark Quiz** (5 Qs, `quizBest.clark`), 2 Clark questions in Quiz Blitz, **Logo Three Ladder** drill (shooting L2), and a 13th badge **Logo Three Legend** (finish both Clark lessons). Quiz Championship grows 10 → 12 questions (2 from each of 6 quizzes; `champBest` cap 12).
- What's New popup version `menus-2026-11`; dashboard What's New list refreshed. SW cache v6. Save format unchanged (new fields optional/defaulted). Tests: new `test_menus.py` 31 checks; all 8 suites PASS, zero page errors.

## Games + Form Studio + 4 Features Update (2026-11-15, per Nathan)
- **3 new games** (Train > Games): ⏰ **Buzzer Beater** (tap SHOOT with the needle in the gold zone before the 5-second clock dies, 5 shots, `buzzerBest`) • 🙌 **Quick Hands** (tap falling balls before they hit the floor, 30s, `handsBest`) • 🎨 **Color Court** (match the color word; rounds 6–10 flip to ink-color Stroop, 10 rounds, `colorBest`).
- **🎬 Form Studio** — new Train menu panel with 4 animated SVG form visuals (SMIL): B.E.E.F. shooting form (rotating arm + arcing ball), Low Dribble Eyes Up (bouncing ball), Layup Steps 1-2-UP (sequenced footprints), Defensive Slide (sliding figure).
- **4 new features:** 👕 **Jersey Designer** (Home > Picks & Style — 8 colors × 4 trims × 3 styles, live SVG #14 preview, `state.jersey`) • 🗺️ **Skill Tree Adventure** (Train > Drill Library — all 25 drills as nodes, lit gold when the drill appears in a logged practice) • 🐣 **Buddy Growth** (Home > Today — mascot levels through 5 stages at 0/3/6/10/15 total practices) • 📣 **Cheer Me On!** (Home > Today — hype modal with confetti + cheer arpeggio + rotating hype lines, `cheerCount`).
- What's New popup version `studio-2026-11`; dashboard What's New refreshed. SW cache v7. Save format: new fields optional/defaulted (`buzzerBest`, `handsBest`, `colorBest`, `cheerCount`, `jersey`). Tests: new `test_studio.py` 35 checks; all 9 suites PASS, zero page errors.

## Update — Coach's Plan Editor (2026-11-17)
The v1.1 roadmap item (120-upgrades pick #54) is here: Nathan (Coach) can now edit the whole week in Home > My Week. Tap any day to set its focus (list pick or your own words), target minutes, up to 3 drills, and a coach note — saved in a new optional `weeklyPlanDetails` field; the classic `weeklyPlanOverrides` focus behavior is unchanged and old saves load untouched. Four one-tap presets build a full week: 🌟 Regular (back to the classic plan), 🏀 Game Week, 📚 School Week, 🎉 Fun Week. Day rows and the Home "Today's Plan" card show the day's minutes, drills and note. SW v8, update version planner-2026-11. New test suite test_planner.py (26 checks); all 10 suites pass with zero page errors.

## Update — Shot Log (2026-11-17)
120-upgrades pick #55: a per-drill shot log in Log > Practice. Pick any of the 25 drills, tap MAKE +1 / MISS +1 after each shot, and watch running percentages per drill with bars, an all-drills total, and a "Best touch right now" shout-out (hottest drill with 5+ attempts). Undo reverses the last tap; each drill row can reset. Tallies live in a new optional `shotLog` field ({drillId:{m,a}}, normalized with makes clamped to attempts; old saves load untouched) — separate from session makes/attempts and the shot-chart heat map. Two build bugs were caught by the suites and fixed pre-ship: a function-name collision with the heat map's addShot(x,y) (renamed logShotTap) and a duplicate #shotUndoBtn id (renamed #shotLogUndoBtn). SW v9, update version shotlog-2026-11. New suite test_shotlog.py (17 checks); all 11 suites pass individually with zero page errors.

## Update — Form Studio Printables (2026-11-17)
120-upgrades pick #59: the Form Studio goes on paper. Train > Form Studio gains a "Form Cards for the Fridge & Practice Bag" card with Print All 4, plus a Print button on each form card for single-card printing. The print layout is built from the SAME visuals and cue text (cloned into a print-only area at load — no duplication to drift): clean white cards with black borders, the visual on its dark panel exactly as in the app, full cues, and a "Ne'ala Hoops #14" footer; one card per page on Letter. Printing integrates with the app's existing print system via a body.printing-forms class (scoped @media print rules hide the summary/certificate sections, modals and scroll buttons; the summary and certificate prints are untouched — verified by the full suite run and a real Chromium PDF render, 4 pages, inspected). No state changes. SW v10, update version printables-2026-11. New suite test_printables.py (19 checks); all 12 suites pass individually with zero page errors.
