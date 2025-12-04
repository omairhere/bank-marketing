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
    git clone [https://github.com/YOUR_USERNAME/bank-marketing-pipeline.git](https://github.com/YOUR_USERNAME/bank-marketing-pipeline.git)
    cd bank-marketing-pipeline
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

![Class Distribution](images/class_distribution.png)
*Figure 1: Target Class Distribution showing dataset imbalance.*

![Correlation Heatmap](images/correlation_heatmap.png)
*Figure 2: Correlation Heatmap of top features.*

### 2. Model Evaluation
Comparing how well the models separate positive and negative classes.

![ROC Curve](images/roc_curve_comparison.png)
*Figure 3: ROC Curve Comparison indicating LightGBM's superior AUC.*

![Metric Comparison](images/metric_comparison.png)
*Figure 4: Side-by-side metric comparison.*

### 3. Feature Importance
What drives a customer to say "Yes"?

![Feature Importance](images/feature_importance.png)
*Figure 5: Top features identified by Random Forest and LightGBM.*

---

## 📂 Project Structure

```text
├── data/
│   └── bank-additional.csv    # Source dataset
├── images/                    # Saved plots and graphs
│   ├── roc_curve.png
│   ├── confusion_matrix.png
│   └── ...
├── main.py                    # Main execution script
├── README.md                  # Project documentation
└── requirements.txt           # Python dependencies
