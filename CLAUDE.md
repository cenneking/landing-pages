# Landing Pages — Arena

This is Christina's landing-page arena: one workspace that holds every sales/landing page she publishes, with a single path to get them live on the web.

## What lives here

Each top-level folder is one landing page. Each page is a single self-contained `index.html` plus its logo image.

| Folder | Page | Live URL |
|---|---|---|
| `sprint/` | The REAL Heroic Journey Sprint — 4-week intensive | `go.christinarobertsenneking.com/sprint` |
| `irreplaceable/` | The Irreplaceable You | `go.christinarobertsenneking.com/irreplaceable` |
| `wounds-to-wisdom/` | Wounds to Wisdom — 16-week group coaching | `go.christinarobertsenneking.com/wounds-to-wisdom` |

Each folder also has its own `CLAUDE.md` with page-specific notes (what's safe to edit vs. not). Read those before editing a page.

To add a new page: create a new folder at the root (the folder name becomes the URL slug), drop an `index.html` and a logo in, commit, push.

## Brand constants (do not change without asking)

- Colors: teal, gold, cream
- Fonts: Cormorant Garamond (display), Libre Franklin (body)
- Logo filename is always `Christina-Logo-nog.png` — do not rename or re-path

## Publishing model

Single GitHub repo, deployed via GitHub Pages, served from one subdomain with path-based routing:

```
<repo root>/
├── CNAME                          → go.christinarobertsenneking.com
├── .gitignore
├── CLAUDE.md
├── sprint/index.html
├── irreplaceable/index.html
└── wounds-to-wisdom/index.html
```

Pages are self-contained — each folder keeps its own logo copy, no shared `assets/` directory.

## Workflow for edits

1. Edit the `index.html` inside the relevant folder. Only the words, unless Christina specifically asks for a design change.
2. Double-click the file to preview in the browser.
3. When happy, publish:
   ```
   git add .
   git commit -m "describe what changed"
   git push
   ```
4. GitHub Pages rebuilds in ~60 seconds.

## Notes for Claude

- When Christina asks for page changes, edit `index.html` in the relevant folder directly. Confirm what you changed and remind her to preview before pushing.
- When in doubt about scope, follow the per-folder `CLAUDE.md`.
- Don't introduce build tools, bundlers, or frameworks. These pages are intentionally single-file HTML.
- Don't rename the top-level folders — the folder name IS the URL slug.
