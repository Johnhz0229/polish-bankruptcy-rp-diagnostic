# CLAUDE.md

## Project Overview
Random Projection diagnostic tool for credit risk models.
Dataset: Polish Companies Bankruptcy (UCI)
Goal: Show how much a high-dimensional financial distress
dataset can be compressed using Sparse Random Projections
while retaining classification performance (AUC).
Final deliverable: notebook.ipynb

## Language
All output must be in English.
This includes: markdown cells, plot labels, axis titles,
printed outputs, code comments, and take-home message.
No Chinese anywhere in the notebook.

## Environment
- conda env: credit-rp (Python 3.11)
- dependencies: see requirements.txt

## Data
- Source: UCI Machine Learning Repository
- Dataset: Polish Companies Bankruptcy
- URL: https://archive.ics.uci.edu/ml/machine-learning-databases/00365/
- Files: 1year.arff through 5year.arff
- Use: 5year.arff (largest, most features, best for RP)
- Do NOT commit data to git

## Notebook Structure
0. Setup & Imports
1. Data Download & Preprocessing
2. EDA
3. Baseline: Full-dimension Logistic Regression
4. Random Projection Experiment (Sparse RP, ensemble n=20)
5. Intrinsic Dimensionality Diagnosis
6. Final Visualization + Take-home Message

## Code Style
- Simple and readable — code will be presented and explained
- Each code cell max 30 lines
- English labels on all plots
- Markdown cells explain the "why", not just the "what"
- No redundant comments inside code
- Variable names should be self-explanatory

## Key Parameters
- test_size = 0.2
- random_state = 42
- n_ensemble = 20
- k_range = [2,3,4,5,8,10,15,20,25,30,35,40,45,50,55,60,64]
- threshold = 0.99
- class_weight = 'balanced'

## Why This Dataset
Polish bankruptcy data contains 64 financial ratios derived
from balance sheets and income statements. These ratios are
mathematically interrelated (e.g. liquidity ratios share
common terms), creating high statistical redundancy.
This makes it ideal for demonstrating Random Projection's
ability to detect feature redundancy in financial data.