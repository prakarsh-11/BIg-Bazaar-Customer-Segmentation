# Project Plan: Big Bazaar Customer Segmentation

Goal: split customers into **3 segments** using income, spending score and visit frequency, and give each segment a promotion strategy.

## Phase 1: Data collection
- [x] Load the raw dataset (5,100 rows, 10 columns)
- [x] Keep only `Annual_Income_k`, `Spending_Score`, `Visit_Frequency` (+ `CustomerID`)
- [x] Audit: types, missing values, duplicates, value ranges

## Phase 2: Pre-processing
- [x] Drop duplicate rows (5,100 → 5,000)
- [x] Flag extreme visits (> 3 × IQR) as data-entry errors
- [x] Impute missing + flagged values with the spending-band median
- [x] Sensitivity check: cap vs impute vs log transform
- [x] StandardScaler

## Phase 3: Visualisation (EDA)
- [x] Histograms, boxplots, value counts
- [x] Correlation heatmap
- [x] Pairwise scatter plots (raw)

## Phase 4: Modelling (k = 3)
- [x] Elbow / silhouette / Davies-Bouldin / Calinski-Harabasz for k = 2..10
- [x] K-Means, Hierarchical (Ward), Gaussian Mixture at k = 3
- [x] Select the best model (K-Means)

## Phase 5: Evaluation
- [x] Silhouette, Davies-Bouldin, Calinski-Harabasz
- [x] Per-customer silhouette plot
- [x] Bootstrap stability (Adjusted Rand Index)

## Phase 6: Interpretation
- [x] 2-D and 3-D segment plots
- [x] Segment profiles, names and decision rules
- [x] Promotion strategy per segment; save the sorted CSV

## Ideas for later
See "Future work" in the [README](README.md).
