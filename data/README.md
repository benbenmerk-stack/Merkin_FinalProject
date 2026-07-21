# Data Directory

## Dataset Documentation

This directory contains processed datasets used in the materials science analysis pipeline. All raw data should be sourced from external APIs and not committed to this repository if larger than 50 MB.

### Datasets

| Filename | Source | Description | Size | Status |
|----------|--------|-------------|------|--------|
| | | | | |

*Add entries as datasets are acquired and processed.*

## Data Sources

### External APIs & Databases

- **Materials Project API** (`mp-api`): Crystal structure and property data for inorganic materials
- **JARVIS** (`jarvis-tools`): Joint Automated Repository for Various Integrated Simulations
- **Matminer** (`matminer`): Materials informatics feature generation and descriptors

### Data Acquisition

All data is fetched programmatically in `../notebooks/01_data_acquisition.ipynb` using API credentials stored in `.env` (not committed).

## Processing Notes

- Raw CSV files are processed in `02_eda_featurization.ipynb`
- Missing values and outliers are handled according to domain-specific criteria
- Feature engineering and scaling applied as documented in the featurization notebook

## Figures

Generated plots and visualizations are saved in the `figures/` subdirectory with descriptive names indicating the analysis step and content (e.g., `02_correlation_heatmap.png`, `03_model_performance_comparison.png`).
