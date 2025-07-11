📊 Evaluating Oregon’s Measure 110: A Difference-in-Differences Policy Analysis

This repository contains the code and analytical documentation for a policy evaluation of Oregon’s Measure 110, which decriminalized possession of small amounts of drugs starting in 2021. Using a matched-pair Difference-in-Differences (DiD) approach, the study compares Lane County, OR (Eugene) to Ada County, ID (Boise) to assess whether decriminalization impacted overdose mortality rates when compared to "business as usual" zero-tolerence law enforement approaches.

⸻

🔍 Project Overview
	•	Policy Focus: Oregon’s Measure 110 — drug decriminalization + social support investment
	•	Research Question: Which drug policy is more effective at reducing overdose deaths? 
	•	Method: Matched-pairs, DiD using annual data (2018–2023) with fixed effects for year and a placebo outcome test
	•	Treatment Group: Lane County, OR
	•	Control Group: Ada County, ID
	•	Primary Outcome: Overdose deaths per 100,000
	•	Placebo Test: Motor vehicle death rates (to check for spurious associations)[in progress]
 
 📦 R Packages Used
	•	tidyverse
	•	fixest
	•	broom
 	•	here
	•	lmtest
	•	modelsummary
 
📈 Methodology Summary
	•	Model 1: OLS DiD
	•	No fixed effects
	•	Includes treatment, time, and interaction term
	•	Model 2: Fixed Effects DiD
	•	Adds year fixed effects (| Year)
	•	Uses clustered standard errors (clustered by year)
	•	Placebo Test: Repeats DiD design using motor vehicle death rates to ensure observed treatment effect is not due to general mortality trends [in progress]

 📌 Key Findings
	•	Overdose deaths increased significantly in Lane County following Measure 110, relative to Ada County (not adjusting for extraneous factors)
	•	The DiD estimate (β = 24.07, p < 0.01) remained robust with fixed effects (not adjusting for extraneous factors)
	•	Placebo analysis with motor vehicle deaths showed no significant effect, strengthening causal interpretation [in progress]
	•	The policy’s outcome likely reflects challenges in implementation lag, treatment access, and system capacity, not the failure of harm reduction principles [in progress]

⸻

⚠️ Limitations
	•	Small sample (2 counties × 6 years)
	•	Assumes parallel trends (visually inspected, both exhibited positive trends pre policy implementation)
	•	Observational data—subject to unobserved confounders [**in progress to add extensive/comprehensive covariates]
	•	Data from CDC WONDER is aggregated; individual-level (city/town) analysis not possible 
 

📬 Contact
Author and researcher Brittany Spinner, M.Ed., M.S., Ph.D. Candidate
For questions or collaboration inquiries, contact:
📧 [spinner.prevsci@gmail.com]
🔗 [https://www.linkedin.com/in/b-spinner-datasci/]
written article available upon request
