# Colorectal-Cancer-Screening-SDOH-Analysis

🔎 ##**About This Project**

This project analyzes the 2022 Behavioral Risk Factor Surveillance System (BRFSS) dataset to estimate colorectal cancer (CRC) screening prevalence among U.S. adults aged 45–75. The analysis aims to highlight disparities in screening across income, education, race/ethnicity, insurance status, and geography, and evaluate how states perform relative to the Healthy People 2030 CRC screening target (68.3%).

This is a fully reproducible public health data analysis pipeline built in R and Quarto, using survey-weighted methods and publication-quality visualizations and tables.

🎯##**Objectives**
@Estimate national and state-level CRC screening prevalence.
@Stratify results by race, sex, income, education, insurance status, and metro status.
@Visualize disparities using bar charts and summary tables.
@Identify states that fall below the national screening benchmark.

🧪 ##**Methodology**

- **Dataset**: [2022 BRFSS (LLCP2022.XPT)](https://www.cdc.gov/brfss/annual_data/annual_2022.html).
- **Population**: Adults aged 45–75 (USPSTF recommendation)
- **Software**: R (Quarto), survey, gtsummary, ggplot2
- **Survey Design**: Complex survey weighting (svydesign)
- **Statistical Estimates**: Proportions with 95% CI using xlogit method
- **Key Outcome Variable**: X_CRCREC2 (CRC screening status)

📊 ##**Key Findings**

**Lower CRC screening rates were observed among:**

@Ages 45–54, those without insurance, low-income groups, males
@Racial/ethnic minorities including Hispanic, Asian, AI/AN, NH/OPI
@Those without a personal healthcare provider
@32 states failed to meet the Healthy People 2030 CRC screening target of 68.3%

Bar charts and tables visually display these disparities, supporting action-oriented public health messaging.

📁 ##**Repository Structure**
📦 brfss-2022-crc-screening/
├── README.md                 # Project description and instructions
├── brfss_crc_screening.qmd   # Cleaned Quarto analysis script
├── data/ [LLCP2022.XPT](https://www.cdc.gov/brfss/annual_data/annual_2022.html) # (Local only - not included in repo due to size) 
├── output/ plots             # Visualizations of disparities

📦 ## **Required R Packages**
pacman::p_load("tidyverse", "janitor", "survey", "gtsummary", "ggplot2", 
               "reshape2", "writexl", "flextable", "foreign", "knitr")
