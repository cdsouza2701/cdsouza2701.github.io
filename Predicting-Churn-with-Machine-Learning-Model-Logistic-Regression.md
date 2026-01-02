## Predicting Churn with Machine Learning Model: Logistic Regression 
📓 <a href="https://github.com/cdsouza2701/cdsouza2701/blob/dcbac02185120ad2f3467417b4d66e975318a050/Webscraper.ipynb" target="_blank" rel="noopener noreferrer">View Project Code</a>


### 🧩 Project Overview: 
A predictive analytics project designed to identify customers likely to churn from a telecom service provider using a logistic regression model. The model helps reduce customer attrition and improve retention strategy.


### 💡 Problem Statement: 
Customer churn directly affects recurring revenue and profitability.  
The challenge was to **detect customers most likely to leave**, using historical service and demographic data — enabling proactive retention actions such as targeted offers and contract renewals.

### 🔍 Approach: 
- **Data Exploration:** Verified data completeness (no missing values) and examined customer trends such as tenure and contract type.  
- **Data Cleaning:** Removed non-informative identifiers (e.g., `customerID`) and ensured numeric types were correctly set for all columns.  
- **Feature Encoding:** Used `LabelEncoder` to transform categorical variables (e.g., `Contract`, `PaymentMethod`, `InternetService`) into numeric codes suitable for model training.  
- **Model Training:** Trained a `LogisticRegression(max_iter=1000)` classifier on 80% of the data, using 20% for testing.
  - Logistic Regression was chosen for **its interpretability**, **speed**, and **probabilistic outputs**, which help rank customers by churn risk.
- **Evaluation:** Used metrics like accuracy, precision, recall, F1-score, and ROC-AUC to assess predictive performance and balance between false positives/negatives.  

### 📊 Key Insights:

<table style="border-collapse:collapse; width:260px; font-size:0.95rem;"> 
  <tr> 
    <th style="border:1px solid #d0d7de; background-color:#f6f8fa; text-align:left; padding:8px 10px; font-weight:600;">Metric</th> 
    <th style="border:1px solid #d0d7de; background-color:#f6f8fa; text-align:left; padding:8px 10px; font-weight:600;">Score</th> 
  </tr> 
  <tr style="background-color:#ffffff;"> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">Accuracy</td> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.81</td> 
  </tr> 
  <tr style="background-color:#f6f8fa;"> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">Precision</td> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.77</td> 
  </tr> 
  <tr style="background-color:#ffffff;"> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">Recall</td> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.74</td> 
  </tr> 
  <tr style="background-color:#f6f8fa;"> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">F1-score</td> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.75</td> 
  </tr> 
  <tr style="background-color:#ffffff;"> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">ROC-AUC</td> 
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.84</td> 
  </tr> 
</table>

- **Customers with short tenure and high monthly charges** were most likely to churn.  
- **AutoPay** and **long-term contracts** significantly reduced churn risk.  
- The model achieved a **ROC-AUC of 0.84**, indicating strong ability to separate churners from non-churners.  

**Why it matters:**  
These insights provide clear business actions — encourage AutoPay enrollment, reward long-term contracts, and target short-tenure, high-charge customers with loyalty offers.

### 🛠️ Tools & Techniques:

<table style="border-collapse:collapse; width:100%; font-size:0.95rem;">
  <tr> 
    <th style="border:1px solid #d0d7de; background-color:#f6f8fa; text-align:left; padding:8px 12px;">Category</th> 
    <th style="border:1px solid #d0d7de; background-color:#f6f8fa; text-align:left; padding:8px 12px;">Tools / Libraries</th> 
    <th style="border:1px solid #d0d7de; background-color:#f6f8fa; text-align:left; padding:8px 12px;">Reason for Use</th> 
  </tr> 
  <tr style="background-color:#ffffff;"> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">Data Analysis</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">pandas, numpy</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">For cleaning and exploration</td> 
  </tr> 
  <tr style="background-color:#f6f8fa;"> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">Visualization</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">matplotlib, seaborn</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">For visual pattern discovery</td> 
  </tr> 
  <tr style="background-color:#ffffff;"> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">Preprocessing</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">LabelEncoder</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">Convert categorical to numeric</td> 
  </tr> 
  <tr style="background-color:#f6f8fa;"> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">Modeling</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">LogisticRegression (scikit-learn)</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">Fast, interpretable binary classifier</td> 
  </tr> 
  <tr style="background-color:#ffffff;"> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">Evaluation</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">classification_report, confusion_matrix, accuracy_score</td> 
    <td style="border:1px solid #d0d7de; padding:8px 12px;">To measure performance metrics</td> 
  </tr> 
</table>

### 🚀 Outcome:
Delivered a complete, reproducible **machine learning pipeline** to predict customer churn with 81% accuracy and 0.84 ROC-AUC.  
The project demonstrates end-to-end implementation — from data cleaning to business insights — and serves as a baseline for future experiments with advanced models (e.g., Random Forest or XGBoost).


<details>
<summary><b>📈 Behind the Model</b></summary>
Your text here
</details>

