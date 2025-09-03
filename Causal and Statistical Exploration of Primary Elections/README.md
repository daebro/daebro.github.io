# A Causal and Statistical Exploration of the 2022 Primary Election

##� Project Overview
This project explores how candidate characteristics and endorsements affected outcomes in the 2022 U.S. primary elections.  
We combine **statistical hypothesis testing (RQ1)** and **causal inference (RQ2)** to answer two core questions:

- **RQ1:** Which candidate characteristics are associated with higher vote share in U.S. primary elections?  
- **RQ2:** Does having at least one endorsement *cause* an increase in a candidate’s primary vote percentage?  

---

## Workflow Summary
1. **Data Cleaning & Feature Engineering**  
   - Converted vote share values into numeric percentages  
   - Encoded endorsements into binary variables  
   - One-hot encoded categorical features (e.g., race)  

2. **Exploratory Data Analysis (EDA)**  
   - Distribution of vote shares  
   - Vote share by gender, race, and party  
   - Correlation between endorsements and vote share  

3. **RQ1: Statistical Testing**  
   - T-tests and ANOVA on candidate traits  
   - Multiple-testing corrections (Bonferroni & FDR)  

4. **RQ2: Causal Inference**  
   - Inverse Propensity Weighting (IPW) with logistic regression  
   - Adjusted for confounders (incumbency, gender, opposition, party, race, office)  
   - Estimated Average Treatment Effect (ATE)  

---

## Dataset
- Source: [FiveThirtyEight – Primary Project 2022](https://github.com/fivethirtyeight/data/tree/master/primary-project-2022)  
- Granularity: candidate-level (each row = one candidate)  
- Key variables: demographics, endorsements, vote share  

---

## Results

### RQ1 (Statistical Testing)
- **Significant traits:** incumbency, party affiliation, race, and Sanders endorsement  
- **Non-significant traits:** gender, EMILY’s List endorsement  
- Corrections confirmed 4/6 tests remained significant  

### RQ2 (Causal Inference)
- **Naive ATE:** +38.2 percentage points  
- **Adjusted ATE (IPW):** +25.05 percentage points  
- **95% CI:** [14.88, 36.47]  

**Conclusion:** Endorsements have a strong causal effect on candidate vote share, but candidate characteristics still matter.  

---


##  Reproducibility
To run the notebook:

```bash
git clone https://github.com/daebro/election-analysis.git
cd election-analysis
pip install -r requirements.txt
jupyter notebook notebooks/Data_Analysis_Primary_Elections.ipynb
