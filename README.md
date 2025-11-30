# High-Cost-Patients-Project 
This project contains an end-to-end data analytics workflow for identifying and understanding high-cost healthcare patients.

It includes:
1) A Python notebook that performs data import, preprocessing and machine learning modeling.

2) A Power BI dashboard that visualizes patient characteristics, cost drivers, and risk factors.

3) An exported Excel dataset created after cleaning and feature processing steps.

The goal of the project is to support data-driven decision-making in healthcare by predicting which patients are likely to generate high future costs, and by exploring the factors that influence those costs.

# Data Preparation & Cleaning (Python)
## Data Import
<img width="1002" height="468" alt="image" src="https://github.com/user-attachments/assets/a6e2fde9-bfd4-43c4-a15f-5079e70504b6" />







## Check our data
<img width="401" height="638" alt="image" src="https://github.com/user-attachments/assets/b02ccaf5-0226-42db-89a6-11c771f2c85c" />








## Missing Data Handling and Feature Cleaning
### ✔ Duplicates
<img width="270" height="79" alt="Στιγμιότυπο οθόνης 2025-11-26 150047" src="https://github.com/user-attachments/assets/e4443238-879d-4ae9-a945-274beef7680e" />





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





### ✔ "insurance_type" column (+ create an insurance_flag column)
<img width="622" height="546" alt="image" src="https://github.com/user-attachments/assets/645c5918-00a3-4755-b194-07c69e6e6d30" />

# Exploratory Data Analysis (EDA) 
### basic statistical measurements
<img width="1000" height="312" alt="image" src="https://github.com/user-attachments/assets/93fd901f-020c-4d28-9a31-9d71e59ab7af" />





### correlation (+ heatmap)
<img width="1016" height="365" alt="image" src="https://github.com/user-attachments/assets/3d3d7cf8-e23d-4a9f-bac9-cafffbfac49b" />












<img width="985" height="827" alt="image" src="https://github.com/user-attachments/assets/38b359b8-9bc5-40b2-9958-d3a10f4f877e" />



#### the greatest correlation is between high_cost and prev_year_cost 

### outliers + plot (between the columns prev_year_cost and income)
<img width="622" height="242" alt="image" src="https://github.com/user-attachments/assets/43f9effb-527a-4c74-806f-b9adf06c6154" />






<img width="613" height="552" alt="image" src="https://github.com/user-attachments/assets/4aab84e8-88b7-40ae-b6aa-9cee5d6d9c2a" />


## Dataset After Cleaning
<img width="1848" height="646" alt="image" src="https://github.com/user-attachments/assets/3a17d195-1808-4295-b639-85b8a2450be5" />











# Logistic Regression
### ➡ Create a logistic regression model to predict which patients will fall into the high cost category.
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



### Create the model (accuracy + predictions)
<img width="1022" height="293" alt="image" src="https://github.com/user-attachments/assets/2c062d51-6443-443a-b71f-579ebb0b2039" />











<img width="997" height="465" alt="image" src="https://github.com/user-attachments/assets/8eb1638f-f3fa-4866-99e0-e6592a737e4f" />








#### accuracy: 84%
### ✔ Coefficiency (+ plot)
<img width="610" height="313" alt="Στιγμιότυπο οθόνης 2025-11-25 215206" src="https://github.com/user-attachments/assets/92067338-3287-4eef-9be7-c87a564872b8" />







<img width="591" height="598" alt="Στιγμιότυπο οθόνης 2025-11-25 215305" src="https://github.com/user-attachments/assets/e427c759-48d9-4126-bcba-3335fb29e7b3" />





### ✔ Confusion matrix
<img width="222" height="87" alt="image" src="https://github.com/user-attachments/assets/a3b778e1-05ec-48a5-8353-744758f1759a" />




### ✔ Classification report
<img width="386" height="195" alt="image" src="https://github.com/user-attachments/assets/27552b49-0ffa-4bfb-9cb0-7492033dee10" />



### ✔ Roc auc test
<img width="222" height="71" alt="image" src="https://github.com/user-attachments/assets/05f4de02-2332-43d8-8a72-fb86b57b89bf" />




## Forecast With Your Data
Example:
1) Yearly income = 23000

2) Medical costs of previous year = 500
        
3) Type of insurance = 1 (private)
         
4) Number of admissions = 2
         
5) Number of ED visits = 3
         
6) Number of comorbidities = 1


<img width="1020" height="743" alt="image" src="https://github.com/user-attachments/assets/8ea8211b-bc0f-4258-a079-b7c8320034b7" />











# Power BI Dashboard 
<img width="1368" height="734" alt="Στιγμιότυπο οθόνης 2025-11-25 221745" src="https://github.com/user-attachments/assets/44bfa13e-e61a-43bd-9559-8feca55ce5f9" />









## This Power BI report provides a rich analytical view of the dataset, including:
### ✔ Cost Analytics

Total vs. high-cost patient spending

Previous year cost distribution

Cost drivers and demographic breakdowns


### ✔ Patient Characteristics

Age, gender, BMI, income

Smoking status

Comorbidity counts


### ✔ Utilization Metrics

Hospital admissions

Emergency department visits

Insurance coverage patterns
