# Global Hydroclimatic Whiplash

Code and processed data accompanying the manuscript
"Global Hydroclimatic Whiplash and Its Uneven Translation into Hydrological Water Stress"
(Debankana Bhattacharjee, Saraswati Harivenu Nair, Chandrika Thulaseedharan Dhanya, 2026).


## Overview
This repository contains the code used to detect, validate, and characterize
hydroclimatic whiplash events (1980–2019) and to assess their linkage with
hydrological stress using event coincidence analysis.

## Repository structure
- `code/` – analysis scripts
- `data (read me)/` –  – description of the processed datasets (`data (read me)/README.md`). The large
     NetCDF files are archived on Zenodo: [DOI to be added]
- `figures/` – final figures

## Requirements
Python 3.11. Main packages: numpy, pandas, xarray, scipy, matplotlib, cartopy, geopandas, json

## Input data (not included)
Download the original datasets from their sources (MSWEP and GLEAM require
free registration or a data request):

| Variable | Dataset | Version | Link |
|---|---|---|---|
| Precipitation | MSWEP | v2.8 | https://www.gloh2o.org/ |
| Runoff | G-RUN | ENSEMBLE | https://figshare.com/articles/dataset/G-RUN_ENSEMBLE/12794075 |
| Soil moisture | GLEAM | v4 | https://www.gleam.eu/ |
| Actual Evaporation | GLEAM | v4 | https://www.gleam.eu/ |
| Potential Evaporation | GLEAM | v4 | https://www.gleam.eu/ |
| Recorded Global Droughts and Flood Events | GDF Catalogue |  | https://registry.opendata.aws/global-drought-flood-catalogue/ |

## Running the code

Run the scripts in `code/` in the following order:

1. **`Global_Whiplash_Stress_Linkage`**
   Detects, characterizes, and validates hydroclimatic whiplash events globally
   (1980–2019) and links them to hydrological stress using Event Coincidence
   Analysis (ECA).
   - Input: [input datasets, e.g. precipitation, runoff, soil moisture, GDFC catalogue]
   - Output: [e.g. whiplash event datasets, ECA results saved in `data/`]

2. **`Results_Interpretations`**
   Uses the outputs of the first script to analyze the temporal and spatial
   evolution of whiplash events and their variation across climate zones,
   and to produce the main results and figures.
   - Input: outputs of `Global_Whiplash_Stress_Linkage`
   - Output: [e.g. figures saved in `figures/`]

## Archived version
[Zenodo DOI, add after you create the release]

## License
Code: MIT. Data: [license].

## Contact
[Saraswati Harivenu Nair, saraswatinair1999@gmail.com] 
