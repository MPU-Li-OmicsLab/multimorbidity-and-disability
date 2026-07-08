# Global Epidemiology and Multi-Ancestry Cross-Trait GWAS Uncover Shared Synaptic Genetics Linking Physical-Psychological Multimorbidity to Functional Decline in Aging

This repository contains the main epidemiological analysis code used in the manuscript on multimorbidity and functional disability in aging populations.

## Project summary
This study integrates large-scale epidemiological evidence from five harmonized aging cohorts across 21 countries, together with multi-ancestry genetic and molecular evidence, to identify which chronic disease combinations are most strongly linked to functional disability, how these patterns vary across populations, and what biological mechanisms may underlie these associations. The epidemiological analyses draw on data from the China Health and Retirement Longitudinal Study (CHARLS), the English Longitudinal Study of Ageing (ELSA), the Health and Retirement Study (HRS), the Mexican Health and Aging Study (MHAS), and the Survey of Health, Ageing and Retirement in Europe (SHARE).

The findings show that physical-psychological multimorbidity is a major global driver of incident functional disability, associated with higher disability risk, greater population-level burden, and shorter disability-free life expectancy. Clear cross-national heterogeneity is also observed: physical-cognitive multimorbidity is more prominent in China, whereas physical-psychological multimorbidity is more prominent in Western cohorts.

Beyond the epidemiological findings, the study incorporates disease-level Mendelian randomization, multi-ancestry cross-trait GWAS, MiXeR, and conjFDR analyses, which together suggest partially shared causal and genetic architecture linking depression, hypertension, diabetes, and functional disability. Follow-up gene-level analyses further highlight shared pleiotropic genes, particularly NEGR1, and implicate synaptic function, neuronal connectivity, and neuroplasticity as key biological pathways. Additional support from temporal brain transcriptomic profiles, eQTL-based MR, colocalization analyses, and knockout models strengthens the interpretation that multimorbidity and functional decline may partly arise from a common biological substrate.

## Main scripts
- `01meta-analysis-cross-sectional.R`: cross-sectional logistic regression and pooled meta-analysis of odds ratios across CHARLS, ELSA, HRS, MHAS, and SHARE.
- `02mata-analysis-cohorts.R`: longitudinal cohort analysis for incident disability, including harmonized risk-difference estimation and meta-analysis.
- `03meta-regression.R`: meta-regression analyses for between-cohort heterogeneity.
- `04PAF-analysis.R`: estimation of adjusted population attributable fractions for chronic disease and multimorbidity patterns.
- `05network-analysis.R`: network analysis of disease co-occurrence and links with disability.
- `06mediation-analysis-BA.R`: mediation-related analyses.
- `function/`: helper functions for extracting odds ratios, risk differences, and tidying model outputs.

## Data access
Individual-level cohort data are not redistributed in this repository because access is governed by the data use policies of the original studies. Researchers who wish to reproduce or extend the analyses should request or download the data directly from the corresponding cohort platforms, subject to each study's application and approval procedures.

The analyses are based on the following aging cohort resources:
- `CHARLS` (China Health and Retirement Longitudinal Study): a nationally representative longitudinal study of middle-aged and older adults in China. Data access information is available at the official CHARLS website.
- `ELSA` (English Longitudinal Study of Ageing): a longitudinal panel study of aging in England. Data are available through the UK Data Service.
- `HRS` (Health and Retirement Study): a nationally representative longitudinal study of older adults in the United States. Data access information is available through the HRS website.
- `MHAS` (Mexican Health and Aging Study): a longitudinal study of aging in Mexico. Data access information is available through the MHAS website.
- `SHARE` (Survey of Health, Ageing and Retirement in Europe): a cross-national panel database covering multiple European countries. Data access information is available through the SHARE Research Data Center.

After obtaining approval, users should place the harmonized cohort-level `.RData` files in a local `data/` directory before running the scripts.

## Notes
- The code is organized around the epidemiological figures and summary results used in the main manuscript revision.
- Variable names and disease-domain definitions follow the harmonized analytic datasets prepared for the study.
