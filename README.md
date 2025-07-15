# 💊 GLP-1 Adherence & Cost Impact Modeling

This project models the impact of adherence to weight-loss GLP-1 medications—**Wegovy, Saxenda, and Zepbound**—on healthcare costs using mock claims data. The goal is to evaluate how consistent usage of these drugs affects **medical and pharmacy spending** over a multi-year period.

> ⚠️ **Note**: This study was originally performed using internal company data. The version presented here uses **mock data** for educational and portfolio purposes only. Results and observations in the notebooks will not match the real-world study.

---

## 🎯 Objectives

1. Assess whether members on GLP-1 medications experience reduced medical costs over time.
2. Compare cost trends between adherent users, low-adherence users, and matched non-users.
3. Model differences in outcomes using claims, demographic data, and pharmacy adherence rates.

---

## 🗂️ Study Parameters

- **Dataset Size**:
  - 261 members with ≥65% PDC (adherent users)
  - 171 members with ≤20% PDC (low-adherence)
  - 1,000,000+ members in full book of business (mocked)
- **Study Period**: Calendar years 2021 to 2024
- **Baseline Year**: 2021 (pre-GLP-1 usage)
- **Eligibility**:
  - Continuous enrollment since January 2021
  - Overweight or obesity diagnosis
  - PDC (Percentage of Days Covered) calculated across two years

- **Matching Method**: Propensity Score Matching (PSM) on:
  - Age  
  - Gender  
  - Plan relationship (subscriber/spouse/dependent)  
  - Diagnosis (overweight/obese)

---

## 🛠️ Tools & Stack

- `SQL` – data extraction from mock claims tables
- `Python` – data processing, modeling, and statistical matching
- `Jupyter Notebooks` – exploratory analysis and methodology
- `Power BI` – interactive reporting and data visualization

---

## 📊 Key Findings

### 📈 High-Adherence GLP-1 Users (≥65% PDC)

- 88% female, mostly Gen X; 87% plan subscribers
- **Medical costs** dropped **41%** from \$13,143 in 2021 → \$7,740 in 2024
- **Pharmacy costs** increased **411%** to \$17,276 annually
- Inpatient costs dropped from \$202 → \$36 PMPM
- Chronic condition PMPM dropped from \$1,091 → \$645

### ⚠️ Low-Adherence GLP-1 Users (≤20% PDC)

- 83% female, 70% plan subscribers
- **Medical costs increased** by **16%** from \$9,831 in 2021 → \$11,233 in 2024
- Many discontinued after year one
- GLP-1 PMPM fell to \$100 as majority dropped treatment

---

## 📁 Project Structure

| File | Description |
|------|-------------|
| `BOB_GLPWLA_Analysis_PDC_Longevity.ipynb` | PDC and cost analysis for ≥65% adherence |
| `BOB_GLPWLA_Analysis_PDC_Longevity-20.ipynb` | PDC and cost analysis for ≤20% adherence |
| `Combined_Cohort_PDC-NOFILTER.ipynb` | Propensity Score Matching logic for comparison |
| `NO_WEGOVY_MEMBERS.ipynb` | Logic to exclude weight-loss GLP-1 users from control group |

---

## 🔎 Insights

- Medication adherence appears to be a key driver in reducing long-term medical costs, despite rising drug spend.
- Poor adherence shows cost trends comparable to non-users—suggesting **inconsistent use may dilute benefit**.
- Findings support the use of **adherence-based stratification** in ROI modeling and plan design.

---

## 🚀 Future Work

- Add modeling via `Streamlit` for adjustable cost scenarios (by drug, adherence, and plan size)
- Simulate cost trajectories with real-world pricing assumptions
- Create a web-based dashboard for employer benefit strategy teams

---

## 📬 Contact

For questions or collaboration inquiries, reach out to [Your Name] at [your-email@example.com] or visit [your-portfolio-site.com].