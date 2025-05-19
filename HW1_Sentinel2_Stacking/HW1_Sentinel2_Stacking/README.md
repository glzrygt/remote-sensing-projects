# HW1 – Sentinel-2 Stacking & Spectral Analysis

This project was conducted as part of the GMT447 "Digital Image Processing" course at Hacettepe University.

## 📌 Objective
To process Sentinel-2 Level-2A imagery using Google Earth Engine (GEE) for:
- Cloud-filtered image selection
- Band resampling to uniform 10m resolution
- Stacking visible and NIR/SWIR bands
- Computing per-band statistics (mean, stdDev, min, max)
- Calculating covariance and manually-derived correlation matrices

## 🛰️ Data
- **Source**: Sentinel-2 Surface Reflectance (Level-2A)
- **Area**: Manavgat, Turkey
- **Platform**: Google Earth Engine

## 🔬 Analysis Steps
1. Filtering based on cloud cover and date
2. Resampling 20m bands to 10m
3. Band stacking using `.addBands()`
4. Covariance and correlation matrix derivation using `ee.Array` methods
5. Exporting the final image as GeoTIFF

## 📁 Files
- `report.pdf`: Assignment report
- `outputs/`: Example output images (figures from GEE)

## 🔗 Resources
- [GEE Script](https://code.earthengine.google.com/6059dacaed47780ea009305cd204a15b)
- [GEE Sentinel-2 Dataset](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR)

## 📌 Note
Correlation values revealed high redundancy among visible bands (e.g., Blue-Green: 0.86) and complementarity with SWIR bands (r ≈ 0.01), highlighting the spectral diversity and importance of combining bands in remote sensing tasks.
