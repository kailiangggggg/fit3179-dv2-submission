# Beyond the Garden Gate

**FIT3179 Data Visualisation 2 — Topic 7: Australian Botanical Gardens**

[View Interactive Visualisation](https://kailiangggggg.github.io/fit3179-dv2-submission/)

## Project Overview

Beyond the Garden Gate is an interactive data visualisation exploring botanical gardens, plant collections, and wild seed origins across Australia.

The visualisation examines the distribution of registered botanical gardens and arboreta, the composition of selected botanical collection records, and the geographical origins of seed accessions. It also considers how these collections relate to botanical research, biodiversity conservation, and education.

The story highlights limitations in the available data, including incomplete geographic coordinates and collection dates.

## Visualisation

The website presents **13 visualisation groups** across four chapters:

1. **A National Footprint** — Distribution, population-adjusted comparisons, rankings, and registered facility sizes.
2. **Inside the Collections** — Living specimens, preserved herbarium records, and botanical collection composition.
3. **Beyond the Garden Gate** — Wild seed origins, accession records, and geographical and temporal data coverage.
4. **What the Evidence Means** — Key findings, conservation and education context, and limitations.

The visualisations are implemented using Vega-Lite, including three different map techniques and interactive filtering.

## Data Sources

The project uses publicly available data from:

- Geoscience Australia
- Australian Bureau of Statistics (ABS)
- Global Biodiversity Information Facility (GBIF)
- Atlas of Living Australia (ALA)

Information about data processing, source attribution, licences, and limitations is available in [Sources and Methods](docs/sources-and-methods.md).

## Technologies

- HTML, CSS and JavaScript
- Vega-Lite and Vega-Embed
- Vite
- Python for data preparation

## Running Locally

Requires Node.js 22 and pnpm.

```bash
pnpm install --frozen-lockfile
pnpm run dev
```

To validate the visualisation specifications and build the website:

```bash
pnpm run validate:specs
pnpm run test:site
pnpm run build
```

The Vega-Lite specifications are located in `public/specs/`, and the processed datasets are available in `public/data/`.

## Project Information

Developed for FIT3179 Data Visualisation 2, Monash University Malaysia.

The original development repository and history are retained in the [project repository](https://github.com/kailiangggggg/fit3179-dv2-botanical-gardens).
