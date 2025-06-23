# GLP-1 Study
**Objective**

Determine whether members taking weight-loss GLP-1 agonists (Wegovy, Saxenda, or Zepbound) decrease their medical costs. The first hypothesis is that members taking GLP-1s have reduced medical expenses over time. The second hypothesis is that members who are similar in medical characteristics but who have not taken GLP-1s are more costly on the plan.
A second study was done looking at members who took a GLP-1 who took the prescription for 20% of the time over two years. The hypothesis is that those members will not see their medical costs drop as much as the more consistent GLP-1 takers.

**Parameters**

261 members were analyzed in MMA’s book of business. There are over a million members in the PATH database. These members initiated weight-loss agents in 2022 and were required to have a Percentage of Days Covered (PDC) for 65% of the time they were on the GLP-1s for at least two years. Since this is a smaller dataset, the PDC was dropped down from the standard 80% to capture a wider net of study. They also needed to be continuously enrolled on plans since January 2021. All claims reviewed with paid in calendar years 2021 through 2024. 2021 is the baseline year where no members were prescribed GLP-1 drugs.
The matched pair cohort used propensity score to match members with similar characteristics to the original cohort. They needed to be continuously enrolled since 2021. These members were matched to the original cohort using covariates based on age, gender, member relationship, and including an overweight or obese diagnosis in the study timeline. The matched pair cohort had members with rheumatoid arthritis agents removed from the dataset because the specialty costs of those drugs were skewing the pharmacy costs – an issue where the treatment study did not have those high cost drugs.
For the second study, the PDC was dropped to 20% over two years. 171 members were located in this cohort.

Medical and pharmacy claims were reviewed adjusted for inflation. Source and computation are at the end of the document.

**Observations**

GLP-1 Cohort >= 65%
Most of the members are Generation X, with 88% of the cohort being female. 87% of the population were the subscribers on the plan. 

In 2021, normalized medical PMPM was $1,091 and pharmacy PMPM was $267. In 2024, medical PMPM was $645 and pharmacy PMPM was $1,633. Pharmacy costs increased 511% and medical costs dropped 41%. Average medical member costs for 2021 was $13,143 per year. They dropped to $7,740 in 2024. Average pharmacy cost per member in 2021 was $3,406. This increased to $17,276 in 2024.

Most notably, inpatient PMPMs dropped for $202 in 2021 to $36 in 2024. Outpatient surgeries dropped $244 in 2021 to $147 in 2024. ER visits and PMPMs stayed relatively consistent from $49 to $41. Chronic conditions costs $1,091 in 2021 and dropped to $645. 

Weight-loss GLP-1 cost $727 PMPM and increased to $1,067 in 2024. Only 251 of the 261 members continued to take the GLP drugs into 2024.

Osteoarthritis costs dropped from $96 PMPM to $31 PMPM. Spondylopathies dropped $63 to $16. Persons encountering for health exams increased $49 to $65. Sleep disorders dropped $41 to $4.

GLP-1 Cohort =< 20%
171 members were in this cohort. Most of the members are Generation X, with 83% of the cohort being female. 70% of the population were the subscribers on the plan. 

In 2021, normalized medical PMPM was $795 and pharmacy PMPM was $160. In 2024, medical PMPM was $920 and pharmacy PMPM was $469. Pharmacy costs increased 193% and medical costs increased 16%. Average medical member costs for 2021 was $9,831 per year. They increased to $11,233  in 2024. Average pharmacy cost per member in 2021 was $2,164. This increased to $5,862 in 2024.

OP surgeries and inpatient admits costs about the same PMPM from 2021-2024, with a drop in the middle. ER visits and chronic condition costs stayed around the same or increase steadily. 

Weight-loss GLP-1 cost $122 PMPM and dropped to $100 in 2024. Only 39 of the 171 members continued to take the GLP drugs into 2024. 41 stayed on in 2023, so the majority of those stopped taking it after the first year. However, a lot of these members had taken Mounjaro and Ozempic as well. Those hovered at $129 in 2024.


Tools used to perform this analysis were SQL, Python, Jupyter Notebooks and Power BI.

BOB_GLPWLA_Analysis_PDC_Longevity: Notebook that runs initial query and determines PDC for 65%
BOB_GLPWLA_Analysis_PDC_Longevity-20:Notebook that runs initial query and determines PDC for 20%
Combined_Cohort_PDC-NOFILTER: Runs PSM cohort matching for PDC 65 and no GLP-1 takers
NO_WEGOVY_MEMBERS: Runs initial query to exclude members with weight-loss drugs


