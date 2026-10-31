# tm-pham.github.io

Personal website of Mui Pham, built with [Quarto](https://quarto.org) and published to GitHub Pages by `.github/workflows/publish.yml` on every push to `master`.

## Working on the site

```bash
quarto preview      # live preview at http://localhost:4200
quarto render       # build into _site/
```

## Where things live

| What | Where |
|---|---|
| Homepage (hero + About) | `index.qmd` |
| CV page / PDF | `cv.qmd`, `files/Pham_CV.pdf` |
| Research and publications | `research/index.qmd`, `research/publications.qmd` |
| Teaching and resources | `teaching/` |
| Photo gallery | `photography.qmd`, `images/photos/` |
| Colours, fonts, layout | `styles/theme.scss` |
| Navigation and footer | `_quarto.yml` |

## Adding photos

Export as WebP at about 2000 px on the long edge **with location data removed**, put the file in `images/photos/`, and add a line to `photography.qmd`:

```markdown
![Caption](images/photos/new-photo.webp){group="photos" fig-alt="Short description"}
```

## Updating the CV

Copy the PDF from the CV pipeline (`output/academic_cv/Pham_CV_academic.pdf`) to `files/Pham_CV.pdf`.
