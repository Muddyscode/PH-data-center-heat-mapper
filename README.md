# PH Data Center Heat Mapper

## Project Overview
First end-to-end data project: Simulates heat management in Port Harcourt's Equinix PR1 DC (Nigeria's southern digital gateway). Blends real PH weather (VisualCrossing), Nigeria climate (HDX), global DC sensors (Kaggle). Applies Fourier's law for flux, strains for humid/rain, analyzes trends, viz hotspots, ML predicts/alerts. Built for Rivers State's oil-to-data shift—entry data eng/science flex.

## Key Steps & Insights
- **Data Merge (Eng)**: 300 rows from 2024-25 PH dailies + benchmarks.
- **Sim (Eng)**: Effective Flux avg ~16000 Wm-2 (humid boosts 10-20%).
- **Analysis**: Rack 3 hottest (~18000 avg); humidity-flux corr 0.51.
- **Viz**: Heatmap shows Sep 2024 red zones; lines spike rainy months.
- **ML**: LinearReg R2 0.55; flagged 80+ hotspots (e.g., 2024-09-07 Rack 3: 21000 Wm-2—"Reroute!").

## Files
- `ph_dc_heat_data.csv`: Raw merged data.
- `simulated_dc_data.csv`: Post-sim/ML (Effective_Flux, Predicted_Flux, Hotspot_Flag).
- `heat_mapper_analysis.ipynb`: Full notebook (imports to ML).
- PNGs: flux_heatmap.png, monthly_flux_trends.png, rack_flux_trends.png, ml_predictions.png.

## Run It
1. Clone repo: `git clone https://github.com/Muddyscode/PH-data-center-heat-mapper.git`
2. Open in VS Code/Jupyter: `jupyter notebook heat_mapper_analysis.ipynb`
3. Tweak: Change k=200 in Fourier func for custom metals.

## Why PH DC? 
Equinix PR1 = game-changer for southern Nigeria (cable-linked, UBA-ready). This sim flags cooling risks—scale to real ops!

Built with Python/Pandas/Seaborn/Scikit-learn. Feedback? @amj_mykel on X.