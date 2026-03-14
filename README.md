E-Waste Management – Recoverability Classification

Project Overview

Electronic waste (E-waste) contains valuable metals that can potentially be recovered through recycling. However, not all discarded electronic components are economically viable for recovery.

This project develops a machine learning classification model that predicts whether an electronic component is recoverable or non-recoverable based on its material composition data.

Problem Statement

Classify discarded electronic components as recoverable or non-recoverable using material composition data.
Evaluate the model using overall classification accuracy and fine-tune the model parameters to improve prediction performance.

Dataset

Dataset used:
- e_waste_cleaned_recoverable.csv

The dataset contains electronic components with their material composition values.

A target variable 'Recoverable' is used for classification:

- 1 → Recoverable
- 0 → Non-Recoverable

Project Workflow

1. Data Preprocessing

- Handling missing values using median imputation
- Validating numerical data types
- Removing outliers using the Interquartile Range (IQR) method

2. Feature Engineering

- Calculated the total economic value of metals in each component.
- Created the Recoverable classification label based on value distribution.

3. Model Training

- The dataset was split into training and testing sets (80–20 split).
- Model: Random Forest Classifier

4. Model Evaluation

Models were evaluated using:

- Confusion Matrix
- Classification Report
- Precision
- Recall
- F1 Score
- Overall Accuracy

5. Model Fine-Tuning

Hyperparameter tuning was performed using GridSearchCV with 5-fold cross validation.

Parameters optimized:

- Number of trees (n_estimators)
- Maximum depth (max_depth)
- Minimum samples split (min_samples_split)
- Minimum samples per leaf (min_samples_leaf)

6. Final Model Performance

Final model: Random Forest Classifier

Performance metrics:

- Accuracy: 97.9%
- Precision: ~0.98
- Recall: ~0.95 – 0.99
- F1 Score: ~0.97 – 0.98

The model successfully classifies electronic components as recoverable or non-recoverable based on material composition.

7. Project Structure

E-WASTE-RECYCLABILITY-MAIN
├── e_waste_cleaned_recoverable.csv
├── e_waste_dataset_with_profit.csv
├── EvaluationandFineTuning.ipynb
├── finalclassification.ipynb
├── README.md

8. Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

## The master branch of the repository stores the Final Project.
