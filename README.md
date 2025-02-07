# **Recursive Feature Elimination (RFE) for Diabetes Prediction**

## **Introduction to RFE**
Recursive Feature Elimination (RFE) is a feature selection technique that iteratively removes the least important features to enhance model performance and interpretability. It helps identify the most significant predictors while reducing overfitting and computational complexity.

## **Overview**
This project applies RFE using a linear regression model to the diabetes dataset from Scikit-learn. The goal is to determine the optimal subset of features that best predicts diabetes progression while maintaining high model accuracy.

## **Requirements**
To run this project, install the necessary dependencies:
- sci-kit-learn
- NumPy
- pandas
- matplotlib
- seaborn
## **Features of the Diabetes Dataset**
The dataset includes the following features:

- Pregnancies: Number of times pregnant
- Glucose: Plasma glucose concentration (mg/dL)
- BloodPressure: Diastolic blood pressure (mm Hg)
- SkinThickness: Triceps skinfold thickness (mm)
- Insulin: Serum insulin (mu U/ml)
- BMI: Body mass index (weight in kg/height in m²)
- DiabetesPedigreeFunction: Diabetes pedigree function (a function of the family history of diabetes)
- Age: Age (years)
- Outcome: Class variable (0 or 1, where 1 indicates diabetes)

## **Results**
After applying Recursive Feature Elimination (RFE), the following features were selected as the most important predictors of diabetes progression:
Optimal Number of Features Identified: 2
- Most Important Features:
  - s1 (Serum Cholesterol Level): 931.49
  - s5 (Log Serum Triglycerides Level): 736.20
  - BMI (Body Mass Index): 542.43
  Optimal Number of Features Identified: 2
- R² Score of Initial Model: 0.4526
- Final Feature Selection: Highlighted significant metabolic factors influencing diabetes progression.
These features significantly reduced the complexity of the model while maintaining a high level of accuracy compared to using the full feature set. Eliminating less relevant features optimized the model's performance and reduced overfitting.

## **Performance Metrics**
R² (Coefficient of Determination): Shows the proportion of variance explained by the selected features.

## **Author**
- Jayana Sarma
  
  ---
For more details, check the **report.pdf** or explore the **RFE_Assignment.ipynb** notebook.
