# Lockyer Valley — Flood Risk Assessment

Interactive web map published via GitHub Pages.

**Live map:** https://alberto98gallodot.github.io/LOCKYER-VALLEY/

## Overview
Flood risk assessment for Lockyer Valley LGA (Queensland) using the HAND (Height Above Nearest Drainage) model applied at two resolutions: 30m SRTM DEM and 5m LiDAR (Elvis Portal, Geoscience Australia — Toowoomba-Lockyer Valley 2015).

## Layers
- **Buildings at Risk — HAND Classification** — 26,260 building footprints classified by flood risk (High / Medium-High / Medium-Low / Low)
- **Building Comparison (30m vs 5m HAND)** — resolution comparison showing UPGRADED / UNCHANGED / DOWNGRADED buildings when moving from 30m to 5m DEM
- **Flood Risk Index (HAND 5m)** — dissolved flood risk polygons at 5m LiDAR resolution
- **Flood Risk Index (HAND 30m)** — dissolved flood risk polygons at 30m SRTM resolution
- **IQ QLD Floodplain Assessment Overlay** — official Queensland floodplain boundary (cross-validation reference)
- **Waterways** — drainage network context

## Methodology
HAND model computed in GRASS GIS (r.watershed → r.grow.distance). Risk classes based on height above nearest drainage:
- High: 0–5m
- Medium-High: 5–10m
- Medium-Low: 10–15m
- Low: >15m

Cross-validated against IQ QLD Floodplain Assessment Overlay — median HAND inside official floodplain = 2.03m, confirming 5m threshold captures 75% of flood-exposed buildings.

Resolution comparison: 30% of buildings upgraded, 54% unchanged, 16% downgraded when moving from 30m SRTM to 5m LiDAR.

## Data Sources
- DEM 5m LiDAR: Elvis Portal, Geoscience Australia (Toowoomba-Lockyer Valley 2015, entry 89644)
- DEM 30m: SRTM, Geoscience Australia
- Building footprints: Geoscience Australia — Queensland Building Footprints
- Floodplain overlay: IQ QLD Floodplain Assessment Overlay (Queensland Spatial)
- Waterways: OpenStreetMap

## Tools
QGIS 3.44 · GRASS GIS · QGIS2Web (Leaflet) · GitHub Pages

## Author
Alberto Gallo — GIS Analyst & Urban Planner
Graduate Member, Planning Institute of Australia (PIA)
