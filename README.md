# We-Ko-PAW

Live scoring for We-Ko-PAW — a static web app on GitHub Pages, backed by a Firebase Realtime
Database. Forked from [golf-event-template](https://github.com/phodgman22/golf-event-template),
the reusable base for future events — that repo, not this one, is where template-wide fixes
and new formats belong.

- Players: https://phodgman22.github.io/We-Ko-PAW/
- Commissioner console: https://phodgman22.github.io/We-Ko-PAW/admin.html

**Full technical reference:** [HANDOFF.md](HANDOFF.md) — architecture, data model, every
format and setting, and the bugs already found and fixed (don't reintroduce them).

Its own Firebase project (`we-ko-paw`) and a fresh `ADMIN_PIN` are already wired up —
isolated from the template's database, so nothing entered here touches Covid Cup 2026's
data or vice versa. Still to finish before this is live for real players:
1. Set up the event from the commissioner console — event name, courses, roster, rounds.

Run locally with `node serve.js`, then open http://localhost:8765. Scoring tests:
`node tests/run.mjs`.
