# Portfolio: P. Tarun Sai, Data Analyst

A single-page portfolio in plain HTML, CSS and a little JavaScript. No build step, no dependencies.

**Live site (after enabling GitHub Pages):** https://tarun-sai99.github.io/portfolio/

## How to open it

- **Easiest:** download or clone the repo and double-click `index.html`.
- **Locally with a server:** run `python3 -m http.server 8000` in this folder, then visit http://localhost:8000.
- **Publish free on GitHub Pages:** repo **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)` → Save**. The site appears after about a minute.

Fonts load from Google Fonts. Offline, the page falls back to Georgia and system fonts.

## Files

| File | What it holds |
|---|---|
| `index.html` | All content: hero, about, four projects, process, contact |
| `style.css` | All styling. Colors, fonts and spacing are variables at the top |
| `script.js` | Scroll reveal, theme toggle, footer year |
| `photo.png` | Portrait shown in About. Replace the file (keep the name) to change it |
| `og.png` | Preview image shown when the link is shared on LinkedIn, WhatsApp, etc. |
| `images/` | Project thumbnails (WebP, about 30 KB each), one per project row |

## Design choices (adjust these)

**Concept: the analyst's notebook.** The page is graph paper. Sections are numbered like figures, the hero is a bar chart that grows on load, and projects are ledger rows with one headline number each, not cards. The contact section is a dark "ink" band.

**Palette** (variables at the top of `style.css`)

| Token | Light | Dark | Use |
|---|---|---|---|
| `--paper` | `#F3EFE4` | `#121315` | Background |
| `--ink` | `#16171A` | `#ECE7DA` | Text, bars |
| `--muted` | `#57544B` | `#A8A395` | Secondary text |
| `--rule` | `#CFC9B8` | `#34332F` | Hairlines |
| `--accent` | `#C52F14` | `#FF6B47` | The one accent (vermilion) |

To re-theme, change `--accent` first. Dark mode follows the visitor's system setting, and the round button in the top bar switches it (the choice is remembered).

**Fonts** (the `<link>` in `index.html`, and `--serif`, `--sans`, `--mono` in `style.css`)

- **Fraunces** (serif): headings and big numbers.
- **IBM Plex Sans:** body text.
- **IBM Plex Mono:** labels, tool lists, captions.

**Motion** (all off for visitors who prefer reduced motion): hero name rises and bars grow on load; sections fade up on scroll; project rows draw an accent underline on hover.

**Layout:** one column on phones. From about 900px, project rows have three columns (index, text, headline number) and the process steps sit in a row of four. Content is capped at 1120px.

## Editing content

- **Projects:** the `<li class="row">` blocks in `index.html`. The big number is the `<p class="stat">`.
- **Skills:** the `<ul>` inside `.skills`.
- **Process steps:** the `.steps` list. Each links to a real file in your repos.
- **Contact links:** the `.links` list at the bottom.
- **Link preview:** the `og:` meta tags in `<head>`. If you use a different web address, update the `canonical`, `og:url` and `og:image` URLs there.

Project summaries were written from each repo's README.
