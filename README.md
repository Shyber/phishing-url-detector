# 🎣 Phishing URL Detector

Detect phishing URLs in real time by analyzing the **URL structure only**, without visiting the page.

## Goal

Extract lexical features from a URL (length, IP address, number of subdomains, special characters…) and train a binary classifier.

## Tools

Python, Pandas, Scikit-Learn (Random Forest / XGBoost), Streamlit

## Dataset

[PhiUSIIL Phishing URL Dataset](https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+dataset): 235,000+ URLs (Kaggle / UCI).
Download it into `data/` (not tracked by git).

## Structure

```
├── data/        # Dataset (not committed)
├── notebooks/   # Exploration and experiments
└── src/         # Python code
```

## Team

- 3 students
