# Algerian Wildfire Prediction Project

## 📌 Overview
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
- `notebook.ipynb`: Full analysis (cleaning → modeling)
- `data/`: 
  - `FireData.csv` (raw)
  - `FireData_Cleaned.csv` (processed)
- `requirements.txt`: Python dependencies

## 🚀 Setup
```bash
pip install -r requirements.txt
jupyter notebook notebook.ipynb

@misc{abid2019algerian,
  author = {Abid, A.},
  title = {Algerian Forest Fires Dataset},
  year = {2019},
  publisher = {UCI Machine Learning Repository},
  doi = {10.24432/C5KW4N}
}