# 🧬 TCGA Dataset Analysis

This Jupyter Notebook provides an analysis of gene expression data from The Cancer Genome Atlas (TCGA) project. The focus is on preprocessing, imputing missing values, and preparing the dataset for downstream tasks such as classification or clustering.

## 📊 Dataset Overview

- The input dataset (`Mulholland_40333245_dataset_1.csv`) contains gene expression data.
- **Rows** represent **gene identifiers**.
- **Columns** represent **patient samples**.
- A special row labeled `Subgroup` identifies class labels (e.g., cancer subtypes).

## 🔍 Objectives

- Load and inspect the structure of TCGA gene expression data.
- Handle missing values using appropriate imputation techniques.
- Apply normalization and scaling to prepare the data for analysis.
- Transpose the dataset to align features with machine learning conventions.

## ⚙️ Tools & Libraries

The following Python libraries are used:

- `pandas` and `numpy` for data handling
- `scikit-learn` for preprocessing and imputation
  - `IterativeImputer`
  - `MinMaxScaler`, `StandardScaler`
- `matplotlib` and `seaborn` (if present later) for visualization

## 🧼 Preprocessing Steps

1. **Load Dataset**: Read the CSV file and assign gene identifiers as the index.
2. **Inspect Data**: Use `.head()` and `.tail()` to understand the shape and content.
3. **Handle Categorical Row**: The `Subgroup` row is extracted and stored for later use, then removed from the main dataset.
4. **Transpose**: Switch the dataset orientation to have samples as rows and features as columns.
5. **Check for numeric types** and apply:
   - **Missing Value Imputation** using `IterativeImputer`
   - **Scaling** using either `MinMaxScaler` or `StandardScaler`

## 🚀 How to Run

1. Ensure the following Python libraries are installed:
   ```bash
   pip install pandas numpy scikit-learn jupyter
   ```
2. Place `TCGA_dataset.csv` in the same directory as the notebook.
3. Launch Jupyter:
   ```bash
   jupyter notebook TCGA_Dataset_Analysis.ipynb
   ```

## 📌 Notes

- Make sure to handle missing values before scaling.
- Review the data distribution before choosing a scaling technique.
- The notebook is designed for flexible reuse with similar transcriptomic datasets.

