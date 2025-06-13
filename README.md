# 🔐 URL Phishing Detection System

A complete full‑stack phishing URL detection app with machine learning backend and a user-friendly web GUI built using Flask, HTML, CSS, and JavaScript.

---

## 🔍 Overview

This application classifies URLs as **Safe** or **Phishing** by:

1. **Extracting features** from URLs (structural and content-based).
2. **Training machine learning models** (Random Forest, Logistic Regression, Naive Bayes).
3. **Selecting Random Forest**, which delivered ~96.9% accuracy.
4. **Deploying via Flask**, exposing a `/predict` API consumed by a JavaScript frontend.

---

## 💡 Key Features

- 🔬 **ML-based detection**: Random Forest performs best (~96.9% accuracy), compared to Logistic Regression (~93.4%) and Naive Bayes (~60.5%).
- 🧠 **Feature engineering & EDA**: Includes correlation heatmaps, pairplots, and pie‑charts for visualization.
- 🛠 **GUI**: Users can input a URL, trigger Flask backend, and view phishing predictions live.
- 🌐 **Modern front-end stack**: HTML/CSS for layout, vanilla JavaScript (or AJAX) for seamless interaction.
- ✅ **Persistence**: Trained model saved via `pickle` for deployment.

---

## 📈 Model Performance

| Model                 | Accuracy | F1 Score | Recall | Precision |
|-----------------------|----------|----------|--------|-----------|
| Random Forest         | 96.9%    | 97.2%    | 99.4%  | 98.9%     |
| Logistic Regression   | 93.4%    | 94.1%    | 94.3%  | 92.7%     |
| Naive Bayes           | 60.5%    | 45.4%    | 29.2%  | 99.7%     |

---

## 📦 Requirements
```bash
Flask
scikit-learn
pandas
numpy
matplotlib
seaborn
```

---

## 💻 Installation

Clone and install dependencies:

```bash
git clone https://github.com/garvitverma21/URL-Phishing-Detection-System.git
cd URL-Phishing-Detection-System
pip install -r requirements.txt
```

---

## ▶️ Running the App
1. Ensure random_forest_model.pkl is present:
   ```bash
   python phishing_detection.ipynb  # Or run training script
   ```
3. Start Flask:
   ```bash
   python app.py
   ```
5. Open `http://localhost:5000` in your browser, enter a URL, and click Scan to see the result.
