# Fraud Detection (Capstone Project)

## Business Goal
Detect fraudulent credit card transactions to reduce fraud losses while minimizing false alarms that harm customer experience.

## Dataset
- Source: Kaggle – Credit Card Fraud Detection (ULB dataset)
- Note: Raw dataset not uploaded due to licensing/size. Download it from Kaggle and place it in `data/raw/creditcard.csv`.

## Project Structure
- `notebooks/` – Jupyter notebooks (EDA, training, evaluation)
- `src/` – reusable scripts (prep, training, evaluation, fairness audit)
- `models/` – saved trained models
- `reports/` – final report / documentation
- `figures/` – plots for reporting

## How to Run (Reproducible Setup)

### 1) Create environment
```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# Mac/Linux:
source .venv/bin/activate
```

### 2) Install dependencies
```bash
pip install -r requirements.txt
```

### 3) Download dataset
Download `creditcard.csv` from Kaggle and place it here:
`data/raw/creditcard.csv`

### 4) Run notebook
Open and run:
`notebooks/Fraud_Detection_Project.ipynb`

## Results Summary (Test Set)
- Model: Tuned Random Forest
- PR-AUC: 0.8685
- Precision: 0.9111
- Recall: 0.8367
- F1: 0.8723
- Threshold: 0.29

## Ethical AI
A proxy fairness audit was conducted using:
- `Amount_Band` (transaction size bands)
- `Hour_Band` (time-of-day bands)
Metrics reported: flag rate, TPR/FPR, and disparate impact ratios.
