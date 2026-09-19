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

## Status

- **Chapter 1 — PREP**: complete. 40 questions.
- Remaining 11 frameworks: listed in-app as "Coming next".

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
