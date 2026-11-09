# Student Performance Prediction System

A classroom prototype that predicts whether a student is **at risk** of failing the final Mathematics grade.

## Problem
Academic risk is often noticed only after poor results. This prototype explores early identification using available student indicators (study time, absences, failures, G1, G2, etc.).

## Dataset
[UCI Machine Learning Repository - Student Performance](https://archive.ics.uci.edu/dataset/320/student+performance) (ID 320), downloaded through the `ucimlrepo` package.

## Prediction target
`G3 < 10` = **AT RISK**; `G3 >= 10` = **NOT AT RISK**.
`G3` is the target only and is never used as an input feature.

## Technologies
Python, pandas, scikit-learn (Random Forest), joblib, Streamlit, GitHub.

## Installation and run
```bash
git clone https://github.com/YOUR-USERNAME/student-performance-prediction.git
cd student-performance-prediction
pip install -r requirements.txt
python train_model.py        # creates student_data.csv and student_model.pkl
streamlit run app.py         # opens http://localhost:8501
```
In the app, download the sample input CSV and upload it back to test predictions.

## Limitations
- Trained on one Portuguese secondary-school dataset; it may not generalize to other institutions or populations.
- Predictions are not diagnoses and must not be the sole basis for real student decisions.
- Accuracy alone is not enough; review precision, recall and F1 for the "At risk" class.
