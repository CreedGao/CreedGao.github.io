# creedgao.github.io

Personal academic website of Jiechao Gao — plain static HTML, no build step and no
external dependencies beyond a Google Fonts stylesheet.

## Layout

```
index.html          Home (about, research themes, selected work)
publications.html   Full publication list
collaboration.html  Collaboration
service.html        Professional service
awards.html         Awards & honors
news.html           News archive
research.html       Research detail page (not linked from the nav)
assets/
  style.css               single stylesheet for every page
  jiechao_gao_web.jpg     portrait
  favicon.svg
  fig_overview_layered.svg, fig_pipeline.svg
  Jiechao_Gao_CV.pdf      CV
  papers/*.pdf            local copies of selected papers
```

## Editing

Edit the HTML directly, or regenerate it from the source pipeline kept outside this
repo (`~/Desktop/faculty/网站/build/`, see `SPEC.md` there) and copy `site/` over the
repo root.

## Preview locally

```bash
python3 -m http.server 4007
```

Then open <http://localhost:4007>.

## Deploy

Pushing to `master` triggers `.github/workflows/deploy.yml`, which force-pushes the
repository contents to the `gh-pages` branch that GitHub Pages serves at
<https://creedgao.github.io>.
