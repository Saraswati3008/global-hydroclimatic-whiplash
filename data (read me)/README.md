# Data description

All gridded files cover 1980–2019 at 0.5° resolution with a monthly time step
(time format: YYYY-MM-DD). All variables were interpolated to the common 0.5° grid,
the native resolution of the coarsest dataset (G-RUN ENSEMBLE).

## pr_1980_2019_0.5degree.nc
Monthly precipitation used to identify wet and dry phases.
- Source: MSWEP v2.8, https://www.gloh2o.org/
- Variable: [precipitation] ([mm/per month])
- Resolution: 0.5°, monthly, 1980–2019
- Format: NetCDF
- Processing: interpolated to 0.5°, converted to monthly time step, and
  subset to the study period (1980–2019).

## runoff_1980_2019_0.5degree.nc
Monthly runoff used in the cause-effect whiplash definitions.
- Source: G-RUN ENSEMBLE, https://figshare.com/articles/dataset/G-RUN_ENSEMBLE/12794075
- Variable: [Runoff] ([mm/day])
- Resolution: 0.5°, monthly, 1980–2019
- Format: NetCDF
- Processing: subset to the study period (1980–2019). Native 0.5° grid, which
  was used as the reference grid for all other datasets.

## smrz_1980_2019_0.5degree.nc
Monthly root-zone soil moisture used in the cause-effect whiplash definitions.
- Source: GLEAM v4, https://www.gleam.eu/
- Variable: [smrz] (m3/m3)
- Resolution: 0.5°, monthly, 1980–2019
- Format: NetCDF
- Processing: interpolated to 0.5° and subset to the study period (1980–2019).

## water_stress_1980_2019.nc
Hydrological water stress, used to define the binary stress indicator for
Event Coincidence Analysis.
- Source: derived from GLEAM v4 actual evaporation (E) and potential
  evaporation (Ep), https://www.gleam.eu/
- Variable: ET/PET ratio (unitless). Lower values indicate stronger water
  limitation, where evaporative demand exceeds land-surface water supply.
- Resolution: 0.5°, monthly, 1980–2019
- Format: NetCDF
- Processing: GLEAM actual evaporation (E) and potential evaporation (Ep) are
  used as actual evapotranspiration (ET) and potential evapotranspiration
  (PET), respectively, as they represent the same processes. The ET/PET ratio
  was computed at each grid cell and month as an integrated diagnostic of
  vegetation water limitation and surface moisture availability.

## gdfc_events.json
Drought and flood event catalogue used to validate the whiplash definitions.
- Source: Global Drought and Flood Catalogue (GDFC),
  https://registry.opendata.aws/global-drought-flood-catalogue/
- Variables: event_id, event_type, indicator, continent, source, start_time,
  end_time, lat_min, lat_max, lon_min, lon_max
- Time format: YYYY-MM-DD HH:MM:SS
- Format: JSON (list of events)
- Processing: subset to 1980–2016, the period covered by the catalogue
  (events are available only until 2016).