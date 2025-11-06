# Customer Churn Prediction — Telco Dataset

This project aims to predict customer churn for a telecom service provider using statistical modeling and machine learning techniques. The system identifies customers who are likely to discontinue services, enabling proactive retention strategies.

## 📁 Project Structure
```
├── WA_Fn-UseC_-Telco-Customer-Churn.csv   # Dataset
├── churn_model.pkl                        # Saved Deployment Model
├── Customer_Churn_Analysis.ipynb          # Google Colab Notebook
└── README.md
```

## 🎯 Project Objective
- Analyze telecom customer data  
- Identify key churn indicators  
- Build & compare prediction models  
- Extract human-understandable rules  
- Save the best model for deployment  

## 🧾 Dataset Details
**Source:** Telco Customer Churn Dataset  
**Rows:** ~7043 customers  
**Target Variable:** `Churn` (Yes / No)

### Key Columns
| Feature | Description |
|--------|-------------|
| tenure | Number of months customer stayed |
| MonthlyCharges | Monthly billing amount |
| Contract | Contract type |
| PaymentMethod | Preferred payment option |
| TotalCharges | Total billed amount |

## 🔧 Tools & Libraries Used
| Category | Tools Used |
|---------|-----------|
| Programming | Python (Google Colab) |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Modeling | DecisionTreeClassifier (CHAID Equivalent), Logistic Regression |
| Deployment | Pickle |

## 📊 Exploratory Data Analysis
- Cleaned missing values  
- Categorical → Numeric Encoding  
- Visualized churn distribution  
- Generated correlation heatmap  

## 🤖 Models Developed
| Model | Purpose | Strength |
|------|---------|---------|
| CHAID (Decision Tree - entropy) | Rule extraction | Interpretability |
| Logistic Regression | Predictive accuracy | Best performance ✅ |

### Model Comparison
| Metric | CHAID Model | Logistic Regression |
|--------|-------------|--------------------|
| Accuracy | Medium | Higher |
| ROC-AUC | Medium | **Higher** ✅ |

**Selected Best Model:** Logistic Regression  
Saved as → `churn_model.pkl`

## ⚙ Model Deployment
```python
import pickle
model = pickle.load(open("churn_model.pkl", "rb"))
```

## 📌 How to Run
1. Open Google Colab notebook
2. Upload the dataset:
   ```python
   from google.colab import files
   files.upload()
   ```
3. Run all cells sequentially
4. Model file (`churn_model.pkl`) will be generated

## 📈 Business Insights
- Month-to-month contract holders churn more  
- Higher monthly cost impacts churn likelihood  
- Electronic check customers show higher churn  
- Longer contracts reduce churn significantly  

## 👨‍💻 Author
**Mukund**  
B.Tech Artificial Intelligence — SRM IST
