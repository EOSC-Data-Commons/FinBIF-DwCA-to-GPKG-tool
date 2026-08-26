# DwCA to GeoPackage Converter

A Python script that converts Darwin Core Archive (DwCA) biodiversity data to GeoPackage format for use in GIS applications.

## Overview

This tool:
- Downloads DwCA archives from GBIF (Global Biodiversity Information Facility)
- Extracts occurrence records with spatial data
- Converts WKT geometry strings to spatial objects
- Handles mixed geometry types by converting them to compatible formats
- Saves the result as a GeoPackage file (GPKG)

## Requirements

- Python 3.x
- geopandas
- pandas
- shapely
- requests

Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. Open `process_dwca.ipynb` in Jupyter or VS Code
2. Update the `collection_id` in Step 2 to your desired GBIF collection. The collection IDs are the same as collection IDs in [https://laji.fi/en/theme/dataset-metadata]('https://laji.fi/en/theme/dataset-metadata').
3. Run all cells in sequence
4. Output will be saved as `HR_7580.gpkg` (or `{collection_id}.gpkg`)

## Output

The output GeoPackage file contains:
- All occurrence records from the archive
- Original data columns
- Spatial geometry column (WGS84 CRS)
- Compatible geometry types for GIS software

## Files

- `process_dwca.ipynb` - Main processing script
- `requirements.txt` - Python dependencies
- `HR_7580.gpkg` - Generated output file
