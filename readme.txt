
#  Healthcare Risk Factors Analysis

**Exploratory Data Analysis using Python, Pandas & Seaborn**

---

##  Project Overview

This project performs a comprehensive **Exploratory Data Analysis (EDA)** on a healthcare dataset to examine how **physiological indicators, lifestyle behaviors, and medical risk categories** interact. The primary objective is to uncover meaningful patterns that help interpret patient health risk profiles and understand factors associated with chronic disease conditions.

The analysis focuses on:

* Understanding data structure and quality
* Exploring distributions of health indicators
* Investigating relationships between lifestyle and medical risks
* Identifying trends that may assist in preventive healthcare interpretation

This is an analytical project aimed at **insight discovery**, not predictive modeling.

---


##  Objectives

* Study the relationship between **BMI and medical conditions**
* Examine how **Lifestyle Index** relates to glucose and blood pressure risk
* Understand the impact of **family history** on disease prevalence
* Explore interactions among **behavioral factors** (activity, diet, stress, sleep)
* Analyze correlations between physiological variables

---


Healthcare Risk Factors Dataset – Column Summary

---

-  Age

Definition: Age of the patient in years.
Why it matters: Age affects risk for many medical conditions; older people are more likely to have chronic diseases.
Typical ranges / interpretation:

0–18 → Child / adolescent

19–40 → Young adult

41–65 → Middle-aged adult (increased risk for chronic conditions)

65+ → Older adult (higher risk for diabetes, hypertension, cardiovascular disease)
Daily life impact: Risk factor for chronic diseases and complications increases with age.



---

-  Gender

Definition: Biological sex of the patient (Male, Female).
Why it matters: Some conditions have different prevalence between genders (e.g., men have higher risk of heart disease, women more prone to osteoporosis).
Typical values: Male, Female (sometimes blank in dataset).
---

-  Medical Condition

Definition: Diagnosed medical condition. Categories include Diabetes, Hypertension, Obesity, Cancer, Asthma, Arthritis, Healthy.
Why it matters: This is the target variable for predicting health risk.
Daily life impact: Determines treatment, lifestyle changes, and risk management strategies.


---

-  Glucose (mg/dL)

Definition: Blood sugar level. Indicates current energy metabolism.
Ranges:

Normal: 70–99

Prediabetes: 100–125

Diabetes: ≥126
Impact: High glucose → risk of diabetes; low glucose → risk of hypoglycemia.
---

-  Blood Pressure (mmHg)

Definition: Systolic blood pressure. Measures pressure on arteries.
Ranges (systolic):

Normal: <120

Elevated: 120–129

Hypertension Stage 1: 130–139

Hypertension Stage 2: ≥140
Impact: High BP increases risk for heart attack, stroke, and kidney disease.
---

-  BMI (kg/m²)

Definition: Body Mass Index, a measure of weight relative to height.
Ranges:

Underweight: <18.5

Normal: 18.5–24.9

Overweight: 25–29.9

Obese: ≥30
Impact: High BMI increases risk for diabetes, heart disease, hypertension.
---

-  Oxygen Saturation (%)

Definition: Percentage of oxygen in the blood.
Ranges:

Normal: 95–100%

Below normal: <95% (may indicate lung or heart problems)
Impact: Low oxygen saturation can lead to fatigue, shortness of breath, or organ damage.
---

-  LengthOfStay (days)

Definition: Number of days the patient stayed in hospital / healthcare facility.
Ranges:

Short stay: 1–3 days

Medium stay: 4–7 days

Long stay: 8+ days
Impact: Longer stays usually indicate severe or complicated conditions.
---

-  Cholesterol (mg/dL)

Definition: Total cholesterol level. Indicator of heart disease risk.
Ranges:

Desirable: <200

Borderline high: 200–239

High: ≥240
Impact: High cholesterol increases risk of heart attack and stroke.

---

-  Triglycerides (mg/dL)

Definition: Fat content in blood.
Ranges:

Normal: <150

Borderline high: 150–199

High: 200–499

Very high: ≥500
Impact: High triglycerides contribute to cardiovascular disease.
---

-  HbA1c (%)

Definition: Average blood sugar over 2–3 months.
Ranges:

Normal: <5.7%

Prediabetes: 5.7–6.4%

Diabetes: ≥6.5%
Impact: Reflects long-term glucose control; high HbA1c → risk of diabetic complications.
---

-  Smoking (0/1)

Definition: Smoking status. 1 = Smoker, 0 = Non-smoker.
Impact: Increases risk of heart disease, stroke, cancer, and lung diseases.
---

-  Alcohol (0/1)

Definition: Alcohol consumption. 1 = Drinks alcohol, 0 = Does not.
Impact: Excessive alcohol can increase risk for liver disease, heart disease, and some cancers.
---

-  Physical Activity (score / scale)

Definition: Level of physical activity (numeric score).
Impact: Higher activity reduces risk of obesity, diabetes, heart disease. Negative or low scores may indicate sedentary lifestyle.
---

-  Diet Score

Definition: Numeric score of diet quality. Higher = healthier diet.
Impact: Poor diet increases risk for obesity, diabetes, cardiovascular disease.
---
-  Family History (0/1)

Definition: Indicates whether a patient has family history of disease. 1 = Yes, 0 = No.
Impact: Genetics can predispose people to diabetes, heart disease, or cancer.


---

-  Stress Level (0–10)

Definition: Numeric scale of stress.
Impact: High stress affects heart health, glucose control, sleep, and overall well-being.

---

- Sleep Hours (hours/day)

Definition: Average daily sleep duration.
Ranges:

Healthy: 7–9 hours

Insufficient: <7 hours

Oversleep: >9 hours
Impact: Poor sleep increases risk of obesity, diabetes, hypertension, and mood disorders.
---

-  random_notes (Text)

Definition: Miscellaneous text like lorem, ipsum, ###.
Impact: Not useful for analysis; can be dropped.
---

-  noise_col (Numeric)

Definition: Random numeric noise column.
Impact: Synthetic / irrelevant for analysis; can be dropped.

---

##  Project Structure

Healthcare_Risk_Factors_EDA/
│
├── Healthcare Risk Factors Dataset/
│   └── dirty_v3_path.csv        # Raw dataset
│
├── data_cleaning_hrf.ipynb      # Data cleaning and preprocessing
├── cleaned_hrf.csv              # Final dataset used for analysis
├── EDA_HRF.ipynb                # Exploratory Data Analysis notebook
---

##  Data Preparation

Data preparation was carried out in **data_cleaning_hrf.ipynb** to ensure analytical reliability.

### Cleaning Steps Performed:

* Missing value assessment
* Duplicate record identification
* Data type validation and corrections
* Range sanity checks for clinical measurements
* Creation of derived categorical features:

  * BMI Category
  * BP Category
  * Glucose Risk
  * Lifestyle Level

The processed dataset was saved as **`cleaned_hrf.csv`** for use in analysis.

---

##  Exploratory Data Analysis

The EDA notebook (**EDA_HRF.ipynb**) investigates the dataset through structured analysis.

### 1 Distribution Analysis

Understanding overall dataset composition:

* BMI category distribution
* Frequency of medical conditions
* Family history prevalence

### 2 Lifestyle and Health Risk

Evaluates how lifestyle influences clinical risk factors:

* Lifestyle Index vs Glucose Risk
* Lifestyle Index vs Blood Pressure Category
* Lifestyle variation across age and gender

### 3  BMI and Disease Association

* BMI vs Medical Condition comparison
* Relationship between BMI category and lifestyle quality

### 4 Correlation Analysis

A correlation heatmap was used to explore relationships among numerical variables, including:

* Glucose
* Cholesterol
* Triglycerides
* HbA1c
* BMI
* Lifestyle Index
* Sleep and stress metrics

### 5 Behavioral Factors Interaction

Exploration of how:

* Physical Activity
* Diet Score
* Stress Level
* Sleep Hours
  contribute to the Lifestyle Index.

---

##  Key Insights

* Elevated BMI levels are associated with higher occurrence of chronic medical conditions.
* Lower Lifestyle Index scores are linked with increased glucose and blood pressure risk.
* Family history appears related to greater disease prevalence.
* Behavioral habits such as physical activity and diet significantly influence lifestyle health metrics.
* Several physiological indicators show meaningful interrelationships.

---

##  Limitations

* Observational data limits causal inference.
* Lifestyle Index is a composite metric and may not capture all lifestyle aspects.
* Findings are exploratory and intended for analytical interpretation.

---

## Tools & Libraries

* **Python**
* **Pandas** – Data manipulation and preprocessing
* **Matplotlib & Seaborn** – Visualization
* **Jupyter Notebook** – Analysis environment

---

## Conclusion

This project demonstrates how EDA can be applied to healthcare data to reveal connections between lifestyle behavior, biological indicators, and disease risk categories. The insights emphasize the importance of healthy lifestyle patterns and early identification of risk indicators in preventive healthcare analysis.

