# Dublin Beauty Services — Flyer Targeting Map

An interactive web map of around 800 beauty businesses across Dublin, built to find the densest street-level clusters of beauty-conscious foot traffic for targeted flyer distribution.

Freelance project for **HILO**, a beauty app.

### 🔗 [View the live interactive map →](https://conorfahy99.github.io/dublin-beauty-flyer-map/)

*(Click pins for business details, toggle layers on/off, and zoom to street level.)*

---

## What it shows

The map plots every salon, beauty college, and training academy in Dublin as colour-coded pins, then overlays a density analysis to reveal where these businesses cluster tightest.

| Layer | Count | Purpose |
|---|---|---|
| Salons | ~780 | Nail bars, hair, makeup, lash & brow, waxing, tanning, non-medical clinics |
| Beauty colleges | 10 | Accredited QQI beauty / aesthetics providers |
| Training academies | 13 | Private short-course providers (lash, nails, brows, makeup) |

A **buffer-overlap hotspot layer** counts how many businesses fall within 300 m of each other — areas with four or more overlapping buffers are genuine tight clusters, not smeared district-level blobs. A **transport-stop overlay** (bus, Luas, DART) highlights where dense clusters meet high-footfall transit, the strongest candidate spots for handing out flyers.

## Why it was built

There's no historical flyer-uptake data, so the map uses **business density as a proxy for audience concentration**. The goal is operational: identify the specific streets and junctions where a flyer is most likely to reach someone already engaged with the beauty industry.

## Method

| Stage | Tools |
|---|---|
| Data collection | Overpass Turbo (OSM salon data), manual research for colleges/academies |
| Build & styling | QGIS desktop, category-split point layers |
| Hotspot analysis | 300 m fixed-radius buffers, dissolved and counted by overlap |
| Transport overlay | TFI / data.gov.ie open data (bus, Luas, DART stops) |
| Web export | qgis2web → Leaflet |
| Hosting | GitHub Pages |

Source data is in this repo (`dublin_beauty_businesses_clipped.csv`), along with the hotspot and prime-zone outputs as GeoJSON and shapefile.

## Tech

QGIS · OpenStreetMap / Overpass · Leaflet · GitHub Pages
