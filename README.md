# Merkin_FinalProject

## Project Title: Predicting Transition Metal Oxide Stability

## Scientific Question

Which type of machine learning model is best for predicting transition metal oxide stability, and will adding structural features improve the prediction?

## Data

All data for this project comes from Materials Project API. Access is recieved through the notebooks.

[1]M. K. Horton et al., “Accelerated data-driven materials science with the Materials Project,” Nature Materials, July 2025, doi: 10.1038/s41563-025-02272-0.
[2]A. Jain et al., “Commentary: The Materials Project: A materials genome approach to accelerating materials innovation,” APL Materials, vol. 1, no. 1, p. 011002, July 2013, doi: 10.1063/1.4812323.

## Quick Start

### Prerequisites

- Conda (Miniconda or Anaconda)
- Git

### Installation

1. Clone the repository:
```bash
git clone https://github.com/benbenmerk-stack/Merkin_FinalProject.git
cd Merkin_FinalProject
```

2. Create the conda environment:
```bash
conda env create -f environment.yml
```

3. Activate the environment:
```bash
conda activate matds
```

4. Launch Jupyter Lab:
```bash
jupyter lab
```

## Project Structure

```
Merkin_FinalProject/
├── README.md                          # This file
├── environment.yml                    # Conda environment specification
├── .gitignore                         # Git ignore rules
├── notebooks/                         # Jupyter notebooks for analysis pipeline
│   ├── 01_data_acquisition.ipynb      # Fetch data from materials APIs
│   ├── 02_eda_featurization.ipynb     # Exploratory analysis & feature engineering
│   ├── 03_modeling.ipynb              # Model development & training
│   └── 04_results_visualization.ipynb # Results analysis & visualization
├── data/                              # Data directory
│   ├── README.md                      # Dataset documentation
│   └── *.csv                          # Processed datasets
└── figures/                           # Generated plots & visualizations

```

## Workflow

1. **Data Acquisition** (`01_data_acquisition.ipynb`): Retrieve materials data from Materials Project API
2. **EDA & Featurization** (`02_eda_featurization.ipynb`): Explore data distributions and featurize the dataset
3. **Modeling** (`03_modeling.ipynb`): Train and evaluate machine learning models
4. **Results & Visualization** (`04_results_visualization.ipynb`): Interpret results and create publication-quality figures


## Summary of Key Results

I compared random forests (shallow and medium), gradient boosting, and logistic regression models to predict binary transition metal oxide stability. Going by the AUC, the best model was a shallow random forest, at 0.7472. Overall all the models performed better than random, though they had fairly low R2s. I then tried a GroupKFold split by transition metal to look for leakage, and found R2 decreased even more, implying that materials with the same transition metal were influincing one another heavily in the ML model. Finally, I ran 5-fold CVs of both random split and GroupKFolds with and without structural features added, and found that structural features do result in an increase in R2 and a decrease in MAE for both kinds of splits. I also found that mean Mendeleev Number was the feature of highest importance in predicting material stability.

![AUC Results](figures/structural_R2_comparison.png)

## Resources

Copilot and ChatGPT were used in helping to generate and debug the code for this project.
