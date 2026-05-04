# Workflow

How I publish on MAIS Log. This document is for future-me's reference.

## Setup

Local prerequisites:

- [Zola](https://www.getzola.org) — install via package manager or
  `cargo install zola`
- A working knowledge of git
- A markdown editor

Repo clone:

```sh
git clone git@github.com:SHA888/mais-log.git
cd mais-log
```

Local preview:

```sh
zola serve
```

Build for production (CI does this):

```sh
zola build
```

## Drafting

Drafts live in `_drafts/`. Files in `_drafts/` are committed to the repo
but excluded from the Zola build. They are visible in `git log` if anyone
looks, which is consistent with the public-from-day-one philosophy.

Workflow for a new post:

1. Create a file in `_drafts/`. Filename can be a temporary slug.
2. Write. Commit freely. The half-formed thinking is fine in `_drafts/`.
3. When ready to publish, move to the appropriate track:
   - `content/notes/YYYY-MM-DD-slug.md`
   - `content/synthesis/YYYY-MM-slug.md`
   - `content/essays/YYYY-QN-slug/index.md`
4. Add proper front matter (see below).
5. Commit with a message like "publish: <track>/<slug>".
6. Push. CI builds and deploys.

## Front matter

Minimum for any post:

```toml
+++
title = "The post title"
date = 2026-05-04
description = "One-sentence summary."
+++
```

Optional fields used:

- `tags = ["tag1", "tag2"]` — for taxonomy
- `lang = "id"` — for Indonesian-language posts
- `draft = true` — to keep a post in `content/` but not built (rarely needed
  since `_drafts/` exists)

## Editing published posts

### Notes

Editable freely. No revision notes. Push the change.

If the change is substantive enough that readers might be confused, consider
whether it should be a new note instead. The git diff is the record either
way.

### Synthesis and essays

Append-only with revision notes. The original text stays.

For a substantive change, append a `## Revisions` section at the bottom of
the post (or add to it if it exists):

```markdown
## Revisions

- **2026-08-15** — Added §4 on indirect prompt injection after reading
  Greshake et al. more carefully. The original §4 on direct injection
  remains as written above.
```

Typo fixes do not require revision notes.

If the central thesis of an essay becomes wrong, write a new essay. Don't
overwrite the old one.

## Commit message conventions

- `publish: notes/<slug>` — first publication of a note
- `publish: synthesis/<slug>` — first publication of a synthesis piece
- `publish: essays/<slug>` — first publication of an essay
- `note: <slug>: <description>` — edit to an existing note
- `revise: <track>/<slug>: <description>` — substantive revision of a
  synthesis or essay (paired with a Revisions entry in the post)
- `typo: <track>/<slug>` — typo fix
- `meta: <description>` — repo-level changes (templates, config, docs,
  README)

## Deploy

Static site builds to `public/`. Deploy is via **GitHub Pages** (using the
repo's `gh-pages` branch).

**Why GitHub Pages?**

- Cost: free, no billing risk
- Build pipeline: native GitHub Actions support; no external CI needed
- Custom domain: full support for `sha888.id` via CNAME
- Durability: same as the repo itself (GitHub mirrors matter, but the repo
  is our source of truth)
- Low maintenance: no VPS to manage, no third-party account to monitor

CI (GitHub Actions) builds the site on every push to `main`, then deploys
the `public/` directory to the `gh-pages` branch. GitHub automatically serves
the `gh-pages` branch at the configured custom domain.

The deployment target is `https://sha888.id`.

## Backups and durability

- The git repo is the source of truth. GitHub is the primary remote.
- GitHub Pages is deployed from `gh-pages` branch; the source (`main`) is
  always recoverable from the static output.
- Periodically (quarterly?) push to a second remote (self-hosted Gitea,
  Codeberg, or similar) for durability against GitHub-specific risk.
- Local clones on at least two machines.
- The repo is small (markdown only); offline backups are cheap.
- The site's content is also backed up in the `gh-pages` branch history
  on GitHub, independent of `main`.

## GitHub Pages setup

Repository settings (`github.com/SHA888/mais-log/settings/pages`):

1. **Source**: Deploy from a branch
2. **Branch**: `gh-pages` / `/ (root)`
3. **Custom domain**: `sha888.id` (requires DNS CNAME)
4. **Enforce HTTPS**: enabled

CI/CD (GitHub Actions) builds and deploys automatically. No manual steps
after initial DNS setup.

## When this workflow changes

This document is editable. When the workflow changes, update this and note
the change in the next note. Don't let documentation drift from practice.
