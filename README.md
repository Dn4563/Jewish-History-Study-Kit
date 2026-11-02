# Jewish History Study Kit by David Noskow

Live site (once Pages is on): https://dn4563.github.io/Jewish-History-Study-Kit/

Built the same way as the Pre-AP Chemistry kit: content files in `content/`, the shared engine in `core/` (copied from Study-Hub-by-David/kit-core), and one built `index.html`. Don't edit `index.html` by hand.

## Add a unit
1. Make a folder such as `content/unit-01/` with `cards.md`, `asks.json`, `watch.md`, `trees.md`, `guide.json`, `scenarios.json` and `practice.json`. The formats are in `core/README.md`; the Chem kit's `content/ch04-atoms/` is a full example.
2. Add the unit to `units` in `content/course.json`, with `"learnMix": true` (and `"recall": true` for every unit after the first):
   ```json
   { "id": "u1", "dir": "unit-01", "label": "Unit 1", "title": "Unit title", "blurb": "One sentence on what it covers.", "learnMix": true }
   ```
3. Build and test (below), then add the course or unit to the Study Hub's `courses.json`.

## Build and test
Node 18 or newer. The first time, run `npm install`. After every change run `npm test`: it parses the content, builds `index.html` and clicks through every tab. To update the engine, clone Study-Hub-by-David next to this repo and run `npm run sync-core`.

## Publish
Merge into `main`, then turn on Pages once: Settings → Pages → Deploy from a branch → `main` / `(root)`.

See `CLAUDE.md` for how units should be built.
