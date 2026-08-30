# The Clipboard

Squad selection, tournament management and fair game time tracking for a youth rugby squad.

**Live app:** https://meyerdj78.github.io/the-clipboard/

---

## What's here

| File | Purpose |
|---|---|
| `index.html` | The whole app (v3.1w) — React via CDN, no build step |
| `manifest.json` | Lets the app install to a phone home screen |
| `icon-192.png` / `icon-512.png` | App icons |

## Data & privacy

**No player data is stored in this repository.** Everything lives in the browser's
localStorage on the coach's own device. Squad names, assessments and attendance
never leave the phone unless deliberately exported.

This repo is public (required for free GitHub Pages), so nothing identifying a
child should ever be committed to it.

## Backup and recovery

Three independent layers:

1. **Auto-save** — every change writes to localStorage immediately.
2. **Named saves** — up to 8 restore points, created from the 💾 Saves button.
   Make one before every festival.
3. **Export code** — the Export button produces a text blob. Paste it into a note
   or email it to yourself. This is the only backup that survives clearing the
   browser or losing the device.

Code changes are versioned by git — any release can be rolled back from the
repository history.

## Install to a phone home screen

1. Open the live URL in Safari (iOS) or Chrome (Android)
2. Share → Add to Home Screen
3. It opens full-screen, no browser chrome

## Roadmap

Already in v3.1: multi-team festivals (1–4 teams), attendance roster,
team auto-assign, tournament-scoped fairness, scoring and try scorers.

Next:

- [ ] Season-long player records (training attendance, festival participation)
- [ ] Coach assessments: attitude, performance, competence, development focus
- [ ] Position eligibility — 12-a-side: 5 forwards, 9, 10, 15, 2 wings, backs
- [ ] Player combinations — who plays well together, who doesn't
- [ ] Read-only sharing for other coaches and parents
