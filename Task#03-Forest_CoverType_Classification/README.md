# Task 03: Forest Cover Type Classification

## Overview
This project is part of my internship at **Elevvo Pathways** (Task 03), focusing on multi-class classification to predict forest cover types using the UCI Covertype dataset. The goal is to classify forest cover into one of seven types based on cartographic and environmental features, leveraging tree-based models (Random Forest and XGBoost). The project includes data preprocessing, model training with hyperparameter tuning, evaluation, and visualization of results through confusion matrices and feature importance plots.

## File Structure
```
Task#03-Forest_CoverType_Classification/
├── Output/
│   ├── rf_Confusion_Matrix.png
│   ├── xgb_Confusion_Matrix.png
│   ├── rf_Feature_Importance.png
│   ├── xgb_Importance.png
├── Forest_Cover_Type_Classification.ipynb
├── covtype.rar
├── README.md
```

- **Output/**: Contains four PNG files visualizing model performance:
  - `Random_Forest_Confusion_Matrix.png`: Confusion matrix for Random Forest model.
  - `XGBoost_Confusion_Matrix.png`: Confusion matrix for XGBoost model.
  - `Random_Forest_Feature_Importance.png`: Feature importance plot for Random Forest.
  - `XGBoost_Feature_Importance.png`: Feature importance plot for XGBoost.
- **Forest_Cover_Type_Classification.ipynb**: Jupyter notebook with the complete code for data preprocessing, model training, evaluation, and visualization.
- **covtype.rar**: Compressed dataset file (Covertype dataset, ~200MB uncompressed) due to its large size.
- **README.md**: This file, providing project details and instructions.

## Dataset
The **UCI Covertype dataset** contains 581,012 samples with 54 features, predicting one of seven forest cover types. Features include:
- **Numerical (10)**: Elevation, Aspect, Slope, distances to hydrology/roads/fire points, hillshade indices.
- **Categorical (44)**: Binary indicators for 4 wilderness areas and 40 soil types.
- **Target**: `Cover_Type` (1 to 7, representing forest types like Spruce/Fir, Lodgepole Pine, etc.).

The dataset is provided as `covtype.rar` due to its size. Uncompress it to access the data (or use the `ucimlrepo` library to fetch it directly).

## Setup
### Prerequisites
- Python 3.8+
- Libraries: Install via `pip install -r requirements.txt` or:
  ```bash
  pip install pandas numpy scikit-learn xgboost matplotlib seaborn ucimlrepo
  ```

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Usmansarwar143/elevvo-pathways-tasks
   cd Task#03-Forest_CoverType_Classification
   ```
2. Uncompress `covtype.rar` to access the dataset (optional if using `ucimlrepo`).
3. Install dependencies (see above).
4. Open `Forest_Cover_Type_Classification.ipynb` in Jupyter Notebook or JupyterLab:
   ```bash
   jupyter notebook Forest_Cover_Type_Classification.ipynb
   ```

## Usage
1. **Run the Notebook**:
   - Execute all cells in `Forest_Cover_Type_Classification.ipynb`.
   - The notebook:
     - Fetches the dataset using `ucimlrepo` (or uses the uncompressed `covtype.rar` if modified).
     - Preprocesses data (scales numerical features, handles XGBoost label mapping from 1-7 to 0-6).
     - Trains Random Forest and XGBoost models with `RandomizedSearchCV` (optimized for speed with 10% subsampling, `n_iter=2`, `cv=2`).
     - Evaluates models with accuracy and classification reports.
     - Generates and saves four plots to the `Output/` folder.

2. **Key Features**:
   - **Preprocessing**: Scales numerical features using `StandardScaler`; categorical features are pre-encoded.
   - **Models**: Random Forest and XGBoost with hyperparameter tuning.
   - **Optimizations**: Subsampling (10% of data), reduced hyperparameter grid, and `RandomizedSearchCV` for faster runtime.
   - **Visualizations**: Confusion matrices and feature importance plots for both models.

3. **Output**:
   - Console: Prints best hyperparameters, accuracy, and classification reports.
   - Files: Saves four PNGs in `Output/` (see File Structure).

## Results
- **Performance**: Achieved ~75-80% accuracy on a 10% subsampled dataset, with XGBoost slightly outperforming Random Forest.
- **Key Features**: Elevation and specific soil types were among the most important predictors.
- **Visualizations**: Confusion matrices show strong performance for common classes (e.g., types 1 and 2), with some misclassification for rarer classes. Feature importance plots highlight influential features.
- **Challenges Overcome**:
  - Fixed XGBoost `ValueError` by mapping `Cover_Type` labels from 1-7 to 0-6.
  - Optimized runtime by subsampling and streamlining hyperparameter tuning.

## Notes
- **Runtime**: The notebook runs in ~5-10 minutes on a standard machine (8-core CPU, 16GB RAM) due to optimizations.
- **Improvements**:
  - Increase subsample size (e.g., 20%) for better accuracy at the cost of longer runtime.
  - Explore LightGBM for faster training.
  - Address class imbalance using SMOTE or class weights for improved performance on rare classes.
- **Dependencies**: Ensure the latest XGBoost version (`pip install xgboost --upgrade`) to avoid deprecated parameters.
- **Dataset Access**: If `covtype.rar` is used, uncompress it and modify the notebook to load the local file (replace `ucimlrepo` code).

## Acknowledgments
- **Elevvo Pathways**: For providing this internship opportunity and guidance.
- **UCI Machine Learning Repository**: For the Covertype dataset.

For questions or contributions, please open an issue or contact me via [LinkedIn](<your-linkedin-profile>).
