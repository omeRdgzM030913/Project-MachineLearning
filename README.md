# Project-MachineLearning
This repository showcases a complete application of Machine Learning techniques (supervised and unsupervised) to classify and segment patients with respect to diabetes. It starts from a Kaggle dataset containing medical variables to efficiently predict and group diabetes cases.

Project Overview

Data Loading and Preparation
A dataset with multiple variables (e.g. number of pregnancies, glucose level, etc.) is used along with a binary Outcome (diabetic/non-diabetic).
Cleaning and normalization of numerical attributes:
MinMaxScaler to transform values ​​in the range [0,1].
StandardScaler for data with a near-normal distribution.

Exploratory Analysis and Visualization
Histograms of each variable to understand its distribution and identify outliers.
Heatmap to evaluate the correlation between attributes.
t-SNE (dimensionality reduction) to visualize, in 2D, the distribution of instances with respect to their characteristics.

Supervised Learning: Classification
Data separation (Train/Test) using 80% for training and 20% for testing.
Decision Tree:
Hyperparameter search via GridSearchCV (criterion, max_depth, etc.).
Accuracy and F1 metrics in train and test to detect possible overfitting problems.
Confusion matrix and classification report (precision, recall, F1).
Random Forest:
Extends the logic of the Decision Tree with n_estimators and the importance of similar hyperparameters.
Comparison of results vs. Decision Tree, measuring the performance and robustness gain.

Unsupervised Learning: Clustering
K-Means:
Calculation of SSE (Sum of Squared Errors) and Silhouette Coefficient to determine the optimal number of clusters.
Use of the KneeLocator (elbow method) and the silhouette method for the final selection of K.
Comparison of the predicted labels with the Outcome variable (although in clustering there are no real labels, it is done in an exploratory manner).
Gaussian Mixture Models (GMM):
BIC criterion to compare model adequacy at different K values.
Analysis of cluster consistency via the silhouette coefficient.
Observation of patterns in variable subsets (e.g. Glucose, Pregnancies, etc.).

Evaluation and Metrics
Accuracy and F1-Score for the supervised part, with cross-validation by GridSearchCV in the case of Decision Trees.
Confusion Matrix and classification_report to evaluate imbalance in classes (diabetes vs. non-diabetes).
Silhouette coefficient and BIC for unsupervised algorithms, allowing to discern the cohesion and separation of clusters.



With these steps, this project demonstrates competencies in feature engineering, predictive modeling, clustering, and the ability to optimize classification and segmentation methods in Python. It also highlights the ability to analyze and communicate results clearly, supported by metrics and visualizations that guide decision making.
