# Task 1: Student Score Prediction

## Overview
This project is part of my Machine Learning internship task at Elevvo Pathways, an Egypt-based company. It aims to predict students' exam scores based on relevant features from the *Student Performance Factors* dataset using linear and polynomial regression models. The project includes data cleaning, exploratory data analysis, visualization, model training, and performance evaluation using Python, Pandas, Matplotlib, Seaborn, and Scikit-learn.

## Dataset
The dataset used is `StudentPerformanceFactors.csv`, sourced from Kaggle. It contains various features influencing student performance, but this project focuses on `Hours_Studied` and `Previous_Scores` to predict `Exam_Score`.

## File Structure
```
Task#01-Student_Score_Prediction/
├── Output/
│   ├── hours_studied_vs_score.png
│   ├── previous_scores_vs_score.png
│   ├── linear_regression_predictions.png
│   ├── polynomial_regression_predictions.png
├── Student_Score_Predictor.ipynb
├── StudentPerformanceFactors.csv
├── README.md
```

- **Output/**: Folder containing visualization outputs as PNG files.
- **Student_Score_Predictor.ipynb**: Jupyter Notebook with the complete code for data cleaning, visualization, and model training/evaluation.
- **StudentPerformanceFactors.csv**: The dataset used for analysis and modeling.
- **README.md**: This file, providing project details and instructions.

## Features
- **Data Cleaning**: Handles missing values by dropping rows with null entries.
- **Exploratory Data Analysis**: Includes descriptive statistics and scatter plots for `Hours_Studied` and `Previous_Scores` vs. `Exam_Score`.
- **Modeling**: Implements linear regression and polynomial regression (degree 2) to predict exam scores.
- **Evaluation**: Uses Mean Squared Error (MSE) and R² score to compare model performance.
- **Visualization**: Generates plots for data exploration and model predictions, saved in the `Output` folder.

## Prerequisites
To run the project, ensure you have the following installed:
- Python 3.8+
- Jupyter Notebook or JupyterLab
- Required Python libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Usmansarwar143/elevvo_pathways_tasks
   cd Task-01-Student_Score_Prediction
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

## Usage
1. Open `Student_Score_Predictor.ipynb` in Jupyter Notebook.
2. Ensure `StudentPerformanceFactors.csv` is in the same directory as the notebook.
3. Run all cells in the notebook to:
   - Load and clean the dataset.
   - Generate exploratory visualizations.
   - Train and evaluate linear and polynomial regression models.
   - Save visualizations to the `Output` folder.
4. Check the `Output` folder for the generated PNG files:
   - `hours_studied_vs_score.png`: Scatter plot of Hours Studied vs. Exam Score.
   - `previous_scores_vs_score.png`: Scatter plot of Previous Scores vs. Exam Score.
   - `linear_regression_predictions.png`: Linear regression predictions.
   - `polynomial_regression_predictions.png`: Polynomial regression predictions.

## Model Details
- **Linear Regression**: Predicts `Exam_Score` using `Hours_Studied` and `Previous_Scores`.
- **Polynomial Regression**: Uses degree 2 polynomial features for improved fit on non-linear relationships.
- **Evaluation Metrics**:
  - Mean Squared Error (MSE): Measures average squared difference between predicted and actual scores.
  - R² Score: Indicates the proportion of variance in `Exam_Score` explained by the model.

## Results
The notebook outputs:
- Descriptive statistics of the dataset.
- MSE and R² scores for both models.
- Visualizations saved in the `Output` folder for easy reference.

## Bonus
The project includes a polynomial regression model (degree 2) to compare performance with linear regression, providing insights into which model better captures the relationship between features and exam scores.

## Contributing
Feel free to fork the repository, make improvements, and submit pull requests. For major changes, please open an issue to discuss proposed updates.

## Contact
For any questions or feedback regarding this project, please reach out:
- [Email](mailto:muhammadusman.becsef22@iba-suk.edu.pk)
- [LinkedIn](https://www.linkedin.com/muhammad-usman-018535253/)
- For more information about the company, visit [Elevvo Pathways LinkedIn Profile]([https://www.elevvo-pathways.com](https://www.linkedin.com/company/elevvopaths/posts/?feedView=all)


## Acknowledgments
- Dataset sourced from Kaggle: *Student Performance Factors*.
- Built as part of my Machine Learning internship at Elevvo Pathways, an Egypt-based company.
- Built using Python, Pandas, Matplotlib, Seaborn, and Scikit-learn.
