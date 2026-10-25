# farukoguz.github.io

Personal CV site for **Ramazan Faruk Oğuz**, served by GitHub Pages at
<https://farukoguz.github.io/>.

Plain HTML and CSS, no build step, no dependencies.

## Contents

| File | Purpose |
|---|---|
| `index.html` | The CV page (also contains the print stylesheet) |
| `Ramazan_Faruk_Oguz_CV.pdf` | Downloadable 2-page A4 CV, linked from the page |
| `photo.png` | Circular profile photo (400×400, transparent corners) |
| `.nojekyll` | Tells GitHub Pages to serve files as-is instead of running Jekyll |

## Updating

The page and the PDF are generated from the same content, kept locally in
`~/Documents/cv-2026/`:

```sh
# 1. edit the content in cv.html, then rebuild the PDF
"/Applications/Brave Browser.app/Contents/MacOS/Brave Browser" \
  --headless=new --disable-gpu --no-pdf-header-footer \
  --print-to-pdf=Ramazan_Faruk_Oguz_CV.pdf "file://$HOME/Documents/cv-2026/cv.html"

# 2. mirror the change into index.html, then publish
cp Ramazan_Faruk_Oguz_CV.pdf ~/Documents/cv-2026/site/
```

Commit and push to `main`; Pages redeploys automatically in about a minute.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000/
```
