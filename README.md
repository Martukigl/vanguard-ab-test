# Vanguard-ab-test
A/B testing analysis of Vanguard’s digital process redesign, including EDA, KPIs, hypothesis testing, and visualization.
---
## 🛠️ Tech Stack & Tools

![Python](https://img.shields.io/badge/Python-3.10-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)
![uv](https://img.shields.io/badge/uv-Environment-4CAF50)
![Tableau](https://img.shields.io/badge/Tableau-Data%20Visualization-E97627?logo=tableau&logoColor=white)


---

## Project Overview

We are a team of data analysts who work with data from start to finish, cleaning it, analyzing it, and presenting insights in a clear and meaningful way.


The presentation is available (Insert when done)
---

## 💾 Data Sources

The analysis merges multiple data sets to come up with a concise answer on if the upgrade was worth it

| Dataset                        | Source                                                    | Purpose                                                                                    |
| :----------------------------- | :-------------------------------------------------------- | :----------------------------------------------------------------------------------------- |
| **Client Profile**             | GitHub: 'Df_final_demo'                                   | Demographics like age, gender, and account details of our clients                           |
| **Digital Footprints**         | GitHub: 'Df_Final_Web_Data'                               | A detailed trace of client interactions online, divided into two parts: pt_1 and pt_2.     |
| **Experiment Roster**          | GitHub: 'Df_final_experiment_clients'                     | A list revealing which clients were part of the grand experiment                            

## Day 1: Exploration and Hypothesis Formulation

The initial day focused on exploratory data analysis and defining the analytical framework.

### Analysis Goals

1. **Goal A:** Evaluate whether the new design increases completion rates.
2. **Goal B:** Assess changes in client efficiency and engagement.
3. **Goal C:** Identify which client benefit most from the redesign.

### Testable Hypotheses

| ID     | Category                  | Hypothesis Statement                                                                                                                |
| :----- | :------------------------ | :---------------------------------------------------------------------------------------------------------------------------------- |
| **H1** | Reduce time to Complete   | Clients using the new design complete the process faster than clients using the original design.                                    |
| **H2** | Less error/drop off       | Clients in the test group are less likely to abandon the process during the initial steps compared to the control group.            |


---

## Day 2: Data Cleaning and Preprocessing

Day 2 focused on preparing the raw Vanguard datasets for analysis and ensuring consistency across demographic and web interaction data.

### Key Cleaning Steps (Python/Pandas)

1. **Column Name Standardization**: Renamed columns for consistency (lowercase, underscores) across demographic and web datasets.
2. **Data Type Validation**: Ensured correct data types for age, tenure, timestamps, and categorical variables.
3. **Handling Missing Values**: Identified and assessed missing values in demographic attributes and web events.
4. **Initial EDA**: Conducted preliminary analysis to examine distributions, completion rates, session counts, and potential anomalies.
 
 

---

## Day 3: Hypothesis Testing – Completion & Balance Checks

Day 3 focused on validating whether the new design led to a meaningful and reliable improvement in completion rates.



### 1. `Completion Rate – Statistical Significance`
- `Hypothesis` → The new design increases completion rates compared to the old design.
- `Method` → Chi-square test (appropriate for binary completion outcomes).
- `Result` → Statistically significant difference Chi-square Statistic: 139.93, P-value: 0.00000.
- `Conclusion` → The new design significantly improves completion rates.
  
---

### 2. `Practical Impact – Cost-Effectiveness Threshold`
- `Threshold` → Minimum required improvement set at 5%.
- `Observed Uplift` → ~8.7%.
- `Conclusion` → The improvement exceeds the practical threshold, indicating a meaningful effect size.

---

### 3. `Group Balance Check – Client Tenure`
- `Test group tenure` → 11.98 years
- `Control group tenure` → 12.09 years
- `Finding` → Slight statistical difference but negligible in practice.
- `Coclusion` → Groups are sufficiently balanced; results are not biased by tenure.


---

### 🔗 Key Takeaway

- The new design delivers a statistically significant and practically meaningful increase in completion rates, with no material group imbalance.



---

## Day 4: Design Effectiveness & Experiment Validation

Day 4 focused on confirming that the experiment results were reliable and not driven by demographic bias or poor experimental design.

### Demographic Balance Checks

- **Gender:** No significant difference in engagement between genders (p = 0.305). The new design performs equally well for men and women.
- **Age:** Average age was nearly identical between groups (47.5 vs 47.2 years). While statistically significant due to large sample size, the difference is practically negligible.

### Experiment Quality Assessment

- **Randomisiation:** Test and Control groups were largely balanced, with only minor demographic differences that do not affect conclusions.
- **Assesment:** Long enough to capture typical user behavior and reduce short-term or novelty effects.


### 🔗 Key Takeaway

- The experiment was well-designed, sufficiently long, and free from meaningful demographic bias, supporting confidence in the results.


---
## Day 5: Bonus Analysis – Client Behavior & Efficiency

Day 5 focused on deeper behavioral insights and validating the robustness of our findings beyond completion rates.

- **User behavior remains consistent:** Clients follow similar paths in both designs, with no increase in steps or complexity.
- **Efficiency unchanged:** Time spent is statistically different but practically negligible (+5.5s), meaning both designs are equally efficient.
- **Robust results:** Effect size and power analysis confirm the sample size was sufficient and the findings are reliable.

- ### 🔗 Key Takeaway

- Bonus analysis confirm that the new design improves completion, reinforcing confidence in the rollout decision.

---

## Day 6 and 7: 
