Group 1 MDS Capstone Project – Winter 2026
Machine Learning Approach to Forecasting Nonprofit Donor Retention
Tristan Roman, David Lightfoot, Julian Estrada, Julia Klayman
GitHub Repository: https://github.com/d-lightfoot/DSC-288-Capstone-Project/

Overview

This project builds a leakage-safe, year-conditional donor lapse prediction pipeline using opportunity-level donation records from a nonprofit Salesforce CRM. The goal is to rank donors by lapse risk and enable targeted, resource-constrained outreach.

Repository Contents

Notebook.ipynb: Full pipeline: cleaning, EDA, feature engineering, modeling, and evaluation
RunPodSetupInstructions.txt: Instructions for running the notebook on RunPod
DatasetDownloadLink.txt: Link to download the dataset (not included in zip due to data privacy; access has been shared directly with the professor and instructional assistants)

How to Run

1. Download the dataset using the link in DatasetDownloadLink.txt
2. Follow RunPodSetupInstructions.txt to set up your environment
3. Place the dataset at the path specified in Cell 2 of the notebook
4. Run cells in order - Cell 0 is optional if your environment is already stable
5. Cells 4-6 (cleaning) can be skipped if the cleaned dataset is already available

Pipeline Summary

Section A: Data cleaning (removes PII, normalizes types, deduplicates transactions)
Section B: EDA (validates coverage and temporal donation trends)
Section C: Donor x Year panel construction, leakage-safe feature engineering, and year-conditional lapse labeling
Section D: Temporal train/val/test split (2014-2023/2024/2025) and model training (Logistic Regression, Random Forest, XGBoost)
Section E: Probability calibration (Platt scaling) and Top-K outreach policy evaluation

Key Results (Test Year: 2025)

XGBoost AUPRC: ~0.75
Precision@1000: ~79%
Lift@1000: ~1.26x over random outreach

Requirements

See Cell 0 in the notebook for environment setup. Compatible with RunPod and local Python environments.
