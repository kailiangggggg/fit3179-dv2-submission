# Beyond the Garden Gate

FIT3179 Data Visualisation 2 · Topic 7 · Australian botanical gardens

- **Published website:** https://kailiangggggg.github.io/fit3179-dv2-submission/
- **Repository:** https://github.com/kailiangggggg/fit3179-dv2-submission

This is an independent release snapshot of the production site at source commit `b0c46dbf54fc015054f9953f832f16ad7ca3f781`, taken from [the original repository](https://github.com/kailiangggggg/fit3179-dv2-botanical-gardens). It is not a copy of the original development history; that repository remains intact. The page retains the author and snapshot date in its footer.

## Run and validate

Use Node.js 22 and pnpm 11.25.0.

```powershell
pnpm install --frozen-lockfile
pnpm run dev
pnpm run validate:specs
pnpm run test:site
pnpm run build
pnpm run preview
```

The production build is written to `site-dist/`. GitHub Actions builds and deploys that directory to GitHub Pages when `main` is updated.

## Charts, data and sources

The site contains 13 chart groups, three distinct map idioms, and human-readable Vega-Lite v5 specifications in `public/specs/`. The processed data required by the charts is in `public/data/` (about 1.2 MB). Charts use local specifications and data rather than a third-party runtime data API.

Sources, licences, filters, limitations and data-preparation methods are documented in [`docs/sources-and-methods.md`](docs/sources-and-methods.md). Font licence texts are included under [`licenses/fonts/`](licenses/fonts/).

Raw source archives are not included in this public snapshot. For local reproduction, acquire the allowlisted inputs into a sibling `data/raw` directory, then verify and prepare them:

```powershell
python -m pip install -r requirements.txt
python -m scripts.fetch_sources --raw-root ..\data\raw
python -m scripts.fetch_sources --verify-only --raw-root ..\data\raw
python -m scripts.prepare_data --raw-root ..\data\raw --output-dir public\data
pnpm run test:data
```

The committed chart-ready files reflect the 14 October 2026 source snapshot. New upstream archives may differ; compare input hashes with `public/data/source_provenance.json` before replacing committed results. The fetch script preserves existing snapshots rather than overwriting them.

This repository packages the website release only. The hand-drawn Topic 7 sketch PDF and Moodle submission are separate student-owned materials and are not included here.
