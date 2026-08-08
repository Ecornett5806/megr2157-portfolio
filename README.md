# MEGR 2157 – Design Portfolio Template

This repository is an MkDocs site (same engine Fab Academy uses) with the Analyze / Decide / Communicate framework built into every assignment page. The rendered site — with the left-hand navigation to every assignment — lives in `docs/`; this README is just for people working with the repo itself.


## Don't do, possible save for later. Preview locally

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open http://127.0.0.1:8000 in your browser. The sidebar nav updates automatically from `mkdocs.yml`.

## Publish

Push to `main` — the included GitHub Actions workflow (`.github/workflows/deploy.yml`) builds the site and publishes it to GitHub Pages automatically.

## Structure

```
mkdocs.yml                  <- controls the site nav (the left sidebar)
docs/
  index.md                  <- site homepage
  portfolio-overview.md     <- running index of assignments
  assignments/
    a1/index.md
    a2-truss-stress/index.md
    a3/index.md
    a4/index.md
    a5/index.md
    a6/index.md
    a7/index.md
    a8/index.md
    a9/index.md
    ?a9x-concept-selection/index.md   <- Pugh matrix: gear vs. pulley vs. lead screw
    a10/index.md
templates/
  assignment-template.md    <- blank copy for reference, not part of the published site
```

## Adding or renaming an assignment

1. Add a new folder under `docs/assignments/` with an `index.md`.
2. Add a matching line to the `nav:` section of `mkdocs.yml` — this is what makes it appear in the sidebar on every page.
