# Car Insurance Prediction Project

## Project Overview
This project implements and compares multiple machine learning models to predict customer interest in car insurance based on various customer attributes. The project uses data from a health insurance provider looking to expand into car insurance.

## Key Features
- Comprehensive data exploration and visualization
- Data preprocessing including handling missing values and outlier removal
- Feature selection using chi-square test and Pearson correlation
- Implementation of three different models:
  - XGBoost
  - Random Forest
  - K-Nearest Neighbors (KNN)
- Handling of imbalanced data using techniques like SMOTEENN and SMOTENC
- Comparative analysis of model performance

## Data
The project uses a dataset provided by a health insurance company, containing customer information and their interest in car insurance. Key features include customer demographics, driving history, and current insurance details.

## Methodology
1. Data Exploration:
   - Analysis of missing values and feature distributions
   - Visualization of feature relationships and outliers

2. Data Preprocessing:
   - Handling missing data using iterative imputation
   - Outlier removal using IQR method
   - Feature scaling for 'AnnualPremium' and 'Age'
   - Encoding of categorical variables

3. Feature Selection:
   - Chi-square test for categorical features
   - Pearson correlation for numerical features

4. Model Implementation:
   - XGBoost, Random Forest, and KNN models
   - Hyperparameter optimization using RandomizedSearchCV

5. Handling Imbalanced Data:
   - Comparison of SMOTEENN, SMOTENC, and class weights

6. Model Evaluation:
   - Use of PR-AUC and ROC-AUC metrics
   - K-Fold Cross Validation

## Results
Performance metrics for the best performing models:

| Model | PR-AUC | ROC-AUC | Cohen's Kappa |
|-------|--------|---------|---------------|
| XGBoost | 0.600 | 0.775 | 0.248 |
| Random Forest | 0.559 | 0.763 | 0.288 |
| KNN | 0.502 | 0.718 | 0.256 |

XGBoost demonstrated the best overall performance, followed by Random Forest. KNN showed the lowest performance among the three models.

## Repository Structure
- `data/`: Contains the dataset
- `notebooks/`: Jupyter notebooks for data analysis and model implementation
- `src/`: Source code for data preprocessing and model implementation
- `results/`: Output files and figures
- `requirements.txt`: List of required Python packages

## Usage
1. Clone the repository
2. Install the required packages: `pip install -r requirements.txt`
3. Run the Jupyter notebooks in the `notebooks/` directory for step-by-step analysis and model implementation

## Future Work
- Exploration of more advanced feature engineering techniques
- Testing of additional machine learning models
- Further optimization of model hyperparameters
- Investigation of deeper insights into feature importance and model interpretability

## Contributors
- Eshaq Rahmani

## Acknowledgments
- The health insurance company for providing the dataset
- The scikit-learn, XGBoost, and imbalanced-learn development teams for their excellent libraries