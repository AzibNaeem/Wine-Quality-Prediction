# Wine Quality Prediction Project

This project predicts the quality of wine (both red and white) using machine learning models based on physicochemical properties. It includes EDA, class balancing with SMOTE, and classifier performance comparison.

## Dataset
- `winequality-red.csv`
- `winequality-white.csv`

## Key Steps

1. **Data Preprocessing**
   - Merging datasets
   - Feature engineering
   - Removing duplicates

2. **Exploratory Data Analysis**
   - Visualizations using `seaborn` and `matplotlib`
   - Analysis of wine quality distribution

3. **Handling Class Imbalance**
   - Used **SMOTE** to balance underrepresented classes

4. **Model Training**
   - Trained and compared:
     - Random Forest Classifier
     - Gradient Boosting Classifier
     - Support Vector Classifier (SVC)

5. **Evaluation**
   - Evaluated with accuracy metrics

## Technologies Used
- Python
- pandas, matplotlib, seaborn
- scikit-learn
- imbalanced-learn (SMOTE)
- keras, tensorflow *(imported but not used)*

## Results
- Random Forest and Gradient Boosting achieved competitive accuracy
- Improved class representation using SMOTE
