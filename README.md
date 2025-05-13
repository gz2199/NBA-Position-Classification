# 🏀 NBA Position Classification

This project uses machine learning techniques to classify NBA players into modern position categories (e.g., Guard, Forward-Guard, Center) based on their physical attributes and in-game performance statistics. With positional roles becoming increasingly fluid in today’s NBA, this project aims to provide a data-driven approach to understanding and predicting a player's on-court role.

---

## 📊 Project Overview

- **Goal**: Predict a player's NBA position based on features such as height, weight, shooting accuracy, assist-to-turnover ratio, and other performance metrics.
- **Dataset**: Scraped using [`nba_api`](https://github.com/swar/nba_api) for the 2024–25 NBA season.
- **Total Players**: 559 active players
- **Features Used**: 21 attributes including physical stats, averages per game (rebounds, assists, etc.), and advanced metrics (TS%, AST/TO).
- **Target**: One of 7 official NBA position labels:
  - Guard, Guard-Forward, Forward-Guard, Forward, Forward-Center, Center-Forward, Center

---

## 🧪 Models Implemented

- **Dummy Classifier** (Baseline)
- **Logistic Regression**
- **K-Nearest Neighbors (KNN)**
- **Decision Tree**
- **Random Forest**

All models were trained using an 80–20 train-test split and evaluated with accuracy, precision, recall, and f1-score.

---

## 📌 Key Findings

- **Best Performance**: The Decision Tree (depth=2) achieved the highest test accuracy (69.7%) and the best weighted f1-score (0.70), with high interpretability.
- **Random Forest** also performed strongly, especially on dominant roles like Guards and Forwards.
- **KNN** and **Logistic Regression** worked well on majority classes but struggled on hybrid roles like Guard-Forward.
- Physical features like height and weight, along with performance metrics like AST/TO and TS%, were strong predictors of position.

---

## 🔧 Requirements

- Python 3.8+
- `scikit-learn`, `pandas`, `matplotlib`, `seaborn`, `nba_api`