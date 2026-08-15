# SpecWire

Independent tech explainers and review round-ups, built as a static site.
Phones, laptops and PCs, displays, AI models and audio — every figure traced to
the standard, datasheet, spec page or named lab measurement it came from.

**Live site:** https://mudlbum.github.io/specwire

## What this is

A zero-dependency static site generator plus an editorial system that refuses to
publish an unsourced number. `scripts/factcheck.py` fails the build if a key
takeaway has no resolving source or no figure in it; `scripts/validate.py` fails
the deploy on dead links, missing policy pages, duplicate H1s, bad meta lengths
or placeholder text.

The site does not operate a test lab and never implies otherwise. Measured
values are attributed by name to whoever measured them.

## Quick start

```bash
pip install -r requirements.txt
python3 build.py                 # builds into dist/
python3 build.py --serve         # builds, then serves on :8000
python3 scripts/validate.py      # publication gate — must exit 0
```

On a OneDrive- or network-mounted checkout, build to a local path instead:

```bash
export SW_DIST=/tmp/swdist
SW_DIST=/tmp/swdist python3 build.py
SW_DIST=/tmp/swdist python3 scripts/validate.py
```

## Writing a post

```bash
python3 scripts/new_post.py "Your headline here" --category phones
```

Categories: `phones`, `computers`, `ai`, `displays`, `audio`, `explainers`.
A category stays hidden from the nav, sitemap and homepage until its first
article exists, so empty sections never render as thin pages.

`CLAUDE.md` is the editorial standard — sourcing rules, voice, banned phrases,
post types, artwork policy. `automation/daily-post.md` is the daily routine and
the backlog of queries worth answering.

## Front matter worth knowing about

| Key | Effect |
| --- | --- |
| `chart:` | Hero becomes a real chart of those numbers, with the source printed on it |
| `hero:` | `chart`, `photo` or `cover` — overrides the automatic choice |
| `video:` | Lazy, cookie-less YouTube embed below the article |
| `products:` | Official spec / retail links, rendered as a "check the specs yourself" box |
| `key_takeaways:` | Must be mappings with a bolded figure and a source index, or the build fails |

## Environment

| Variable | Purpose |
| --- | --- |
| `PEXELS_API_KEY` | Licensed hero photography. Without it, heroes fall back to a typographic cover — not an error |
| `SW_DIST` | Build output directory, default `dist/` |
| `SW_OFFLINE` | Use only already-cached photos; skip network calls |

## Theming

Dark by default, light via system preference, and an explicit toggle in the
header that persists in `localStorage`. Every colour is a CSS custom property —
no component hard-codes a hex value. An inline script in `<head>` applies the
saved theme before first paint so there is no flash of the wrong palette.

## Deployment

Push to `main`. GitHub Actions rebuilds, re-runs the validator and deploys to
Pages. A failing validator fails the deploy, by design.

## Licence

Content © SpecWire. Code in this repository is provided as-is.
