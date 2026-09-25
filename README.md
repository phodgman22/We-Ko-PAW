# We-Ko-PAW

Live scoring for We-Ko-PAW — a static web app on GitHub Pages, backed by a Firebase Realtime
Database. Forked from [golf-event-template](https://github.com/phodgman22/golf-event-template),
the reusable base for future events — that repo, not this one, is where template-wide fixes
and new formats belong.

- Players: https://phodgman22.github.io/We-Ko-PAW/
- Commissioner console: https://phodgman22.github.io/We-Ko-PAW/admin.html

**Full technical reference:** [HANDOFF.md](HANDOFF.md) — architecture, data model, every
format and setting, and the bugs already found and fixed (don't reintroduce them).

Still to finish before this is live for real players:
1. Create a new Firebase Realtime Database project for We-Ko-PAW and paste its config into
   `firebase-config.js`; deploy `database.rules.json` to it. (Still pointing at the template's
   Firebase project right now — see the note in `HANDOFF.md`.)
2. Set a real `ADMIN_PIN` in `admin-pins.js`.
3. Set up the event from the commissioner console — event name, courses, roster, rounds.

Run locally with `node serve.js`, then open http://localhost:8765. Scoring tests:
`node tests/run.mjs`.
