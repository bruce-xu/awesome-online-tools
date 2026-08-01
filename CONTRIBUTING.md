# Contributing to Awesome Online Tools (wtoolskit)

Thanks for helping grow this list! This catalog focuses on **free, browser-based, client-side tools** from the wtoolskit family and on other tools that share the same philosophy: no account, no upload, everything runs in your browser.

## What belongs here

- Tools that are part of the wtoolskit family:
  **WebTools**, **CodeJet**, **APIPulse**, **GameHub**, **PeerBeam**.
- Other free, client-side, no-signup web tools that fit the privacy-first philosophy.

## Entry format

Each entry is one line, in English, following this exact shape:

```markdown
- [Tool Name](https://example.com/tool) — Short, factual description.
```

Rules:

- Link **directly to the tool page**, not a homepage section.
- Description: one sentence, factual, no marketing fluff, no "best" / "awesome".
- Keep entries grouped under their existing category/section.
- Use an existing category if one fits; propose a new section only when truly needed.

## How this list is generated

The `README.md` is **generated** from the **wtoolskit monorepo** (the five sibling product repositories). The generator script lives at `webtools/scripts/gen-awesome-readme.mjs` and reads each product's real source data, so tool names, links, and categories stay 100% in sync with the live sites.

To regenerate (run from inside the monorepo):

1. Edit the relevant product source (e.g. add a game in `games/src/lib/game-meta.ts`).
2. From the `webtools` repo root, run:
   ```bash
   node scripts/gen-awesome-readme.mjs
   ```
3. Copy the produced `awesome-online-tools/README.md` into this standalone repo and commit.

Direct manual edits to `README.md` are fine for adding external tools, but they will be **overwritten** on the next regeneration. For anything belonging to the wtoolskit family, please update the source repo and regenerate instead, then open a PR describing the change.

## Pull requests

1. Fork and create a branch.
2. Add your entry following the format above.
3. Make sure the link returns HTTP 200 and the tool is free to use.
4. Open a PR with a short description of what you added and why.
