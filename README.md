# PH Data Center Heat Mapper

## Project Overview
Simulates cooling flow in a Port Harcourt data center using real PH weather, Nigeria climate indicators, and global DC sensor data. Ties materials eng (Fourier's law heat flux) to data pipelines. Built with Python/Pandas/Seaborn/ML.

## Data Sources
Blended VisualCrossing PH weather [https://www.visualcrossing.com/weather-history] + HDX Nigeria indicators [https://data.humdata.org/dataset/world-bank-climate-change-indicators-for-nigeria] + Kaggle DC sensors [https://www.kaggle.com/datasets/mbjunior/data-centre-hot-corridor-temperature-prediction] for realistic Rivers State sim. Filtered 2024-2025 for 300 rows: Date, Temp_C, Adj_Humidity_%, Nigeria_Precip_mm, Proxy_Factor, DC_T_out_C, Rack_ID, Heat_Flux_Wm2.

## Files
- ph_dc_heat_data.csv: Merged dataset (300 rows).
- notebook.ipynb: Analysis/viz/ML (coming).

## How to Run
See notebook for Pandas analysis, Seaborn heatmaps, ML hotspot prediction.