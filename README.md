# 🚀 Microsoft: Classifying Cybersecurity Incidents with Machine Learning 🛡️

> **Objective**  
> The project aims to empower Security Operation Centers (SOCs) with a machine learning model that predicts the triage grade of cybersecurity incidents. By identifying true positives, benign positives, and false positives, SOC analysts can prioritize response efforts, cutting down response time to critical threats. 

## 🧠 Skills Acquired
- 🔄 Data Preprocessing & Feature Engineering
- 🤖 Machine Learning Classification Techniques
- 📊 Model Evaluation Metrics (Macro-F1, Precision, Recall)
- 🔒 Cybersecurity Concepts (MITRE ATT&CK Framework)
- ⚖️ Handling Imbalanced Datasets
- 🚀 Model Benchmarking & Optimization

---

## 🌐 Domain
**Cybersecurity and Machine Learning**

---

## 📝 Problem Statement
As a data scientist at Microsoft, your task is to develop a model that classifies incidents based on historical evidence and customer feedback. Using the GUIDE dataset, this model predicts triage grades (TP, BP, FP) to support SOCs in incident prioritization, aiming to bolster enterprise security.

---

## 💼 Business Use Cases
1. **SOC Automation**: Streamline incident triage, enabling faster analyst response.
2. **Incident Response**: Automated guidance on action steps for various incidents.
3. **Threat Intelligence**: Improved threat detection by utilizing historical data.
4. **Enterprise Security**: Minimized false positives with prioritized threat response.

---

## 🔍 Approach
1. **Data Exploration and Understanding**
   - Inspect data structure and perform EDA with a focus on class imbalance.
2. **Data Preprocessing**
   - Handle missing values, engineer features, and encode categorical data.
3. **Data Splitting**
   - Stratify training and validation sets to address class imbalance.
4. **Model Selection and Training**
   - Begin with a baseline model, then explore Random Forest, XGBoost, LightGBM, etc.
5. **Model Evaluation**
   - Prioritize macro-F1, precision, and recall metrics.
6. **Model Interpretation**
   - Analyze feature importance and conduct error analysis.
7. **Final Evaluation**
   - Compare the model’s performance on the test dataset to the baseline.

---

## 🧪 Methodology

### 1. Data Exploration & Preprocessing
- **Data Source**: Millions of rows with features such as `AlertTitle`, `Category`, `EntityType`, and more. The target variable is `IncidentGrade`.
- **Missing Values**: Addressed missing data by imputing or removing irrelevant columns.
- **Feature Engineering**: Extracted `Year`, `Month`, `Day`, `Hour` from timestamp data.
- **Feature Encoding**: Applied label encoding to categorical columns.

### 2. Model Selection & Training
Tested models included:
- 🔹 Logistic Regression
- 🔹 Decision Tree
- 🔹 Random Forest
- 🔹 XGBoost
- 🔹 LightGBM
- 🔹 Gradient Boosting

### 3. Model Evaluation Metrics
- **Accuracy**: Overall correctness
- **Precision**: Accuracy of positive predictions
- **Recall**: Ability to capture all positive instances
- **F1 Score**: Harmonic mean of precision and recall
- **Macro-F1 Score**: Average F1 score across all classes

---

## 📊 Model Performance Summary

| Model              | Accuracy | Macro-F1 Score | Precision | Recall |
|--------------------|----------|----------------|-----------|--------|
| Logistic Regression | 0.6460  | 0.55          | 0.67      | 0.65   |
| Random Forest       | 0.7093  | 0.68          | 0.71      | 0.71   |
| Decision Tree       | 0.7083  | 0.68          | 0.71      | 0.71   |
| XGBoost             | 0.6860  | 0.62          | 0.73      | 0.69   |
| LightGBM            | 0.6849  | 0.62          | 0.72      | 0.68   |
| Gradient Boosting   | 0.6533  | 0.56          | 0.70      | 0.65   |

---

## 🔍 Findings
- **Best Performing Model**: Random Forest achieved the best balance with 70.93% accuracy and a Macro-F1 Score of 0.68.
- **Accuracy vs. Macro-F1 Score**: Both Random Forest and Decision Tree performed similarly, but Random Forest had a slight advantage in Macro-F1, indicating better performance across all incident grades.
- **Error Analysis**:
   - *Logistic Regression*: Lower recall for minority classes.
   - *XGBoost and LightGBM*: Higher precision but slightly lower recall.

---

## 🎯 Rationale for Model Selection
- **Final Model**: Random Forest was chosen for its superior balance across key metrics, making it effective for handling class imbalances in SOC tasks.
- **Comparison**: XGBoost and LightGBM excelled in precision but lacked recall, making them less suitable for capturing all incidents in SOCs.

---

## 🔧 Model Improvement Suggestions
1. **Hyperparameter Tuning**: Use Grid Search or Random Search to optimize parameters for Random Forest.
2. **Cross-Validation**: Implement k-fold cross-validation for better robustness.
3. **Feature Engineering**: Explore interactions and contextual information from features like `EntityType` and `Category`.

---

## 🏆 Conclusion
The project showcases the power of machine learning in cybersecurity, with the Random Forest model enabling SOCs to prioritize incident response effectively. Further improvements in tuning and feature engineering could enhance support for real-time threat management.

---

##  **presented by!** S.Mohammed Riyaskhan
