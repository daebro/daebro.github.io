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
   - Used **Inverse Propensity Weighting (IPW)**
