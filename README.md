# 🏦 Enhanced Bank Marketing Prediction Pipeline

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn%20|%20LightGBM-orange)
![License](https://img.shields.io/badge/License-MIT-green)

An advanced End-to-End Machine Learning pipeline designed to predict whether a bank client will subscribe to a term deposit. This project leverages **Decision Trees**, **Random Forests**, and **LightGBM** to compare performance, supported by comprehensive data visualization and feature analysis.

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Dataset](#-dataset)
- [Installation](#-installation)
- [Model Performance](#-model-performance)
- [Visualizations](#-visualizations)
- [Project Structure](#-project-structure)

---

## 🔭 Project Overview
The goal of this project is to analyze the "Bank Marketing" dataset and build a robust predictive model. Unlike standard implementations, this pipeline focuses heavily on **interpretability** and **comparative analysis**, providing deep insights into which features drive customer decisions.

The pipeline performs:
1.  **Data Preprocessing:** Label encoding and stratified splitting.
2.  **EDA:** Distribution analysis and correlation heatmaps.
3.  **Modeling:** Training three distinct classifiers (Decision Tree, Random Forest, LightGBM).
4.  **Evaluation:** Generating ROC Curves, Precision-Recall Curves, and Confusion Matrices.

---

## 🌟 Key Features
* **Multi-Model Comparison:** Side-by-side performance metrics for DT, RF, and LightGBM.
* **Advanced Visualizations:** * Interactive-style Correlation Heatmaps.
    * Feature Importance rankings across models.
    * Learning Curves to diagnose overfitting/underfitting.
* **Robust Preprocessing:** Handles categorical data encoding and binary target mapping automatically.

---

## 📊 Dataset
The dataset used is the **Bank Marketing Data Set** from the UCI Machine Learning Repository.
* **Input:** Client info (age, job, marital status), campaign details (calls, duration), and economic indicators.
* **Target:** `y` (has the client subscribed to a term deposit? 'yes'/'no').

> **Note:** The dataset `bank-additional.csv` must be placed in the root directory.

---

## ⚙️ Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/omairhere/bank-marketing.git
    cd bank-marketing
    ```

2.  **Install dependencies:**
    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn lightgbm
    ```

3.  **Run the pipeline:**
    ```bash
    python main.py
    ```

---

## 🏆 Model Performance

The following table summarizes the performance of the three models on the test set:

| Model | Accuracy | Precision | Recall | F1-Score | AUC |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Decision Tree** | 88.5% | 0.48 | 0.51 | 0.49 | 0.72 |
| **Random Forest** | 91.2% | 0.65 | 0.42 | 0.51 | 0.93 |
| **LightGBM** | **91.8%** | **0.67** | **0.54** | **0.60** | **0.94** |

*(Note: Actual results may vary slightly based on random seed).*

---

## 📈 Visualizations

### 1. Exploratory Data Analysis
Understanding the target class balance and feature correlations.

<img width="1268" height="490" alt="target_class_proportion" src="https://github.com/user-attachments/assets/529f9115-1eee-4866-9ef3-d0076c1a354e" />
*Figure 1: Target Class Distribution showing dataset imbalance.*

<img width="1109" height="1016" alt="feature_correlation_heatmap" src="https://github.com/user-attachments/assets/0cb70f77-8c75-43e7-b95f-72b1b781b75e" />
*Figure 2: Correlation Heatmap of top features.*

### 2. Model Evaluation
Comparing how well the models separate positive and negative classes.

<img width="989" height="789" alt="roc_curve_comparison" src="https://github.com/user-attachments/assets/0682ebf6-9589-4a13-9f33-6a3fe39779d2" />
*Figure 3: ROC Curve Comparison indicating LightGBM's superior AUC.*

<img width="1389" height="690" alt="model_performance_comparison" src="https://github.com/user-attachments/assets/9540f459-4db6-4473-b109-ceb663c9bb41" />
*Figure 4: Side-by-side metric comparison.*

### 3. Feature Importance
What drives a customer to say "Yes"?

<img width="1789" height="590" alt="all_models_feature_importance" src="https://github.com/user-attachments/assets/bda41351-f3fc-4079-a6d3-eb7126a7b8ff" />
*Figure 5: Top features identified by Random Forest and LightGBM.*
