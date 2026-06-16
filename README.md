# ActWorld — Project Page

Project page for **ActWorld: From Explorable to Interactive World Model via Action-Aware Memory**.

The page combines the paper content with the interactive qualitative-comparison viewer
(originally the `8993_Visualization.html` supplementary), rebuilt so each clip loads as a
standalone `.mp4` file instead of one 71 MB base64 blob.

## View it

Just open `index.html` in a browser (works directly over `file://` — the comparison
metadata is loaded via `static/js/comparisons.js`, not `fetch`, so there are no CORS issues).
For GitHub Pages, push this folder to a repo and enable Pages; `.nojekyll` is already present.

## Layout

```text
index.html                         # the whole page (HTML + CSS + JS inline)
static/
  images/teaser.png                # Fig. 1  (hero teaser)
  images/pipeline.png              # Fig. 2  (method)
  images/qualitative.png           # Fig. 3  (rollouts)
  pdfs/actworld.pdf                # the paper (linked from the "Paper" button)
  js/comparisons.js                # auto-generated metadata for the comparison viewer
  videos/comparisons/<clip>/<model>.mp4   # 14 clips × 6 methods = 84 videos (~51 MB)
```

## Sections

Hero · Teaser · Abstract · Key stats · Contributions · Method (pipeline + 4 points) ·
**Interactive side-by-side comparison** (14 I-Bench samples, 6 methods each, lazy-loaded,
per-row / play-all controls, first/third-person filter, *Ours* highlighted) ·
Quantitative results (tabbed: VLM-Action-Judge / Key-Mouse-Following / VBench) ·
Qualitative figure · BibTeX (copy button) · Footer.

## Placeholders to fill in

These currently point to `#` in `index.html` — replace when available:

- **arXiv** button `href` (hero)
- **Code** button `href` (hero)
- Author personal-link `href`s (hero) — all `#`
- `static/images/favicon.ico` — replace with your own
- Optional: create `static/images/social_preview.png` (1200×630) for richer link previews

## Regenerating the comparison assets

The 84 clips and `comparisons.js` were extracted from the base64 supplementary
(`arxiv/V2/8993_Visualization.html`). If the supplementary changes, re-run the extraction
scripts that produced `static/videos/comparisons/` and `static/js/comparisons.js`.

## License

Page template adapted from the
[Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template)
(Nerfies lineage), licensed under
[CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/).
