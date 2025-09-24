# SOC-Gain-Potential-Classification-RegenAg

This repository provides data, code, and the trained machine learning model supporting the publication:

**Anand, S.K., Singh, R., Mohanty, B., Rajan, N., & Calabrese, S. (2025). Classifying the potential for soil organic carbon gain under regenerative agriculture. *Environmental Research Letters*, 20(4), 044045.**  
[https://doi.org/10.1088/1748-9326/adc292](https://doi.org/10.1088/1748-9326/adc292)

---

## Repository contents

- **`Supporting_Dataset.xlsx`**  
  Contains globally distributed paired-plot data from peer-reviewed field experiments comparing soil organic carbon (SOC) under conventional tillage (CT) and no-tillage with residue retention (NT). These entries provide the basis for model training and exploratory data analysis.

- **`RF_BORDERLINE_SMOTE.joblib`**  
  The trained random forest classifier (RFC) developed using imbalanced machine learning with Borderline-SMOTE to address the class imbalance between SOC gain and SOC loss. The model identifies thresholds for antecedent SOC, Dryness Index (DI), and Net Primary Productivity (NPP) that determine SOC gain potential under no-tillage transition.

- **`SOC_Classification.ipynb`**  
  Jupyter Notebook that:  
  - Bins and groups dataset entries based on the sign of SOC change (∆SOC) and antecedent SOC under conventional tillage (SOC_CT).  
  - Applies the trained RFC model to reproduce the hierarchical classification framework.  
  - Demonstrates exploratory data analysis and visualizations corresponding to **Figures 1, 2, and 3** in the published manuscript.
 
- **`NMI_Calculation.ipynb`**  
  Jupyter Notebook for calculating **Normalized Mutual Information (NMI)** among the governing features of the random forest classifier for SOC change following the no-tillage transition:  
  - (a) DI and SOC_CT  
  - (b) NPP and SOC_CT  
---

## Study overview

The analysis quantifies the conditions under which transitioning from conventional tillage to no-tillage leads to SOC gains or losses. Key findings include:

- Antecedent SOC stock (SOC_CT) is the dominant factor, with a threshold at **50 t ha⁻¹** beyond which SOC gains are less likely.  
- Climatic aridity, expressed via the **Dryness Index (DI)**, and **Net Primary Productivity (NPP)** further determine SOC gain potential.  
- Hierarchical classification identifies high- and low-potential cropland zones for SOC sequestration under regenerative agriculture practices.
