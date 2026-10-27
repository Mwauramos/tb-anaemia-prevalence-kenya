# TB and Anaemia Prevalence — Kenya Cross-Sectional Study

A population-based epidemiology project estimating the prevalence of pulmonary
tuberculosis and anaemia in Kenyan adults, identifying determinants through
multivariable logistic regression, and mapping county-level variation.

## Study Design

| Feature | Description |
|---|---|
| Design | Cross-sectional survey (KDHS-style) |
| Population | Adults aged 15 to 64 years |
| Sampling | Multi-stage stratified cluster sampling, 47 counties |
| N | 5 400 respondents |
| Outcome 1 | Bacteriologically confirmed pulmonary TB |
| Outcome 2 | Anaemia (Hb < 12.0 g/dL women, < 13.0 g/dL men) |
| Data sources | KDHS 2022, Kenya National TB Prevalence Survey 2016, NASCOP 2022 |

## Research Questions

1. What is the prevalence of TB and anaemia in Kenyan adults, overall and by subgroup?
2. What are the independent determinants of TB and anaemia after adjusting for confounders?
3. Is there a significant co-occurrence of TB and anaemia in the same individuals?
4. How does county-level prevalence vary across Kenya's 47 counties?

## Key Findings

| Outcome | Finding |
|---|---|
| TB prevalence | Approximately 0.55% (calibrated to Kenya 2016 national survey: 558/100 000) |
| Anaemia prevalence | Approximately 15% overall (women higher than men) |
| Strongest TB determinant | HIV positive: Adj OR approximately 8.2 (p < 0.01) |
| Second TB determinant | Previous TB treatment: Adj OR approximately 3.5 |
| Strongest anaemia determinant | Malnutrition (BMI < 18.5): Adj OR approximately 2.4 |
| TB-Anaemia co-occurrence | Significant positive association (OR > 1.0, p < 0.05) |
| HIV stratification | Both TB and anaemia prevalence dramatically higher in HIV-positive adults |

## Analytical Pipeline

1. Synthetic cross-sectional data generation (KDHS multi-stage cluster design)
2. Overall and subgroup prevalence estimates with 95% CI
3. Prevalence bar charts by sex, age, residence, and SES
4. Multivariable logistic regression for TB determinants (bootstrap 95% CI)
5. Multivariable logistic regression for anaemia determinants
6. Dual forest plot: TB and anaemia adjusted ORs side by side
7. County-level ranked prevalence charts for both outcomes
8. TB-Anaemia co-occurrence analysis (2x2 table, OR, stacked bar)
9. HIV-stratified prevalence comparison
10. Epidemiological interpretation with Kenya NTLP and NCD policy context

## Quick Start (Google Colab)

Open `TB_Anaemia_Prevalence_Kenya.ipynb` in Google Colab. All required libraries
(numpy, pandas, scipy, scikit-learn, matplotlib) are pre-installed.

## Tech Stack

`Python 3.10+` · `numpy` · `pandas` · `scipy` · `scikit-learn` · `matplotlib`

## Epidemiological Background

Kenya is one of the 30 high TB burden countries identified by WHO, with an
estimated 133 000 incident TB cases in 2022 (WHO Global TB Report 2023).
The country is also a high TB-HIV co-endemic setting, with approximately
26% of TB patients being HIV co-infected. The Kenya National TB and Leprosy
Programme (NTLP) under MOH targets bacteriological confirmation using
GeneXpert and sputum smear microscopy.

Anaemia affects approximately 19% of Kenyan women of reproductive age
(KDHS 2022), driven primarily by iron deficiency, malaria in endemic zones,
and HIV. The dual burden of TB and anaemia — linked through shared risk
factors (HIV, malnutrition, poverty) and direct biological mechanisms
(anaemia of chronic disease in active TB) — makes integrated screening
and treatment an important public health priority.

## Data Sources

Synthetic data calibrated to:
- Kenya National TB Prevalence Survey 2016 (MOH/NTLP): prevalence by sex, age, HIV
- Kenya Demographic and Health Survey (KDHS) 2022: anaemia, HIV, SES distributions
- NASCOP ART Annual Report 2022: HIV prevalence by county
- WHO Global TB Report 2023: Kenya TB epidemiology

---

*ZENIK.AI · github.com/Mwauramos*
