# 📊 A Causal and Statistical Exploration of the 2022 U.S. Primary Elections

## 🔎 Project Description
This project analyzes the **2022 congressional primary elections** using candidate-level data to explore two main research questions:
1. **RQ1:** Which candidate characteristics (race, gender, party, incumbency, endorsements) are statistically associated with higher primary vote share?
2. **RQ2:** Does receiving at least one political endorsement causally increase a candidate’s vote percentage?

The project combines **statistical hypothesis testing** with **causal inference methods** to uncover both associations and potential causal effects in electoral outcomes.

---

## ⚙️ Workflow
1. **Data Cleaning & Preprocessing**
   - Merged Democratic and Republican candidate datasets
   - Handled missing values in endorsements, race, and vote share
   - Converted categorical variables into binary/one-hot encoded features  

2. **Exploratory Data Analysis (EDA)**
   - Visualized vote share distributions by gender and race
   - Measured correlation between endorsements and primary vote share (ρ ≈ 0.29)

3. **RQ1: Statistical Hypothesis Testing**
   - Ran **t-tests, chi-squared tests, and ANOVA** across candidate traits
   - Applied **Bonferroni and Benjamini-Hochberg corrections** for multiple testing
   - Assessed statistical power for endorsement variable (>99%)

4. **RQ2: Causal Inference**
   - Framed endorsements as a treatment variable
   - Used **Inverse Propensity Weighting (IPW)** with logistic regression to estimate causal effect
   - Trimmed propensity scores to address positivity violations
   - Constructed **95% bootstrapped confidence intervals** for robustness

---

## 📂 Datasets
- **FiveThirtyEight’s 2022 Primary Project**: Candidate demographics, election results, endorsements  
- **Endorsement Data**: Additional information on endorsers (e.g., EMILY’s List, Bernie Sanders, Donald Trump)  
- Each row corresponds to one congressional primary candidate, with attributes like party, gender, race, incumbency, endorsements, and primary vote percentage.

---

## 🧮 Models and Methods
- **Hypothesis Testing**: Two-sample t-tests, chi-squared tests, ANOVA  
- **Multiple Testing Adjustments**: Bonferroni & Benjamini-Hochberg corrections  
- **Causal Model**: Inverse Propensity Weighting (IPW) with logistic regression  
- **Validation**: Bootstrapped confidence intervals, overlap diagnostics on propensity scores

---

## 📈 Key Results
- **RQ1 (Associations):**
  - Endorsements, incumbency, race, and party affiliation all showed **statistically significant effects** on vote share.  
  - Bernie Sanders’ endorsements had especially strong positive association.  
  - Gender and EMILY’s List endorsements were not statistically significant.  

- **RQ2 (Causal Effect of Endorsements):**
  - Naive Average Treatment Effect (ATE): **+38.2 percentage points**  
  - After adjusting for confounders with IPW: **+25.05 percentage points**  
  - 95% CI: **[14.88, 36.47]**, confirming a significant positive causal effect.  

---

## 🏆 My Contributions
- Co-led **RQ1 analysis**: designed hypothesis tests, applied multiple testing corrections, ran statistical power analysis.  
- Assisted with **data preprocessing & feature engineering** (one-hot encoding, handling missing endorsements).  
- Collaborated on **RQ2 workflow**, including propensity score modeling and validation with overlap/weight diagnostics.  
- Consolidated results into final report and visualizations.  

---

## 📌 Next Steps
- Explore **heterogeneous treatment effects** of specific high-profile endorsements (e.g., Trump vs. PACs).  
- Incorporate **campaign finance and polling data** as additional confounders.  
- Extend causal framework to **general election outcomes** across multiple years.  

---

## 📓 Notebooks
- [RQ1 Analysis](./primary_elections_RQ1.ipynb)  
- [RQ2 Analysis](./primary_elections_RQ2.ipynb)  
