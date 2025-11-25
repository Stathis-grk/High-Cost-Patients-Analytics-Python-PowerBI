# High-Cost-Patients-Analytics
This project contains an end-to-end data analytics workflow for identifying and understanding high-cost healthcare patients.

It includes:
1) A Python notebook that performs data import, preprocessing, feature engineering, and machine learning modeling.

2) A Power BI dashboard that visualizes patient characteristics, cost drivers, and risk factors.

3) An exported Excel dataset created after cleaning and feature processing steps.

The goal of the project is to support data-driven decision-making in healthcare by predicting which patients are likely to generate high future costs, and by exploring the factors that influence those costs.

# Data Preparation & Cleaning (Python)
## Data Import
<img width="1093" height="621" alt="image" src="https://github.com/user-attachments/assets/9247b2ef-9271-498f-9723-cc1fd6825f57" />






## Check our data
<img width="401" height="638" alt="image" src="https://github.com/user-attachments/assets/b02ccaf5-0226-42db-89a6-11c771f2c85c" />








## Missing Data Handling and Feature Cleaning
### ✔ "sex" column
<img width="472" height="197" alt="image" src="https://github.com/user-attachments/assets/5a756e22-a0b0-4fc6-9308-11cbd3b587b8" />





### ✔ "age" column
<img width="496" height="457" alt="image" src="https://github.com/user-attachments/assets/8931c6f0-1dae-4204-a1be-a01741aba5ca" />




### ✔ "smoking_status" column
<img width="497" height="291" alt="image" src="https://github.com/user-attachments/assets/52423362-444e-4397-84f5-c54e0dd1ea75" />






### ✔ "bmi" column
<img width="485" height="323" alt="image" src="https://github.com/user-attachments/assets/dca56434-9f3c-4cfb-ab29-069adde7bc9f" />






### ✔ "chronic_conditions" column
<img width="581" height="292" alt="image" src="https://github.com/user-attachments/assets/f223fd51-4786-46fa-8487-8bc68b219bea" />






### ✔ "income" column
<img width="547" height="325" alt="image" src="https://github.com/user-attachments/assets/f6f65ad6-77a7-45d5-ad0c-a8a73fb0bbf5" />





### ✔ "insurance_type" column (+ create a insurance_flag column)
<img width="622" height="546" alt="image" src="https://github.com/user-attachments/assets/645c5918-00a3-4755-b194-07c69e6e6d30" />

# Exploratory Data Analysis (EDA) 
### basic statistical measurements
<img width="1000" height="312" alt="image" src="https://github.com/user-attachments/assets/93fd901f-020c-4d28-9a31-9d71e59ab7af" />





### correlation (+ heatmap)
<img width="1016" height="365" alt="image" src="https://github.com/user-attachments/assets/3d3d7cf8-e23d-4a9f-bac9-cafffbfac49b" />












<img width="985" height="827" alt="image" src="https://github.com/user-attachments/assets/38b359b8-9bc5-40b2-9958-d3a10f4f877e" />



#### ⭐ the greatest autocorrelation is between high_cost and prev_year_cost 

### outliers + plot (between the columns prev_year_cost and income)
<img width="622" height="242" alt="image" src="https://github.com/user-attachments/assets/43f9effb-527a-4c74-806f-b9adf06c6154" />






<img width="613" height="552" alt="image" src="https://github.com/user-attachments/assets/4aab84e8-88b7-40ae-b6aa-9cee5d6d9c2a" />


## Dataset After Cleaing
<img width="1848" height="646" alt="image" src="https://github.com/user-attachments/assets/3a17d195-1808-4295-b639-85b8a2450be5" />











# Logistic Regression
## create a logistic regression model to predict which patients will fall into the high cost category.
1) high_cost = 1 ~ high cost patient
2) high_cost = 0 ~ low cost patient

### Inputs (Features)

Income

Previous year cost

Insurance flag

Number of admissions

Number of ED visits

Comorbidity count



### Outputs

Binary prediction (High-Cost vs. Not High-Cost)




<img width="743" height="218" alt="image" src="https://github.com/user-attachments/assets/26c79487-182f-46d3-b074-2573ed433d38" />
