# Sepsis Prediction

## Early Prediction of Sepsis from Clinical Data

## PhysioNet / Computing in Cardiology Challenge 2019

### Overview

This project focuses on early prediction of sepsis in ICU patients using high-resolution electronic health record (EHR) time-series data from the PhysioNet 2019 Sepsis Challenge.

Sepsis is a life-threatening condition caused by a dysregulated immune response to infection. Early detection is critical, as each hour of delayed treatment significantly increases mortality risk.

The objective of this project was to build a machine learning pipeline capable of predicting sepsis onset hours before clinical recognition, enabling earlier intervention and improved patient outcomes.

### Dataset
	•	Source: PhysioNet 2019 Challenge Dataset
	•	Data type: Multivariate ICU time-series
	•	Variables: Vital signs, laboratory values, demographics
	•	Labels: Hourly SepsisLabel (0/1)
	•	Structure: Patient-level longitudinal records

### Methodology

#### 1. Data Preprocessing
	•	Patient-wise grouping (Patient_ID)
	•	Forward-fill and backward-fill imputation per patient
	•	Feature reduction and selection
	•	Handling missingness patterns
	•	Time-order sorting to preserve temporal structure

#### 2. Feature Engineering
	•	Rolling statistics (mean, trend, variance)
	•	Time since ICU admission
	•	Temporal difference (delta) features
	•	Missingness indicators

#### 3. Modeling Approaches
	•	XGBoost

#### 4. Evaluation Metrics
	•	AUROC
	•	AUPRC (primary challenge metric)


### Results
	•	Achieved strong AUROC and AUPRC performance
	•	Demonstrated improved early detection capability within clinically relevant prediction windows
	•	Showed that temporal feature engineering significantly improves performance over static models


### Future Work
	•	Transformer-based sequence models
	•	Survival analysis framing
	•	Uncertainty quantification
	•	Deployment-ready inference pipeline


