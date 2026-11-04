# Portfolio: P. Tarun Sai, Data Analyst

A single-page portfolio in plain HTML, CSS and a little JavaScript. No build step, no dependencies to install.

## How to open it

- **Easiest:** double-click `index.html`. It opens in your browser.
- **Or serve it locally:** from this folder run `python3 -m http.server 8000`, then visit http://localhost:8000.
- **To publish:** upload the folder to any static host (GitHub Pages, Netlify, Vercel). Set the site root to `portfolio/`.

The fonts load from Google Fonts, so you need an internet connection to see them. Offline, the page falls back to Georgia and system fonts and still works.

## Files

| File | What it holds |
|---|---|
| `index.html` | All content: hero, about, four projects, contact |
| `style.css` | All styling. Colors, fonts and spacing are variables at the top |
| `script.js` | Scroll reveal and the footer year (about 20 lines) |
| `photo.png` | Your portrait, shown in the About section. Replace the file (keep the name) to change it |

## Design choices (adjust these)

**Concept: the analyst's notebook.** The page is a sheet of graph paper. Sections are numbered like figures (01, 02, 03), the hero is a bar chart that grows on load, and projects are ledger rows with one headline number each, not cards. The contact section flips to a dark "ink" band.

**Palette** (variables at the top of `style.css`)

| Token | Value | Use |
|---|---|---|
| `--paper` | `#F3EFE4` | Warm off-white background |
| `--ink` | `#16171A` | Text, bars, contact band |
| `--muted` | `#57544B` | Secondary text |
| `--rule` | `#CFC9B8` | Hairlines, dashed grid lines |
| `--accent` | `#C52F14` | The one accent: vermilion, about 4.9:1 on paper |
| `--accent-hi` | `#FF6B47` | Same accent, lightened for the dark band |

To re-theme, change `--accent` and `--accent-hi` first. Keep `--accent` dark enough to stay readable on `--paper`.

**Fonts** (the `<link>` in `index.html` and `--serif`, `--sans`, `--mono` in `style.css`)

- **Fraunces** (serif): headings and the large numbers. It has character without being fussy.
- **IBM Plex Sans:** body text, for readability.
- **IBM Plex Mono:** small labels, tool lists and captions. It gives the "data" feel. Plex Sans and Mono are from the same family, so they sit well together.

**Motion** (all switched off if the visitor prefers reduced motion)

- Hero name slides up and the bars grow in sequence on load.
- Sections fade up as they scroll into view.
- Project rows draw an accent underline on hover; links get small arrow and underline moves.

**Layout:** one column on phones. From about 900px, project rows become three columns (index, text, headline number). Content width is capped at 1120px.

## Editing content

- **Project text and stats:** edit the `<li class="row">` blocks in `index.html`. The big number on each row is the `<p class="stat">` element.
- **Skills:** the `<ul>` inside `.skills`. The short descriptions under each skill are taken from the project READMEs, so update them if your experience changes.
- **Contact links:** the `.links` list at the bottom of `index.html`.

## Project summaries

The summaries were written from each repo's README (tools and key findings as stated there). The Power BI skill is listed but has no project yet.
