## Predicting Churn with Machine Learning Model: Logistic Regression 
📓 [View on GitHub](https://github.com/cdsouza2701/Predicting-Churn-Model/blob/main/churn_model_notebook.ipynb)


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

<!-- <table style="width:55%; text-align:left; border-collapse:collapse;">
  <tr><th>Metric</th><th>Score</th></tr>
  <tr><td>Accuracy</td><td>0.81</td></tr>
  <tr><td>Precision</td><td>0.77</td></tr>
  <tr><td>Recall</td><td>0.74</td></tr>
  <tr><td>F1-score</td><td>0.75</td></tr>
  <tr><td>ROC-AUC</td><td>0.84</td></tr>
</table> -->

<!-- <table style="width:55%; text-align:left; border-collapse:collapse;">
  <tr>
    <th style="border-bottom:1px solid #ccc; padding:6px 8px;">Metric</th>
    <th style="border-bottom:1px solid #ccc; padding:6px 8px;">Score</th>
  </tr>
  <tr>
    <td style="border-bottom:1px solid #eee; padding:6px 8px;">Accuracy</td>
    <td style="border-bottom:1px solid #eee; padding:6px 8px; font-weight:bold;">0.81</td>
  </tr>
  <tr>
    <td style="border-bottom:1px solid #eee; padding:6px 8px;">Precision</td>
    <td style="border-bottom:1px solid #eee; padding:6px 8px; font-weight:bold;">0.77</td>
  </tr>
  <tr>
    <td style="border-bottom:1px solid #eee; padding:6px 8px;">Recall</td>
    <td style="border-bottom:1px solid #eee; padding:6px 8px; font-weight:bold;">0.74</td>
  </tr>
  <tr>
    <td style="border-bottom:1px solid #eee; padding:6px 8px;">F1-score</td>
    <td style="border-bottom:1px solid #eee; padding:6px 8px; font-weight:bold;">0.75</td>
  </tr>
  <tr>
    <td style="padding:6px 8px;">ROC-AUC</td>
    <td style="padding:6px 8px; font-weight:bold;">0.84</td>
  </tr>
</table> -->

<table style="border-collapse:collapse; width:260px; font-size:0.95rem;">
  <tr>
    <th style="border:1px solid #d0d7de; background-color:#f6f8fa; text-align:left; padding:8px 10px; font-weight:600;">
      Metric
    </th>
    <th style="border:1px solid #d0d7de; background-color:#f6f8fa; text-align:left; padding:8px 10px; font-weight:600;">
      Score
    </th>
  </tr>
  <tr>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">Accuracy</td>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.81</td>
  </tr>
  <tr>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">Precision</td>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.77</td>
  </tr>
  <tr>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">Recall</td>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.74</td>
  </tr>
  <tr>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">F1-score</td>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.75</td>
  </tr>
  <tr>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">ROC-AUC</td>
    <td style="border:1px solid #d0d7de; padding:8px 10px;">0.84</td>
  </tr>
</table>

Customers with shorter tenure and higher monthly charges were most likely to churn.
AutoPay and long-term contracts significantly reduced churn risk.
The final model achieved ROC-AUC = 0.84, demonstrating strong predictive ability.

### 🛠️ Tools & Techniques:
Python, pandas, scikit-learn, matplotlib, Logistic Regression, OneHotEncoder, StandardScaler

### 🚀 Outcome:
Delivered a reproducible machine learning pipeline and visual churn analysis notebook, providing an actionable baseline for future retention analytics.


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
