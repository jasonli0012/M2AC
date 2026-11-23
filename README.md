# M2AC

Project homepage for **"Language-Mediated Multimodal Reasoning for Agile Coordination of Uncrewed Surface Vehicle Swarms"**.

**Live page:** <https://jasonli0012.github.io/M2AC/> — served directly by GitHub Pages; every push to `main` updates it within a minute or two. No local deployment is needed.

- `index.html` — the whole page (self-contained: no frameworks, web fonts or icon libraries)
- `assets/` — result figures, demo video (`assets/M2AC.mp4`), and video poster
- `dataset/` — dataset description and download link

## Dataset

Download from Baidu Netdisk: <https://pan.baidu.com/s/16j_rYS9jQJlKVoRFpHwkqg?pwd=my2c> (access code: `my2c`).

## Editing notes

- **Figures.** Only two figures are published: `assets/results_comparison.*` (method comparison) and
  `assets/human_guidance.*` (before / during / after human guidance). Each is stored as `.webp`
  (served first) plus a `.jpg` fallback, referenced through a `<picture>` element. To replace one,
  export both formats under the same base name and keep the `width` / `height` attributes of the
  matching `<img>` in `index.html` consistent with the new aspect ratio.
  The figure sources are vector PDFs, so render them with the PDF crop box rather than the full page,
  e.g. `pdftoppm -png -r 300 -cropbox -singlefile figure.pdf out`.
- **Method details.** The paper is unpublished, so the page describes the approach only at the level of
  the abstract and publishes no method or architecture figures. Keep implementation details out of
  `index.html` until the paper is public.
- **Numbers.** The comparison table repeats the success, recall, and F1 values printed in the
  comparison figure; update both together if the figure changes.
- **Links.** The paper button is a placeholder ("coming soon"); turn it into a link once the paper is out.

## Preview locally (optional)

```bash
python3 -m http.server 8000      # or, with Node: npx serve .
# open http://localhost:8000
```
