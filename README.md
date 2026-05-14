# CS271 Final Project

## Beyond Known Attacks: Comparing Baseline and Deep Learning Models for Robust Network Intrusion Detection

This project studies the robustness of machine learning and deep learning models for network intrusion detection using the CICIDS-2017 dataset.

## Objective
The goal is to evaluate whether strong benchmark performance under standard closed-world settings translates to robustness against unseen attack families under an out-of-distribution (OOD) setup.

## Dataset
- CICIDS-2017
- Total cleaned records: 2,520,798
- Total classes: 15

## Models Used

### Closed-world baselines
- Random Forest
- XGBoost
- MLP

### OOD supervised models
- Random Forest
- XGBoost
- 1D-CNN

### Anomaly-based models
- Autoencoder
- Isolation Forest
- One-Class SVM

## Main Findings
- Standard supervised models performed strongly in the closed-world setting.
- Under OOD evaluation, Random Forest, XGBoost, and 1D-CNN failed completely on withheld attack families.
- Isolation Forest performed best among the anomaly-based methods.
- Heartbleed was easy to detect, while Web Attack subclasses remained difficult across all methods.
- Strong benchmark accuracy does not imply robustness to unseen attacks.

## Repository Contents
- `CS271_Final.ipynb` — main notebook with preprocessing, training, OOD evaluation, and plots
- `per_class_ood_detection.png` — per-class OOD anomaly comparison figure
- `reconstruction_error_benign_vs_ood.png` — reconstruction error distribution figure
- `CS271_Final_Paper.pdf` — final report

## Reproducibility
The notebook contains the main implementation pipeline for preprocessing, OOD split construction, supervised experiments, anomaly detection, runtime comparison, and plotting.
