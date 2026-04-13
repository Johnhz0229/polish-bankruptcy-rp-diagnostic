# RP-Diag: Credit Risk Model Complexity Audit

Diagnostic tool using Sparse Random Projections to detect
feature redundancy in financial distress prediction models.

## Motivation
Financial ratio datasets contain high mathematical redundancy
— many ratios share common balance sheet terms and are
linearly dependent. This tool quantifies effective
dimensionality and flags over-parameterization risk,
relevant to Basel IRB and IFRS 9 model validation.

## Dataset
Polish Companies Bankruptcy (UCI)
- 5-year bankruptcy prediction
- 64 financial ratio features
- Binary: bankrupt vs. non-bankrupt

## Key Results
- Intrinsic dimensions: 50 / 64
- Redundancy ratio: 21.9%
- Baseline AUC: 0.8171
- Regulatory flag: PASS — Well-calibrated dimensionality

## Methods
- Sparse Random Projection (sklearn)
- Ensemble averaging (n=20)
- Logistic Regression (class_weight='balanced')

## How to Run
1. conda activate credit-rp
2. jupyter notebook
3. Run all cells — data downloads automatically
