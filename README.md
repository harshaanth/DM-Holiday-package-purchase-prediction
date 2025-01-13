# Project Overview

Trips & Travel.Com aims to expand its clientele through innovative packages. The company currently offers five packages: Basic, Standard, Deluxe, Super Deluxe, and King. Despite an 18% purchase rate among customers last year, marketing costs were high due to random outreach strategies. To improve efficiency, the company plans to launch a Wellness Tourism Package to promote healthy lifestyles.

The goal of this project is to analyze customer data to predict the likelihood of purchasing a holiday package. By understanding key factors influencing purchase decisions, businesses can better target their marketing efforts and improve customer conversion rates.

### Business Questions:
1. **What are the key factors that influence a customer's decision to purchase a holiday package?**
2. **Can we predict if a customer will buy a holiday package based on their demographics and behavior?**
3. **Which customer segments are most likely to convert, and how can they be targeted effectively?**

### Dependent & Independent Variables
The goal is to predict whether a customer will purchase the travel package (Target) based on various factors (Predictor Variables). We will use classification models.

Click on the link to view the presentation: 

### Data Preprocessing
**Handling Missing Data:**
- Records Processed: 4128
- Records Deleted: 760
- 760 records with missing values were deleted.

### Summary Characteristics
Outliers were detected in the following variables:
- DurationOfPitch
- NumberOfFollowups
- NumberOfTrips
- MonthlyIncome

### Correlation Analysis
- **NumberOfChildrenVisiting** is highly correlated with **NumberOfPersonVisiting**.
- **MonthlyIncome** is highly correlated with **Age**.

### Visualization
- **Histograms:**
  - Most variables are not skewed, except **DurationOfPitch** and **PreferredPropertyStar**, which are skewed to the right.
- **Scatterplots:**
  - No significant trend between **PitchSatisfactionScore** and other numeric variables.
- **Boxplots:**
  - Outliers are present in **MonthlyIncome**, **NumberOfFollowups**, and **DurationOfPitch**.

### Logistic Regression Model
**Model Selection:**
- Logistic Regression was chosen due to the categorical nature of the target variable.

**Best Subset Selection:**
- Subset 13 was selected with 13 coefficients based on optimal Mallow's Cp and high probability.

**Model Performance:**
- **Training AUC:** 0.816
- **Validation AUC:** 0.7863
- **Overall Accuracy:** 70.68%
- **Specificity:** 0.693
- **Sensitivity (Recall):** 0.7588

**Variables Selected:**
- DurationOfPitch, NumberOfFollowups, PreferredPropertyStar, Passport, MonthlyIncome, TypeofContact, CityTier, Occupation, ProductPitched, and MaritalStatus.

### Comparison Between Models
- Logistic Regression performed consistently across training and validation datasets, with the best balance of accuracy and recall.

### Conclusions
- **Best Model:** Logistic Regression with a cutoff of 0.1506.
- **Answers to Business Questions:**
  - Customers more likely to purchase include younger individuals, those with passports, and those from City Tier 3.
  - Customers less likely include older individuals, those without passports, and those pitched the deluxe product.
- **Recommendations:** Target marketing efforts on younger customers with passports and those from lower city tiers.

---

This repository serves as a comprehensive resource for understanding how data mining techniques can be applied in Excel to solve real-world business problems.
