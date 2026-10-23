# Production Tracker — User Guide

The user guide for Quanta Magazine's **Production Tracker** (the Airtable system replacing the Asana board), built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/). All content is plain markdown under `docs/`, edited like the rest of the vault and published automatically to GitHub Pages.

## How it's organised

```
user-guide/
├── mkdocs.yml                     ← site config + the left-hand navigation
├── requirements.txt               ← the one dependency (mkdocs-material)
├── .github/workflows/deploy.yml   ← auto-publishes on every push to main
├── NEEDED-BEFORE-LAUNCH.md        ← the punch-list to finish the starter
└── docs/
    ├── index.md                   ← home page
    ├── assets/                    ← screenshots live here
    ├── stylesheets/extra.css      ← minor visual tweaks
    ├── getting-started/
    ├── pieces/
    ├── steps/
    ├── art/
    ├── alerts/
    └── admin/
```

## Editing content

Every page is a markdown file in `docs/`. To change wording, edit the file. To add a page, create the `.md` file and add one line to the `nav:` list in `mkdocs.yml`.

Writing style follows the house voice for client-facing material: plain English, second person, short sentences, prose over bullets, a worked example for each idea, no database jargon. Articles are task-based ("schedule a piece"), not table-based.

## Preview locally (optional)

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open <http://127.0.0.1:8000>. The preview reloads as you save.

## Publish (one-time setup)

1. Create a GitHub repo (`quanta-production-tracker-guide`) and push this folder to it.
2. In the repo, **Settings → Pages**, set **Source = GitHub Actions**.
3. Push to `main`. The workflow builds the site and publishes it at `https://<your-user>.github.io/<repo>/`.
4. Set that address as `site_url` in `mkdocs.yml`.

After that, every push to `main` rebuilds and republishes. The build runs `mkdocs build --strict`, so a broken internal link fails the build instead of shipping.

## Before launch

Work through `NEEDED-BEFORE-LAUNCH.md`: confirm the interface links, add the screenshots, and write the pages marked *Not written yet* once their screens are settled.
