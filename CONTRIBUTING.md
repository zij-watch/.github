# Contributing to Zij

These rules apply to every repository in `zij-watch` that has no contributing guide of its own.

## Branches and pull requests

- One branch per change, made from an up-to-date `main` and named for its area and topic: `design/lockups`, `app/calendar`, `pipeline/calibration`.
- Never push to `main`. Open a pull request into `main` and fill in the template; a maintainer reviews and merges.
- Keep pull requests small: one topic each, small enough to review in one sitting. Split anything larger.

## Commits

The subject is a short sentence in sentence case that says what changed, with the area first when it helps:

```
Brand book: the mark is the Seal, the dial an instrument
Pin the Python science stack to the research versions
```

No type prefixes (`feat:`, `fix:`), no emoji, no full stop at the end. When the reason is not obvious from the change, the body says why, in plain sentences wrapped at 72 characters.

## Design

Colours, type, the mark, controls and motion are set in `docs/design/` of the app repository. A design change goes there first, in its own pull request, following `docs/design/CONTRIBUTING.md`. App code follows the design book, never the other way round.

## Secrets

Never commit a secret. The FIRMS `MAP_KEY` lives in `.env.local` (`app/.env.local` in the app), which git ignores; `.env.example` shows the name with no value. If a key is ever committed, write to [info@zij.watch](mailto:info@zij.watch) at once: it is revoked and replaced, because deleting it from the history is not enough.
