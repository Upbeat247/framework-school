# Framework School

**Live: https://upbeat247.github.io/framework-school/**

A silent, offline school for communication frameworks. Learn each framework properly,
then prove you have it with tests hard enough to be worth your time.

Companion to **SpeakMaster**:

- **SpeakMaster** (phone, private) — *production*: say it, deliver it, prep the real meeting.
- **Framework School** (work laptop, silent) — *recognition & judgement*: know the frameworks cold.

## Built for a corporate laptop

Deliberately self-contained so it cannot trip IT policy:

- **One HTML file.** No build step, no dependencies, no install.
- **Zero network requests.** No CDN, no web fonts, no API calls, no telemetry. Verified.
- **No permissions.** No microphone, no camera, no location, no notifications.
- **Local only.** Progress lives in `localStorage` on that browser and never leaves the device.

Open `index.html` straight from disk (`file://`) — or serve it statically. Both work identically,
including offline and on a plane.

## How a chapter works

1. **Read** — the idea, when to reach for it, the anatomy of each element (with its classic
   failure), four worked examples across different domains, and a weak-vs-strong pair.
2. **Check each element** — a short test per element. You must answer *every* question
   correctly; anything you miss comes back until you get it right.
3. **Drill** — endless mixed questions from the whole chapter. Questions you miss are
   weighted to return sooner.
4. **Mastery exam** — 12 questions sampled across every element, 90% to pass. Passing
   unlocks the next chapter.

## Why the questions are hard

The difficulty lives in the *wrong* answers. Every distractor is a real mistake a competent
professional makes — never an obviously silly option. Question types:

- Pick the strongest of four competent-looking versions
- Choose the best next line in a half-finished response
- Diagnose which element is failing, and why
- Spot the impostor that isn't the framework at all
- Label which element a line is doing
- Transfer the framework to an unfamiliar domain

**Every option carries its own explanation**, shown after you answer — why the right one wins
*and* why each wrong one fails. Getting it wrong plus a sharp explanation is the highest-value
moment in the app, so that is where the teaching lives.

## Progression

Chapters are written to build in order, but **nothing is locked** — open whichever one you are
actually on. Progress is stored per browser (`localStorage`) with no sync, so a device that has
not seen your earlier work must not stand between you and the chapter you were on. The home
screen still points at where to go next ("Start here" / "Continue here"), following your real
progress rather than the prescribed order.

Once you have mastered earlier chapters **on that device**, every later exam reserves **3 of its
12 slots** for questions drawn from them, so old frameworks keep resurfacing. Mastery that decays
is not mastery.

To restore strict sequential unlocking, set `GATED = true` in `index.html`.

### On cross-device sync

Deliberately not built. Sync would mean recurring outbound requests from a managed laptop to an
external service — which is data egress, not browsing, and is exactly the traffic shape that gets
flagged. The zero-network property is worth more than automatic sync for state this small. A
copy/paste sync code (still zero network) is the fallback if it ever becomes worth the friction.

## Status

**Complete — 12 chapters, 349 questions.**

| # | Chapter | Questions |
|---|---------|-----------|
| 1 | PREP — Point → Reason → Example → Point | 40 |
| 2 | The 3-Part Answer — Introduction → Body → Conclusion | 28 |
| 3 | Self-Introduction — Name → Role → Value → Hook | 30 |
| 4 | One-Point Clarity — The One Point → Anchor → Landing | 26 |
| 5 | STAR — Situation → Task → Action → Result | 28 |
| 6 | Stakeholder Meeting — Context → Problem → Recommendation → Next Steps | 28 |
| 7 | Bad News — State → Reason → Plan → Support | 28 |
| 8 | Technical Briefing — Thesis → Architecture → Demo → Takeaway | 28 |
| 9 | AIDA — Attention → Interest → Desire → Action | 28 |
| 10 | Impromptu (ABT) — And → But → Therefore | 26 |
| 11 | Q&A Mastery — Listen → Clarify → Pause → Answer → Bridge | 33 |
| 12 | Executive Presence — Credibility → Vision → Call to Action | 26 |

## Link to SpeakMaster

The home screen and every passed mastery exam carry a link to
**https://speakmaster.netlify.app** (opens in a new tab), so framework practice can hand
straight over to speaking practice.

The link is a plain `href` — inert until clicked — so this page still makes **no network
requests of its own**. Note that the destination does: SpeakMaster uses the microphone and
calls an AI endpoint, so it is a personal-device app, not a work-laptop one.

## Where to open it

- **Work laptop:** https://upbeat247.github.io/framework-school/ — `github.io` generally passes
  corporate proxies as developer tooling. Verified live: the page issues **exactly one** network
  request (the document itself).
- **Offline fallback:** it is one file, so save the page (⌘S) or copy `index.html` anywhere and
  open it. It behaves identically from `file://`.
- **Local preview:** `python3 -m http.server 5240 --directory framework-school`

Progress is per-browser (`localStorage`), so work and home progress stay separate.

> If the URL is ever blocked, use the offline copy or ask IT to whitelist it. Never tunnel or
> VPN around the company proxy to reach it.

## Publishing changes

```bash
git add -A && git commit -m "..." && git push
```

GitHub Pages serves `main` from the repo root, so a push is the deploy.
