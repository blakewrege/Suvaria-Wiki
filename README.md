# Suvaria-Wiki — Generated Player Site

This repository is the **generated, player-safe output** of the private [`blakewrege/Suvaria`](https://github.com/blakewrege/Suvaria) campaign repository. The live site is <https://blakewrege.github.io/Suvaria-Wiki/>.

## Ownership rule

Do not author campaign content directly in this repository. Edit the canonical private source, update its explicit publication status, and run the publisher. A later rebuild replaces the managed files here.

| Repository | Role |
|---|---|
| `blakewrege/Suvaria` | Private canonical source, including GM notes, drafts, and published-source Markdown |
| `blakewrege/Suvaria-Wiki` | Public generated pages and GitHub Pages deployment |

## Structure

- [`docs/`](docs/) — flat generated Markdown. The hierarchy players see comes from navigation, not folders or symlinks.
- `mkdocs.yml` — generated navigation and theme settings.
- `requirements.txt` — pinned MkDocs dependency.
- `site/` — ignored local build output.
- `gh-pages` branch — deployed website output.

Latest indexed session: **078**.

This is the latest published session, not necessarily the next scheduled game. Upcoming-session preparation and unfinished work live in the private repository's [WIP.md](https://github.com/blakewrege/Suvaria/blob/main/WIP.md) and session indexes (GM access required). Keep task handoffs and spoilers there, not in this public repository.

The public site contains only entries explicitly marked `published`. Drafts and GM files remain in the private repository. Major campaign locations are also maintained on [Obsidian Portal](https://suvaria.obsidianportal.com/wikis/main-page).

## Maintainer workflow

1. Make the authored change in the private `Suvaria` repository.
   Read its README, Codex.md and WIP.md for source ownership and unfinished work. Before rebuilding, check this public checkout for local edits and reconcile them with the private source; do not overwrite uncommitted work.
2. Review `tools/player-handouts-manifest.json`; new pages begin as drafts.
3. Run `tools/publish_player_handouts.py` from the private checkout.
4. Review the diffs in both repositories.
5. Commit and push each repository separately.
6. From this checkout, deploy with `mkdocs gh-deploy --force`.

The publisher rejects common spoiler markers, private absolute paths, and broken local links, but it cannot replace human spoiler review. Never publish a true secret temporarily: removing it later does not erase public Git history.
