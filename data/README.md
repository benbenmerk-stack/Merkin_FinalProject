# Data Directory


## Datasets

tm_oxygen_binary_compounds.csv
- MP Dataset of binary transition metal oxides, fetched externally

tm_oxygen_binary_compounds_magpie_features.csv
- Binary transition metal oxide dataset featurized with Magpie using Matminer

stability_classification_results.csv
- Test results from the four different models

magpie_feature_names.txt
- List of 132 Magpie features

final_results_table.csv
- Accuracy, F1 Score, AUC, Precision, and Recall for the four models

## Data Sources

- **Materials Project API** (`mp-api`): Crystal structure and property data for inorganic materials
- **Matminer** (`matminer`): Materials informatics feature generation and descriptors

## Data Acquisition

All data is fetched programmatically in `../notebooks/01_data_acquisition.ipynb` using API credentials stored in `.env` (not committed).