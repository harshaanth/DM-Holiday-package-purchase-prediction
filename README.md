# Holiday Package Purchase Prediction

This repository contains a Data Mining project focused on predicting whether customers will purchase a holiday package based on various factors. The analysis was conducted using Excel, employing various data mining techniques to build and evaluate the model.

## Project Overview

The goal of this project is to analyze customer data to predict the likelihood of purchasing a holiday package. By understanding key factors influencing purchase decisions, businesses can better target their marketing efforts and improve customer conversion rates.

### Business Questions:
1. **What are the key factors that influence a customer's decision to purchase a holiday package?**
2. **Can we accurately predict if a customer will buy a holiday package based on their demographics and behavior?**
3. **Which customer segments are most likely to convert, and how can they be targeted effectively?**

### Project Components:
- **Excel File (`Travel_Final.xlsx`)**: Contains the dataset and the model used for predictions.
- **Project Report (`Final Project Report - Holiday Package Purchase Prediction.pdf`)**: A detailed report explaining the project, methodology, results, and insights gained from the analysis.
- **Presentation (`DM Final Presentation.pptx`)**: A PowerPoint presentation that provides a visual summary of the project, including key findings and business recommendations.

### Content Overview:
1. **Dataset**: The dataset includes customer demographics, travel history, and other factors relevant to purchasing decisions.
2. **Model**: The model was built using Excel's data mining capabilities, with a focus on classification techniques to predict purchase likelihood.
3. **Analysis**: The project explores various data mining techniques, including decision trees and clustering, to identify patterns and predict outcomes.
4. **Insights**: Key insights and actionable recommendations are provided based on the model's results, helping businesses better understand and target their customer base.

### How to Use:
1. **Download the repository**: Clone or download the repository to access the Excel file, report, and presentation.
2. **Open the Excel File**: Explore the dataset and model in `Travel_Final.xlsx` to understand how predictions were made.
3. **Read the Report**: Review the project report for an in-depth analysis of the data and methodology.
4. **View the Presentation**: Use the PowerPoint presentation to get a quick overview of the project and its key findings.

## Detailed Project Report

### Holiday Package Purchase Prediction Project Report

**Harshaanth Thiyagaraja Kumar | Geetha Raghiphani | Charles Schlissel**

#### Table of Contents
1. **Project Description**
   - Introduction to Trips & Travel.Com's mission and the introduction of the Wellness Tourism Package.
2. **Business Questions**
   - Specific questions addressed by the project.
3. **Dependent & Independent Variables**
   - Overview of the variables used in the analysis.
4. **Data Preprocessing**
   - Handling missing data and summary of changes made.
5. **Summary Characteristics**
   - Mean, median, standard deviation, and identification of outliers.
6. **Correlation Analysis**
   - Explanation and comments on the correlation between variables.
7. **Visualization**
   - Histograms, scatterplots, and boxplots of important variables.
8. **Logistic Regression Model**
   - Description of the model, variable selection, model output, interpretation of coefficients, and training and validation summary, including lift charts and model performance metrics.
9. **Classification Tree Model**
   - Description of the model, variable usage, model output, interpretation of rules, and training and validation summary, including lift charts and model performance metrics.
10. **Neural Network Model**
    - Description of the attempted model, variable usage, model output, training summary, and training and validation summary, including lift charts and model performance metrics.
11. **Comparison Between Models**
    - Evaluation of model performance and comparison of metrics.
12. **Conclusions**
    - Decision on the best model, answers to business questions, and recommendations.
13. **Summary**
    - Reflections on the analysis process and lessons learned.

### Project Description
Trips & Travel.Com aims to expand its clientele through innovative packages. The company currently offers five packages: Basic, Standard, Deluxe, Super Deluxe, and King. Despite an 18% purchase rate among customers last year, marketing costs were high due to random outreach strategies. To improve efficiency, the company plans to launch a Wellness Tourism Package to promote healthy lifestyles. Our goal is to build a predictive model using supervised machine learning to forecast the likelihood of customers purchasing a product and identifying key determinants.

**Data Source:** Kaggle - Holiday Package Purchase Prediction.

### Business Questions
1. **Can we predict whether a specific customer will purchase the tour package?**
2. **Which customer segments are most and least likely to buy a travel package?**
3. **How can we identify groups for targeted marketing to reduce costs?**

### Dependent & Independent Variables
The goal is to predict whether a customer will purchase the travel package (Target) based on various factors (Predictor Variables). We will use classification models.

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
