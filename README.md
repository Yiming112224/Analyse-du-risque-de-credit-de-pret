# Credit Risk Analysis for Loan Default Prediction

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/-Machine%20Learning-orange)
![Data Visualization](https://img.shields.io/badge/-Data%20Visualization-lightgrey)

A comprehensive analysis of credit risk factors and machine learning model for predicting loan default probability.

## 📌 Project Overview
This project analyzes historical lending data to:
- Identify key risk factors in loan applications
- Visualize relationships between borrower characteristics and default risk
- Build a predictive model for loan default probability using LightGBM

## 🚀 Key Features
- **Data Cleaning & Preprocessing**
  - Outlier detection and removal
  - Missing value imputation
  - Categorical variable encoding
- **Exploratory Data Analysis (EDA)**
  - Boxplot analysis for numerical features
  - Ridgeline plots for age distributions
  - Interactive histograms for categorical features
- **Machine Learning**
  - Automated model comparison with PyCaret
  - LightGBM classifier with 93% recall
  - Feature importance analysis
  - AUC-ROC evaluation (0.98 score)

## 📥 Dataset Setup

### Kaggle Dataset
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-blue?logo=kaggle)](https://www.kaggle.com/datasets/laotse/credit-risk-dataset)

1. **Download the dataset**:
   - Visit the [Credit Risk Dataset](https://www.kaggle.com/datasets/laotse/credit-risk-dataset) on Kaggle
   - Click "Download" (requires Kaggle account)

2. **File Placement**:
   ```bash
   # Create data directory
   mkdir -p data
   
   # Move downloaded CSV to project
   mv credit_risk_dataset.csv data/
   ```

### Alternative (Kaggle API)
```bash
# Install Kaggle CLI
pip install kaggle

# Configure API token (follow: https://github.com/Kaggle/kaggle-api#api-credentials)
kaggle datasets download -d laotse/credit-risk-dataset
unzip credit-risk-dataset.zip -d data/
```

## 📦 Installation
1. Clone repository:
```bash
git clone https://github.com/Yiming112224/Analyse-du-risque-de-credit-de-pret.git
cd Analyse-du-risque-de-credit-de-pret
```

2. Create virtual environment:
```bash
python -m venv credit_risk_venv
source credit_risk_venv/bin/activate  # Linux/Mac
credit_risk_venv\Scripts\activate    # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## 🛠 Usage
1. Ensure dataset is in `data/credit_risk_dataset.csv`
2. Run Jupyter notebook:
```python
Projet-Datamining.ipynb
```
3. For predictions:
```python
# Load test data
test_df = pd.read_csv('data/test_data.csv') 
# Get predictions
predictions = clf.predict(test_df[features])
```

## 📂 Project Structure
```
├── Projet-Datamining.ipynb       # Main analysis notebook
├── data_nettoyé.csv              # Cleaned dataset
├── data_nettoyé_sansNa.csv       # Cleaned dataset (no missing values)
├── test_data.csv                 # Sample test data
├── requirements.txt              # Dependency list
└── README.md
```

## 📊 Key Results
### Feature Correlation
![Correlation Matrix](correlation_matrix.png)

### Age Distribution by Loan Intent
![Ridgeline Plot](ridgeline_plot.png)

### Model Performance
| Metric    | Score |
|-----------|-------|
| Recall    | 93%   |
| AUC-ROC   | 0.98  |
| Accuracy  | 89%   |

## 🤝 Contributing
1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License
Distributed under MIT License. See `LICENSE` for more information.

## 📧 Contact
Yiming Gui - guiyiming07@gmail.com  
Project Link: [https://github.com/Yiming112224/Analyse-du-risque-de-credit-de-pret](https://github.com/Yiming112224/Analyse-du-risque-de-credit-de-pret)
```

Key elements included:
1. Clear project overview and features
2. Installation and usage instructions
3. Visual documentation of results
4. Contribution guidelines
5. Performance metrics table
6. Badges for quick project status overview
7. Structured file organization

To complete the setup:
1. Create a `requirements.txt` with all dependencies
2. Add sample images to an `images/` folder
3. Include a license file
4. Add proper error handling in the notebook for dataset path configuration
