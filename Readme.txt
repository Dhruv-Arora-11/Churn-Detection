End-to-End Telco Customer Churn Prediction
This project is a complete, end-to-end machine learning solution designed to predict customer churn for a fictional telecommunications company. The primary goal is to identify customers who are likely to cancel their subscriptions, allowing the business to proactively take retention measures. The final model is deployed as an interactive web application.

Customer churn is a critical problem for subscription-based businesses, as acquiring new customers is far more expensive than retaining existing ones. This project aims to solve this by building a model that can accurately predict churn, allowing the company to:

Identify high-risk customer segments.

Implement targeted retention campaigns.

Quantify the potential financial impact of churn and the value of intervention.

Tech Stack
Data Analysis & Manipulation: Pandas, NumPy

Data Visualization: Seaborn, Matplotlib

Machine Learning: Scikit-learn, Imbalanced-learn (for SMOTE)

Model Deployment: Streamlit

Cloud Hosting: Hugging Face Spaces

Version Control: Git & GitHub

Project Workflow
The project followed a standard end-to-end machine learning lifecycle:

Exploratory Data Analysis (EDA): Analyzed the dataset to uncover key patterns and relationships between customer attributes and churn.

Feature Engineering: Created new, more predictive features based on EDA insights, such as Is_Independent and TenureGroup, to capture customer personas.

Preprocessing & Modeling: Built a robust scikit-learn pipeline to handle scaling of numerical features, one-hot encoding of categorical features, and balancing the dataset with SMOTE.

Hyperparameter Tuning: Used GridSearchCV with 5-fold stratified cross-validation to find the optimal parameters for a RandomForestClassifier.

Model Evaluation: Assessed the final model's performance on a hold-out test set, focusing on metrics relevant to the imbalanced nature of the data (Recall, F1-Score, ROC AUC).

Deployment: Saved the final trained pipeline and built an interactive web application with Streamlit, which was then deployed on Hugging Face Spaces.

Key Findings & Model Performance
EDA Insights
My analysis revealed several key drivers of churn:

Customers with Month-to-month contracts are significantly more likely to churn.

Low tenure is the strongest indicator of churn risk.

Customers using Fiber optic internet and paying by electronic check also show higher churn rates.

Final Model Performance
The final tuned RandomForestClassifier achieved the following results on the unseen test set:

Metric	Score
ROC AUC Score	0.84
Churn Recall	0.68
Churn F1-Score	0.61
Overall Accuracy	77%

The model successfully improved recall for the churn class, correctly identifying 68% of all customers who were about to leave.

Business Impact
By translating the model's performance into business value, I estimated that by proactively targeting the at-risk customers identified by the model, the company could save over $64,000 in annual recurring revenue.

How to Run
To run this project locally, follow these steps:

Clone the repository:

git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
Create a virtual environment and install dependencies:

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
pip install -r requirements.txt
Run the Streamlit app:

streamlit run app.py
The application will then be available in your browser at http://localhost:8501.