# The Clipboard

Squad selection, tournament management and fair game time tracking for a youth rugby squad.

**Live app:** https://meyerdj78.github.io/the-clipboard/

---

## What's here

| File | Purpose |
|---|---|
| `index.html` | The whole app (v4.1) — React via CDN, no build step |
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

- [x] Player profiles, position eligibility, competence ratings, development focus
- [x] Training attendance, season timeline, attendance import codes
- [x] Behaviour and attitude ratings (TREDS), dated assessment snapshots
- [x] Player combinations — stored once, shown on both profiles
- [ ] Read-only sharing for other coaches and parents

## Positions (12 a side)

| Position | On pitch |
|---|---|
| Prop | 2 |
| Hooker | 1 |
| Lock | 2 |
| Scrum Half | 1 |
| Fly Half | 1 |
| Wing | 2 |
| Fullback | 1 |
| Back (general) | 2 |

Front row (2 props + hooker) and second row (2 locks) make the five forwards.

## Version history

- **v4.1** — behaviour and attitude ratings using the RFU core values (TREDS),
  training sessions on a season timeline, attendance register and import codes,
  player combinations, dated assessment snapshots, overall star average removed
- **v4.0** — player profiles, position eligibility, 1–5 star competence ratings,
  development focus areas, coach notes, position cover summary
- **v3.1w** — first hosted build: multi-team festivals, roster, scoring

## Attendance import codes

Rather than tapping 25 names after every session, an attendance register can be
imported as a code. The code is base64 of this JSON:

```json
{
  "k": "attendance",
  "date": "2026-09-07",
  "title": "Tuesday training",
  "location": "Down Grange",
  "present": ["Jack Meyer", "Theo", "Roo"],
  "absent": ["Zach"]
}
```

Names are matched against the squad case-insensitively, falling back to a unique
first-name or prefix match. The app shows a preview of what matched, what didn't,
and who wasn't mentioned, before anything is written. Nothing is applied until
that preview is confirmed.

Anyone not mentioned in the code is left unset rather than marked absent.

## Assessment approach

There is deliberately **no overall rating** for a player. Skills are compared
against that player's own profile ("strongest", "most room to grow"), never
against other children. Behaviour uses England Rugby's TREDS core values —
teamwork, respect, enjoyment, discipline, sportsmanship — alongside four
coaching behaviours: listening, coachability, effort, and influence on team-mates.
