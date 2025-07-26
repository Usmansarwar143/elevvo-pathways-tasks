# Loan Approval Prediction

## Overview
This repository contains the implementation of **Task 4** for my internship at **Elevvo Pathways**. The project focuses on building a machine learning model to predict loan approval based on a provided dataset, handling missing values, encoding categorical features, and addressing class imbalance. The models used are Logistic Regression and Decision Tree, with SMOTE applied to handle imbalanced data. Performance is evaluated using precision, recall, and F1-score.

## Repository Structure
- **Loan_Approval_Predictor.ipynb**: Jupyter Notebook containing the Python code for data preprocessing, model training, and evaluation.
- **requirements.txt**: List of Python dependencies required to run the notebook.
- **loan_approval_dataset.csv**: Dataset containing loan application data used for training and evaluation.

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Usmansarwar143/elevvo-pathways-tasks
   cd Task#04-Loan-Approval-Prediction
   ```
2. **Install Dependencies**:
   Ensure Python 3.8+ is installed, then install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Notebook**:
   - Open `Loan_Approval_Predictor.ipynb` in Jupyter Notebook or JupyterLab.
   - The dataset (`loan_approval_dataset.csv`) is included in the repository, so no additional data download is required. Ensure the notebook's file path points to `loan_approval_dataset.csv` in the repository root.
   - Run all cells to preprocess the data, train models, and view results.

## Dependencies
Listed in `requirements.txt`:
- pandas
- numpy
- scikit-learn
- imblearn

## Dataset
The repository includes `loan_approval_dataset.csv`, which contains the following columns:
- `loan_id`, `no_of_dependents`, `education`, `self_employed`, `income_annum`, `loan_amount`, `loan_term`, `cibil_score`, `residential_assets_value`, `commercial_assets_value`, `luxury_assets_value`, `bank_asset_value`, `loan_status`

The `loan_status` column is the target variable, indicating whether a loan application was approved or rejected.

## Methodology
- **Preprocessing**: Handles missing values (median for numerical, most frequent for categorical), encodes categorical features (`education`, `self_employed`), and scales numerical features.
- **Models**: Trains Logistic Regression and Decision Tree classifiers.
- **Class Imbalance**: Uses SMOTE to balance the dataset.
- **Evaluation**: Reports precision, recall, F1-score, and confusion matrices for both models, with and without SMOTE.

## Usage
- Run the notebook to train models and view performance metrics.
- The dataset is already included, but verify the file path in the notebook matches `loan_approval_dataset.csv` in the repository root.
- Results include confusion matrices and classification reports for model evaluation.

## Author
Created by Usman Sarwar as part of Task 4 for my internship at Elevvo Pathways.

## Contact
For any questions or feedback regarding this project, please reach out to:
- **Email**:muhammadusman.becsef22@iba-suk.edu.pk
- **LinkedIn**: htttps://www.linkedin.com/in/muhammad-usman-018535253
