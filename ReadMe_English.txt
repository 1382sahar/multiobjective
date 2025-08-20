Multi-Objective Optimization and Classification Pipeline with Machine Learning
Overview
This project consists of several Python scripts implementing advanced machine learning workflows, including:

Multi-class classification with Gradient Boosting and ROC/AUC and Precision-Recall curve analysis.

Multi-objective optimization of regression targets using evolutionary algorithms (NSGA-II, NSGA-III, MOEAD) via the pymoo library.

Training XGBoost regressors on multiple target variables and optimizing solutions on Pareto fronts.

Single-target RandomForest regression with performance evaluation and visualization.

The overall goal is to enable detailed predictive modeling, evaluation, and optimization in problems with multiple outputs or classes.

Components
1. Multi-Class Classification and ROC/AUC Analysis
Load dataset from Excel with PCA features and multiclass target labels.

Binarize labels for multi-class ROC curve evaluation.

Train GradientBoostingClassifier on training data.

Compute and plot ROC curves and AUC values for each class.

Compute and plot Precision-Recall curves for each class.

Calculate micro-average AUC score and save results to Excel.

2. Multi-Objective Optimization of Multiple Regression Targets
Load dataset and select multiple continuous target variables (e.g., T4, T6, T8).

Define custom optimization problem using pymoo to minimize/maximize multiple objectives simultaneously.

Train XGBoost regressors on each target variable.

Run multi-objective evolutionary algorithms (NSGA-II, NSGA-III, MOEAD) to find Pareto optimal solutions.

Save optimization history and Pareto front results to Excel files.

Visualize results with interactive 3D or 2D Pareto front plots.

Zip output folders for easy download and sharing.

3. Two-Target Multi-Objective Optimization (2D Pareto Front)
Similar to the above, but for exactly two target variables.

Includes dedicated plotting and result saving functions.

4. Single Target RandomForest Regression and Evaluation
Load dataset with multiple targets and input features.

Loop over all targets, train separate RandomForest models.

Predict on full dataset, calculate metrics (RMSE, R², MAPE).

Save predictions and plots (actual vs predicted) for each target.

Save summary metrics for all targets in one Excel file.