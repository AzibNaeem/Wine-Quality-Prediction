# 🍷 Wine Quality Analysis & Cleaning with EDA  
### 🔍 IDS Project – Exploratory Data Analysis on Wine Datasets  

![Wine Banner](https://images.unsplash.com/photo-1612198083699-c37cbbfc6739?auto=format&fit=crop&w=1350&q=80)

---

## 📜 Project Overview

Welcome to the **Wine Quality EDA & Cleaning** project! 🎉  
This project explores, cleans, and visualizes data from red and white wine datasets 🍇🍷, aiming to discover patterns and prepare it for machine learning models.

---

## 📁 Dataset Description

The datasets used in this project are:

- `winequality-red.csv` – 🍷 Red wine samples  
- `winequality-white.csv` – 🥂 White wine samples  

Each contains physicochemical properties like:
- 🧪 pH
- 🍶 Alcohol
- 🧂 Sulphates
- 🍋 Citric acid
- ⚖️ Density  

🧠 The target variable `quality` represents a score between **0 to 10**.

---

## 🎯 Project Goals

✔️ Merge datasets & label wine types  
✔️ Handle missing values & remove duplicates  
✔️ Analyze feature distributions  
✔️ Detect & understand outliers  
✔️ Balance the dataset using **SMOTE**  
✔️ Create stunning visualizations & insights  

---

## 📦 Libraries Used

```python
pandas           # Data manipulation 🧠
matplotlib       # Static plotting 📊
seaborn          # Statistical visuals 🌊
imblearn         # SMOTE for resampling ⚖️
```

---

## 🛠️ Data Preprocessing

🔹 Both red and white wine datasets are merged  
🔹 A new column `wine_type` is added:
- `0` → Red 🍷  
- `1` → White 🥂  

🔹 Cleaned for:
- ❌ Missing values
- 🗃️ Duplicates
- 🧾 Data types using `.info()` and `.isna()`

---

## 📊 Data Visualization

🖼️ This project is rich with visualizations! Including:
- 📈 Countplots for wine quality
- 🧊 Correlation heatmaps
- 📏 Pair plots to detect trends
- 📦 Box plots to find outliers

Example:

```python
sns.countplot(data=data, x='quality', hue='wine_type')
```

This reveals how wine types differ across quality ratings!

---

## ⚠️ Outlier Detection

Using **box plots**, outliers were identified in:
- Volatile acidity
- Sulphates
- Alcohol  
These were reviewed for impact and may be removed in ML modeling.

---

## ⚖️ Balancing the Dataset with SMOTE

The dataset was highly imbalanced! 😬  
To fix this, we used **SMOTE (Synthetic Minority Oversampling Technique)**:

```python
from imblearn.over_sampling import SMOTE

smote = SMOTE(random_state=42, k_neighbors=1)
x_sampled, y_sampled = smote.fit_resample(x, y)
```

Balanced data = better models! 🚀

---

## 🧠 Correlation Insights

We generated a heatmap to uncover relationships:

🔍 Key Findings:
- Alcohol ↗️ Quality  
- Volatile Acidity ↘️ Quality  
- Citric Acid & pH are closely tied  

These features may be key in predicting wine quality 🍷✅

---

## 📝 Final Thoughts

The dataset is now:
- Clean ✅
- Balanced ✅
- Visualized ✅
- Insightful ✅

Perfect for training powerful ML models to classify wine quality!

---

## 🚀 Future Plans

Here’s what can be done next:
- 🔍 Apply classifiers: Random Forest, SVM, XGBoost
- 🧮 Perform PCA or feature selection
- 🧑‍💻 Build a Streamlit dashboard for interaction
- 🌐 Deploy with Flask or FastAPI

---

## 🙋‍♂️ Author

Made with ❤️ by **Azib Naeem**  
📧 [azibnaeem17official@gmail.com](mailto:azibnaeem17official@gmail.com)

---

## 💻 How to Run

```bash
git clone <repo_url>
cd wine-eda-project
pip install -r requirements.txt
jupyter notebook
```

> 📂 Make sure `winequality-red.csv` and `winequality-white.csv` are in the same directory as the notebook.

---

⭐ *If you like this project, feel free to star ⭐ the repository and share it!*  
🧠 *Happy Analyzing!*
