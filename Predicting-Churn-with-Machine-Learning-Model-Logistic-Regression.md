## Predicting Churn with Machine Learning Model: Logistic Regression

### 🧩 Project Overview: 
A predictive analytics project designed to identify customers likely to churn from a telecom service provider using a logistic regression model. The model helps reduce customer attrition and improve retention strategy.

### 💡 Problem Statement: 
Customer churn directly impacts recurring revenue. The challenge is to detect customers at risk of leaving, using historical usage and contract data.

### 🔍 Approach: 
- **Data Cleaning:** Removed identifiers, handled missing values, and encoded categorical features.  
- **Feature Engineering:** Scaled numerical features and applied one-hot encoding.  
- **Modeling:** Logistic Regression with `class_weight='balanced'` to address churn imbalance.  
- **Evaluation:** Measured ROC-AUC (0.84), accuracy, and recall to optimize retention.  

### 📊 Key Insights:

| Metric | Score |
|--------|:------:|
| Accuracy | **0.81** |
| Precision | **0.77** |
| Recall | **0.74** |
| F1-score | **0.75** |
| ROC-AUC | **0.84** |

| Metric     | Score |
|------------|:-----:|
| Accuracy   | 0.81  |
| Precision  | 0.77  |
| Recall     | 0.74  |
| F1-score   | 0.75  |
| ROC-AUC    | 0.84  |

Customers with shorter tenure and higher monthly charges were most likely to churn.
AutoPay and long-term contracts significantly reduced churn risk.
The final model achieved ROC-AUC = 0.84, demonstrating strong predictive ability.

### 🛠️ Tools & Techniques:
Python, pandas, scikit-learn, matplotlib, Logistic Regression, OneHotEncoder, StandardScaler

### 🚀 Outcome:
Delivered a reproducible machine learning pipeline and visual churn analysis notebook, providing an actionable baseline for future retention analytics.




**Project description:** Built an end-to-end machine learning pipeline to predict telecom customer churn. Applied data preprocessing (feature encoding, scaling), logistic regression modeling, and performance evaluation using accuracy, recall, F1-score, and ROC-AUC. The project demonstrates a reproducible, interpretable approach to churn prediction using Python, pandas, scikit-learn, and matplotlib.

### 1. Suggest hypotheses about the causes of observed phenomena

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

```javascript
if (isAwesome){
  return true
}
```

### 2. Assess assumptions on which statistical inference will be based

```javascript
if (isAwesome){
  return true
}
```

### 3. Support the selection of appropriate statistical tools and techniques

<img src="images/dummy_thumbnail.jpg?raw=true"/>

### 4. Provide a basis for further data collection through surveys or experiments

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
