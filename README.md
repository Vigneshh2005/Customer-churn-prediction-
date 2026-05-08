# Customer Churn Prediction

## Project Overview
This project predicts whether a telecom customer is likely to churn (leave the service) using various machine learning techniques. It includes data preprocessing, feature engineering, model training, evaluation, and comparison of multiple algorithms to identify the best-performing model for churn prediction.

The goal is to help telecom companies retain customers by proactively identifying those at risk of leaving.

---

## Technologies Used
- **Python** - Programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical data visualization
- **Scikit-learn** - Machine learning library
- **Imbalanced-learn** - Handling imbalanced datasets (optional)

---

## Dataset
**Telco Customer Churn Dataset**

The dataset contains 7,043 customer records with 21 features, including:
- Demographic information: Gender, Senior Citizen, Partner, Dependents
- Service details: Tenure, Phone Service, Multiple Lines, Internet Service, Online Security, Online Backup, Device Protection, Tech Support, Streaming TV, Streaming Movies
- Billing information: Contract Type, Paperless Billing, Payment Method, Monthly Charges, Total Charges
- Target variable: Churn (Yes/No)

**Data Source**: `WA_Fn-UseC_-Telco-Customer-Churn.csv`

---

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Vigneshh2005/Customer-churn-prediction-.git
   cd Customer-Churn-Prediction
   ```

2. Create and activate a virtual environment (recommended):
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # On Windows
   ```

3. Install required packages:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
   ```

4. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

5. Open and run `churn_prediction.ipynb`

---

## Data Preprocessing
- Removed the customer ID column
- Converted Total Charges to numeric (handling missing values by filling with mean)
- Applied Label Encoding to categorical features
- Performed train-test split (80-20)
- Applied Standard Scaling for neural network models

---

## Machine Learning Models Used

### 1. Logistic Regression (with scaling)
- **Accuracy**: 81.62%
- **Precision (Churn)**: 0.68
- **Recall (Churn)**: 0.58
- **F1-Score (Churn)**: 0.63

### 2. Decision Tree Classifier
- **Accuracy**: 73.39%

### 3. Neural Network (MLPClassifier) - Basic
- **Accuracy**: 78.71%
- Hidden layers: (100,)
- Max iterations: 500

### 4. Neural Network (MLPClassifier) - Improved
- **Accuracy**: 77.15%
- Hidden layers: (100, 50)
- Activation: ReLU
- Solver: Adam
- Max iterations: 1000

---

## Results and Analysis
- Logistic Regression achieved the highest accuracy (81.62%) among all models
- Neural Networks performed well but required feature scaling
- Decision Tree was the simplest but least accurate
- The dataset shows class imbalance (churn rate ~26.5%), which may affect model performance

---

## Usage
1. Run all cells in the Jupyter notebook `churn_prediction.ipynb`
2. The notebook will:
   - Load and explore the dataset
   - Preprocess the data
   - Train multiple models
   - Display accuracy metrics and visualizations
   - Compare model performances

---

## Future Improvements
- Handle class imbalance using SMOTE or other techniques
- Feature engineering (create new features)
- Hyperparameter tuning using Grid Search
- Try other algorithms (Random Forest, XGBoost, SVM)
- Deploy the model as a web application

---

## License
This project is for educational purposes. Feel free to use and modify.

---

## Contact
For questions or suggestions, please open an issue in the repository.

This project demonstrates how machine learning can help telecom companies identify customers likely to leave their services and take preventive actions to improve customer retention.
