# Heart Disease Prediction Using Clinical Data

## Project Overview
This project explores clinical and demographic factors associated with heart disease and applies machine learning models to predict the presence of heart disease using structured patient data.

The focus is on:
- Understanding key predictors through exploratory analysis
- Examining categorical associations using normalized crosstabs
- Comparing classification models using ROC–AUC

## Objective
To build and evaluate machine learning models that classify whether a patient has heart disease based on routinely collected clinical features.

## Dataset
The dataset contains patient-level clinical information, including:
- **Demographics:** age, sex
- **Clinical measurements:** blood pressure, cholesterol, maximum heart rate
- **Diagnostic indicators:** exercise-induced angina, number of vessels seen on fluoroscopy, thallium test results

The target variable indicates presence or absence of heart disease.

### Column Descriptions (Data Dictionary)
| Column Name            | Description |
|------------------------|-------------|
| Age                    | Age of the patient (in years) |
| Sex                    | Gender of the patient (1 = Male, 0 = Female) |
| Chest pain type        | Type of chest pain:<br>1 = Typical angina<br>2 = Atypical angina<br>3 = Non-anginal pain<br>4 = Asymptomatic |
| BP                     | Resting blood pressure (mm Hg) |
| Cholesterol            | Serum cholesterol level (mg/dL) |
| FBS over 120           | Fasting blood sugar > 120 mg/dL (1 = True, 0 = False) |
| EKG results            | Resting electrocardiogram results:<br>0 = Normal<br>1 = ST-T wave abnormality<br>2 = Left ventricular hypertrophy |
| Max HR                 | Maximum heart rate achieved |
| Exercise angina        | Exercise-induced angina (1 = Yes, 0 = No) |
| ST depression          | ST depression induced by exercise relative to rest |
| Slope of ST            | Slope of the peak exercise ST segment |
| Number of vessels fluro| Number of major vessels (0–3) colored by fluoroscopy |
| Thallium               | Thallium stress test result (categorical diagnostic indicator) |
| Heart Disease          | Target variable:<br>Presence = Heart disease detected<br>Absence = No heart disease |

## Exploratory Data Analysis (EDA)
EDA was conducted to understand feature distributions and group differences between patients with and without heart disease. Key steps included:
- Summary statistics by heart disease status
- Visualization of numeric feature distributions
- Comparison of mean and median values across groups

## Categorical Feature Associations
Normalized crosstabulations examined associations between categorical variables and heart disease status. Notable findings:
- Exercise-induced angina strongly correlates with heart disease.
- Higher numbers of affected vessels on fluoroscopy are associated with increased heart disease risk.

## Feature Engineering
- The target variable was encoded numerically.
- All features were prepared using standard preprocessing techniques for modeling.

## Machine Learning Models
Three classification models were trained and evaluated:
- Logistic Regression
- Decision Tree
- Random Forest

Data was split into training and testing subsets to evaluate generalization performance.

## Model Evaluation Results
Models were evaluated using the Receiver Operating Characteristic – Area Under the Curve (ROC–AUC) metric.

| Model               | ROC–AUC |
|--------------------|---------|
| Logistic Regression | 0.9466 |
| Decision Tree       | 0.5000 |
| Random Forest       | 0.9206 |

**Interpretation:**
- Logistic Regression achieved the highest ROC–AUC, indicating strong discriminative ability and stable performance.
- Random Forest performed well but slightly below Logistic Regression.
- Decision Tree performed poorly, likely due to overfitting and sensitivity to limited dataset size.

## Key Insights
- Simple clinical features can reliably predict heart disease.
- Logistic Regression provides the best balance of interpretability and performance.
- Exercise-induced angina and number of affected vessels are the strongest predictors in this dataset.
- Complex models like Random Forest may offer slight performance improvements but at the cost of interpretability.

## Conclusion
This project demonstrates that heart disease prediction is feasible using routine clinical variables. Logistic Regression is the most effective model in this dataset, balancing performance with interpretability. Future work could focus on:
- Cross-validation for robust performance estimates
- Hyperparameter tuning
- Model explainability (e.g., SHAP)
- Testing on larger or external datasets

## Tools & Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
"# HeartDisease-Prediction-ML" 
