# cteli-27-13001506-DE-JS

Seismological data pipeline that loads miniSEED files into a normalized SQLite database and displays an interactive dashboard in Google Colab.

## Project Requirements

- Create a Google Colab notebook
- Read miniSEED files
- Create a database in normal form with constraints
- Display the data in a dashboard

## What This Notebook Does

1. Downloads the three miniSEED files (`SEP01.mseed`, `SEP02.mseed`, `SEP03.mseed`) from the USGS-related repository.
2. Creates a three-table SQLite schema (`networks`, `stations`, `traces`) with primary keys, foreign keys, unique constraints, and check constraints.
3. Loads every trace (one row per continuous channel segment) into the database.
4. Enriches station metadata (latitude, longitude, elevation, site name) from the EarthScope FDSN station service.
5. Builds an interactive dashboard containing:
   - Metadata summary table
   - Helicorder-style dayplots for each file
   - Map of station locations (including HOA and SUG)

## How to Run

1. Open the notebook in Google Colab:
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/moistvonlipwig/cteli-27-13001506-DE-JS/blob/main/cteli_27_13001506_DE_JS.ipynb)
2. Run all cells from top to bottom.
3. The dashboard appears at the end of the notebook.

No additional files are required; the miniSEED data is downloaded automatically.
