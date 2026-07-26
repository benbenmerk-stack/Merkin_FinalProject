# Data Directory


## Datasets
cleaned_tm_oxides.json
- Structural data saved in a .json for future use

tm_oxygen_binary_compounds.csv
- MP Dataset of binary transition metal oxides, fetched externally

tm_oxygen_binary_compounds_magpie_features.csv
- Binary transition metal oxide dataset featurized with Magpie using Matminer

magpie_feature_names.txt
- List of 132 Magpie features
  
stability_classification_results.csv
- Test results from the four different models

random_magpie_structure_predictions.csv
- Predictions vs actual of randomly split magpie + structure data saved for parity plot

model_comparison_results
- Comparison table of R2 and MAE for random split vs GroupKFold, with and without structural features added

importances.csv
- Importances data for use in plotting

four_model_results_table.csv
- Accuracy, F1 Score, AUC, Precision, and Recall for the four models

## Data Sources

- **Materials Project API** (`mp-api`): Crystal structure and property data for inorganic materials
- **Matminer** (`matminer`): Materials informatics feature generation and descriptors

## Data Acquisition

All data is fetched programmatically in `../notebooks/01_data_acquisition.ipynb` using API credentials stored in `.env` (not committed).