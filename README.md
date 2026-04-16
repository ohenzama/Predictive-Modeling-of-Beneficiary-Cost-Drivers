# Predictive-Modeling-of-Beneficiary-Cost-Drivers

<h2>Tools Used</h2>

- <b>R:</b> Data Cleaning, Exploratory Data Analysis, Multiple Linear Regression
- <b>POWER BI :</b> Dashboarding / EDA

<h2>Dataset Details</h2> 

<b>Goal: </b> Use the given features to accurately predict insurance costs, which is the **charges** column. 

<b>Size: </b> [1,338 × 7]

<br />
<br />
<b>Features: </b>
**age:** age of primary beneficiary

**sex:** male or female

**bmi**: bmi of beneficiary

**children:** number of children covered by health insurance

**region:** beneficiary’s residential area in the US, northeast, southwest, northwest

**charges:** individual medical costs billed by health insurance

<br />
<br />


<h2>Data Cleaning and Pre-Processing</h2>

- No NA values observed, and no anomalies detected in the descriptive summaries 

<h2>Exploratory Data Analysis</h2>

- Verified linear relationship between each predictor and response variable
- Low correlation found between predictors, verifying each new predictor will bring enough unique information to the model


<h2>Multiple Linear Regression Modelling </h2>

- Split data into a train (80%) and test set
- Created a model including main effects and all two-way interaction combinations, then  performed stepwise model selection to find a better subset of predictor variables for the charges response.
- Akaike Information Criterion (AIC) was used to compare models, since AIC is better for prediction, and this specific project prioritized predictive accuracy.
- The diagnostics plots showed a residual plot adequately scattered around 0, constant variance. The standardized residuals in the qq plot were skewed at the end, but excused by the central limit theorem.
- The resulting model chosen had an Adjusted R squared value of 0.8421, suggesting decent model fit and performance.

<h2>Key Insights</h2>

- Age is psitively correlated with estimated health insurance cost. Specifically, keeping other variables fixed, a one unit increase in the beneficiary’s age increased the estimated insurance cost by 255.
- Number of children is positively correlated with estimated health insurance cost. Specifically, keeping other variables fixed, a one unit increase in the beneficiary’s number of children increased the estimated insurance cost by 704.68.
- Interactions between bmi and smoking status increases the beneficiary’s health insurance costs. 

<h2>Dashboard</h2>

I used my results from my MLR model to guide the way in which I built my dashboard.  I wanted it to be reflective of my results, so I put an emphasis on the significant coefficients found by the model, and included sliders for the significant interaction terms:

https://github.com/user-attachments/assets/31ad2574-bb80-49ee-b4e0-b2024b95610b





<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
