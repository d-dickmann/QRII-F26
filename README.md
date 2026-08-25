# QRII-F26 — course website and materials

Public-facing repository for **Quantitative Reasoning II**, Fall 2026, The University of Austin.

The website is published with GitHub Pages from the `main` branch. Editing a `.md` file and pushing updates the live site within a minute or two — there is nothing to build locally.

## Layout

| Path | What goes here |
|---|---|
| `index.md` | Home page |
| `schedule.md` | Meeting-by-meeting schedule |
| `assignments.md` | Homework |
| `materials.md` | Textbook, software, links |
| `_config.yml` | Site title, theme, and nav bar order |
| `slides/` | Lecture slides (PDF) |
| `exercises/` | Homework and in-class exercises (PDF) |
| `data/` | Datasets |
| `readings/` | Assigned readings |

## Editing

- Pages are plain Markdown with a small YAML block at the top. Leave the block alone; edit below it.
- To add a page to the top navigation bar, create the `.md` file and add its filename to `header_pages` in `_config.yml`.
- To link a file you've added — say `exercises/HW1.pdf` — write `[Homework 1](exercises/HW1.pdf)`.

## Publishing

Settings → Pages → Source: **Deploy from a branch** → Branch: **main** / **/ (root)**.

The repository must be **public** for GitHub Pages to publish on a free account.
