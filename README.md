# Algerian Wildfire Prediction Project
### A data Quality Assessment Pipeline

## Overview
Predicts fire risks using meteorological data from Algeria (2012). Includes:
- **Data cleaning pipeline** (NULL handling, deduplication, boundary checks)
- **Automated validation** (4 quality rules)
- **Risk classification** (K-Means clustering)
- **FWI prediction model** (Gradient Boosting, R²=0.82)

## 🔍 Data Glossary
| Abbreviation | Full Name                | Range       |
|--------------|--------------------------|-------------|
| RH           | Relative Humidity        | 0-100%      |
| Ws           | Wind Speed               | 0-100+ km/h |
| FWI          | Fire Weather Index       | 0-100+      |
| ISI          | Initial Spread Index     | 0-56+       |

## ✅ Validation Rules Applied
| Rule  | Field       | Check                      | Action                 |
|-------|-------------|----------------------------|------------------------|
| C-01  | Temperature | No NULLs                   | Median imputation      |
| V-01  | RH          | 0 ≤ RH ≤ 100               | Capped at boundaries   |
| U-01  | FireID      | Unique format              | Dropped duplicates     |
| B-01  | FWI         | FWI ≥ ISI                  | Recalculated (ISI×1.2) |

## 📂 Files
- `notebook.ipynb`: Full analysis (cleaning → modelling)
- `data/`: 
  - `FireData.csv` (raw)
  - `FireData_Cleaned.csv` (processed)
- `requirements.txt`: Python dependencies

## 📜 Dataset Citation  
Dataset Source:  
[UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/547/algerian+forest+fires+dataset)  

## Explore the project:  
📊 [Kaggle Notebook](https://www.kaggle.com/code/surprisemhlongo/data-quality-mdm-portfolio/) (Interactive Analysis)  



