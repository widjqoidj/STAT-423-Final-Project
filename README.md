# **STAT-423 Final Project**  
**Team: Degree of Freedom**  

## **Project Title: Impact of Sleep Patterns on Productivity and Well-Being**  

### **Dataset Information**  
- **Dataset Name**: Sleep Cycle and Productivity  
- **Source**: [Kaggle](https://www.kaggle.com/datasets/adilshamim8/sleep-cycle-and-productivity)  
- **Description**: This dataset includes various statistics relating to sleep and biological metrics of subjects, such as sleep quality, productivity, mood, and other lifestyle factors.
- **Total Observations**: 5000  
- **Total Variables**: 15  
  
### **Variables**  
#### **Categorical Variables** (All self-reported scores are on a 1-10 scale):  
- `Date`: Date of data collection  
- `Person_ID`: Unique identifier for each individual  
- `Age`: Age of the person (18-60 years)  
- `Gender`: Male, Female, or Other  
- `Sleep Quality`: Self-reported sleep quality  
- `Productivity Score`: Self-reported productivity score  
- `Mood Score`: Self-reported mood score  
- `Stress Level`: Self-reported stress level  
  
#### **Continuous Variables**  
- `Sleep Start Time`  
- `Sleep End Time`  
- `Total Sleep Hours`  
- `Exercise (mins/day)`  
- `Caffeine Intake (mg)`  
- `Screen Time Before Bed (mins)`  
- `Work Hours (hrs/day)`  
  
---  
## **Research Questions**  
1. **Which factors contribute the most to sleep quality?**  
2. **Is there a linear relationship between sleep consistency (variance in sleep duration) and productivity?**  
3. **Does screen time before bed negatively affect sleep quality?**  
4. **Does caffeine intake moderate the relationship between stress level and sleep quality?**  
  
---  
## **Methodology**  
### **Question 1: Factors Influencing Sleep Quality**  
#### **Steps**:  
1. **Data Preparation**: Load and clean dataset, transform variables as necessary.  
2. **Exploratory Data Analysis (EDA)**: Plot variables against sleep quality to analyze correlations.  
3. **Multiple Linear Regression**: Develop a full model and reduced models for comparison.  
4. **Model Diagnostics**: Check normality using residual plots and Q-Q plots.  
5. **Hypothesis Testing**: Conduct statistical tests with a significance level of 0.05.  
  
#### **Regression Model**:  
$$ Sleep Quality = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \beta_3 X_3 + \beta_4 X_4 + \epsilon $$  
where predictors \(X_1, X_2, X_3, X_4\) are selected based on EDA results.  
  
---  
### **Question 2: Sleep Consistency and Productivity**  
#### **Steps**:  
1. **Data Preparation**: Compute sleep consistency as variance in sleep duration per person.  
2. **EDA**: Scatter plots of sleep consistency vs. productivity, add regression line.  
3. **Linear Regression**: Fit a model with productivity as the dependent variable.  
4. **Model Diagnostics**: Residual vs. fitted values plot, Q-Q plot, homoscedasticity check.  
5. **Correlation Analysis**: Compute Pearson correlation coefficient.  
  
#### **Regression Model**:  
$$ Productivity = \beta_0 + \beta_1 (Sleep Consistency) + \epsilon $$  
  
---  
### **Question 3: Screen Time and Sleep Quality**  
#### **Steps**:  
1. **Data Preparation**: Clean and preprocess screen time and sleep quality variables.  
2. **EDA**: Scatter and box plots, correlation heatmaps.  
3. **Hypothesis Testing**:  
   - \( H_0 \): Screen time before bed does not affect sleep quality.  
   - \( H_1 \): Screen time before bed negatively affects sleep quality.  
4. **Multiple Linear Regression**: Adjust for control variables (age, stress, caffeine intake).  
5. **Model Diagnostics**: Residual analysis, normality check.  
  
#### **Regression Model**:  
$$ Sleep Quality = \beta_0 + \beta_1 (Screen Time) + \sum \beta_j (Control_j) + \epsilon $$  
  
---  
### **Question 4: Caffeine as a Moderator Between Stress and Sleep Quality**  
#### **Steps**:  
1. **Data Preparation**: Standardize stress level, caffeine intake, and sleep quality.  
2. **EDA**: Scatter plots for stress vs. sleep quality and caffeine vs. sleep quality.  
3. **Hypothesis Testing**:  
   - \( H_0 \): Caffeine does not moderate the stress-sleep quality relationship.  
   - \( H_1 \): Caffeine moderates the relationship.  
4. **Multiple Regression Model with Interaction Term**  
5. **Model Diagnostics**: Residual analysis, normality check, variance inflation factor (VIF) for multicollinearity.  
  
#### **Regression Model**:  
$$ Sleep Quality = \beta_0 + \beta_1 (Stress) + \beta_2 (Caffeine) + \beta_3 (Stress \times Caffeine) + \epsilon $$  
  
- If \( \beta_3 > 0 \), caffeine reduces the negative effect of stress on sleep quality.  
- If \( \beta_3 < 0 \), caffeine worsens the negative effect of stress on sleep quality.  
  
---  
## **Conclusion**  
- We will analyze model outputs to determine significant relationships.  
- If variables show a strong correlation and significance, we conclude their effect on sleep quality or productivity.  
- Visualizations and statistical results will be included in the final report.  
  
---  
## **Project Contributors**  
- Team: **Degree of Freedom**  
- Course: **STAT-423**  
- Institution: **[Your University Name]**  
  
---  
## **License**  
This project is for academic purposes and follows standard open-source licensing practices.  
  
---  
## **Contact**  
For any questions or collaborations, feel free to reach out via GitHub Issues.  
