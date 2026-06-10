# Mathematics-for-Machine-Learning-PCA_Formative

PCA from scratch on African malaria and health indicators — ALU Mathematics for Machine Learning formative assignment.

## The problem

You have 27 columns of health data across 594 African countries. Plotting everything at once is noise.

You need dimensionality reduction that preserves variance — implemented yourself in NumPy, not `sklearn.decomposition` black box.

## What it does

Implements PCA manually: center data, compute covariance, eigendecomposition, project to principal components. Analyzes `DatasetAfricaMalaria.csv` from Kaggle.

```
594 rows × 27 columns → cleaned 15 features → 2–3 principal components explaining most variance
```

## Install

```bash
git clone https://github.com/irachrist1/Mathematics-for-Machine-Learning-PCA_Formative.git && cd Mathematics-for-Machine-Learning-PCA_Formative
pip install numpy pandas matplotlib jupyter
jupyter notebook PCA_Formative_Gentil_Iradukunda.ipynb
```

## How it works

- **Manual PCA pipeline.** Mean centering → covariance matrix → eigenvalues/eigenvectors → projection — every step explicit in NumPy.
- **Real-world messy data.** 4,485 missing values, non-numeric columns dropped — handles actual CSV chaos, not toy datasets.
- **Variance explained analysis.** Scree plot and cumulative variance — justifies component count with math, not guesswork.
- **African health context.** Malaria incidence, water access, sanitation — interpretable loadings on real policy-relevant features.
- **Formative submission.** ALU checker-compatible notebook with documented methodology section.

ALU coursework · [Christian Tonny](https://github.com/irachrist1)
