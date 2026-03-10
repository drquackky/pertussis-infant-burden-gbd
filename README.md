# Pertussis Burden in Infants Under 1 Year Using Data from Global Burden of Disease 2023

## Project Overview

Pertussis (whooping cough) remains an important public health problem, especially in **infants under 1 year of age**, 
who are at the highest risk of severe illness, hospitalization, and death. Although vaccination has greatly reduced the global burden, 
pertussis continues to persist in many countries and remains unequally distributed across development levels.

In this study, I used data from the **Global Burden of Disease (GBD)**, a large international research program coordinated by **the Institute for Health Metrics and Evaluation (IHME)** 
that provides standardized estimates of disease, injury, and health loss across countries, age groups, and time periods. 
I chose GBD because it offers comparable measures such as incidence, mortality, and disability-adjusted life years (DALYs), which helped me examine how serious pertussis burden is, 
compare patterns between populations, and assess changes over time even when local health data may be limited or incomplete.


GBD data reference:  
https://vizhub.healthdata.org/gbd-results/

---

## Key Concepts

### Pertussis Burden Measures

This analysis examines three indicators of pertussis burden in infants under 1 year:

- *Incidence rate* - the number of new pertussis cases per 100,000 population
- *Mortality rate* - the number of deaths caused by pertussis per 100,000 population
- *DALY rate* - the total health loss per 100,000 population, combining fatal and non-fatal burden

DALYs are included because they capture *both premature death and health loss due to illness* in a single measure. They combine *years of life lost (YLLs)* and *years lived with disability (YLDs)*, 
providing a broader picture of disease burden than incidence or mortality alone.  

### Socio-Demographic Index (SDI)

The *Socio-Demographic Index (SDI)* is a composite indicator used in the GBD study to measure a country’s level of development. SDI is based on three components: income per capita, educational attainment, and fertility rate in individuals younger than 25 years.

Countries are classified into five SDI groups, which allows comparison of pertussis burden across different development settings:

1. *Low SDI* - ex. Niger and Chad  
2. *Low-middle SDI* - ex. Laos and India  
3. *Middle SDI* - ex. Brazil and Egypt  
4. *High-middle SDI* - ex. China and Hungary  
5. *High SDI* - ex. United States of America and Germany  

Socio-demographic index reference:  
https://ghdx.healthdata.org/record/gbd-2023-socio-demographic-index-sdi

---

## Research Questions and Statistical Analysis

This analysis focuses on the following questions:

### 1. How does pertussis burden vary across countries and development levels?
- How do incidence, mortality, and DALY rates differ between countries?
- How does pertussis burden vary across SDI groups?

**Statistical analysis:**  
Differences in pertussis burden rates were analyzed using the non-parametric test **Kruskal–Wallis test** because the data is not normally distributed.  
When significant differences were identified, **Dunn’s post hoc test** was applied for pairwise comparisons, with **FDR adjustment** used to account for multiple testing.

### 2. Is pertussis burden associated with socio-demographic development?
- Is there a positive or negative relationship between SDI and pertussis incidence, mortality, or DALY rates?

**Statistical analysis:**  
The relationship between **SDI** and pertussis burden indicators was examined using **linear regression analysis**.

### 3. How has pertussis burden changed over time?
- Have incidence, mortality, and DALY rates increased or decreased from 1990 to 2023?
- Are there significant turning points in the trends?

**Statistical analysis:**  
Temporal patterns in incidence, mortality, and DALY rates were first explored through **descriptive trend analysis**.  
**Joinpoint regression** was then used to identify statistically significant changes in trend over time.

### 4. Did the COVID-19 period coincide with changes in pertussis trends?
- Were there noticeable disruptions or shifts during the pandemic and post-pandemic years?

**Statistical analysis:**  
Potential changes during the COVID-19 and post-pandemic period were interpreted from the **descriptive trend results** and **joinpoint regression outputs**.


---

## Tools

This project was developed using:

- **R programming language**, using packages from the **tidyverse** such as **dplyr** for data manipulation and **ggplot2** for data visualization  
- **ggstatplot** for enhanced boxplot visualization  
- **Joinpoint Regression Program** developed by the **National Cancer Institute**

**Full report and interpretation can be accessed**:  
...
