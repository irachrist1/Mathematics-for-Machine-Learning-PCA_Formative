# PCA Formative Assignment

**Course:** Mathematics for Machine Learning  
**Student:** Christian Tonny Gentil Iradukunda 
**Date:** February 2026

## Overview

This project implements Principal Component Analysis (PCA) from scratch using NumPy to analyze health and development indicators across African countries. The goal is to reduce the dimensionality of the dataset while preserving as much information as possible.

## Dataset

**Source:** Kaggle https://www.kaggle.com/datasets/lydia70/malaria-in-africa - Africa Malaria and Health Indicators  
**File:** `DatasetAfricaMalaria.csv`

The dataset contains health and development metrics for African countries including:
- Malaria incidence rates
- Access to water and sanitation
- Population statistics
- Geographic coordinates

**Original size:** 594 rows × 27 columns  
**After cleaning:** 594 rows × 15 columns

### Data Characteristics
- Contains missing values (4,485 total across all cells)
- Has non-numeric columns (Country Name, Country Code, geometry)
- Real-world data with natural correlations between features

## Methods

### Data Preprocessing
1. Removed non-numeric columns (text data)
2. Dropped columns with more than 70% missing values
3. Filled remaining missing values with column means

### PCA Implementation
All steps implemented using NumPy only (no sklearn):

1. **Standardization** - scaled features to mean=0, std=1
2. **Covariance matrix** - calculated feature relationships
3. **Eigendecomposition** - found principal directions
4. **Sorting** - ordered by variance explained
5. **Component selection** - chose components to retain 90% variance
6. **Projection** - transformed data to reduced dimensions

## Results

| Metric | Value |
|--------|-------|
| Original features | 15 |
| Components selected | 8 |
| Variance retained | 92.31% |

### Variance Explained by Component

| Component | Individual | Cumulative |
|-----------|------------|------------|
| PC1 | 41.59% | 41.59% |
| PC2 | 13.98% | 55.57% |
| PC3 | 9.34% | 64.90% |
| PC4 | 8.59% | 73.49% |
| PC5 | 6.11% | 79.60% |
| PC6 | 5.41% | 85.01% |
| PC7 | 4.21% | 89.23% |
| PC8 | 3.08% | 92.31% |

## How to Run

1. Make sure you have Python with NumPy, Pandas, and Matplotlib installed
2. Place `DatasetAfricaMalaria.csv` in the same folder as the notebook
3. Open `PCA_Formative_Gentil_Iradukunda.ipynb` in colab or juptyer
4. Run all cells in order

## Files

```
├── README.md                         
├── DatasetAfricaMalaria.csv          # dataset
└── PCA_Formative_TonnyMuhumuza.ipynb # main notebook with all code
```

## Key Findings

- The first principal component alone captures 41.59% of the variance, suggesting there's one dominant pattern in the data (likely related to overall development level)
- 8 components are needed to reach 90% variance retention
- Dimensionality was reduced by nearly half (15 → 8) while keeping most information
- The before/after visualization shows that data structure is preserved after transformation

## References

- Kaggle dataset link: [https://data.worldbank.org/](https://www.kaggle.com/datasets/lydia70/malaria-in-africa)
- NumPy Documentation: https://numpy.org/doc/
