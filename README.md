# Health Indicators and Outcomes Analysis in Sub-Saharan Africa: A Data-Driven Approach Using Open Source APIs
## Introduction
Health outcomes in Sub-Saharan Africa remain a critical area of concern due to persistent disparities in access, quality, and financing of healthcare services.
Despite global efforts to improve health systems, the region still faces high maternal and child mortality, low life expectancy, and limited healthcare infrastructure.
Analyzing key health indicators — such as life expectancy, health expenditure, immunization coverage, and mortality rates — provides vital insights into progress and challenges.
This project leverages open data from the World Health Organization (WHO) and the World Bank (WB) APIs to integrate, clean, and analyze health indicators across Sub-Saharan Africa using Python, Google BigQuery, and Tableau.
## Concept clarification
### Health indicator
A health indicator is a measurable variable used to describe and monitor specific aspects of a population’s health status or determinants of health.
Examples:
1. Health Expenditure (per capita / % GDP):Represents the input or determinant — how much a country invests in health systems. It influences outcomes but is not itself a result.
2. Measles Immunization Rate:Measures health service coverage (preventive measure), showing access and performance of immunization programs.
3. Birth rate:Represents a demographic measure — number of births per 1,000 population. It affects planning but not a direct health outcome.
4. Population Growth rate:Represents a demographic measure — number of births per 1,000 population. It affects planning but not a direct health outcome.
5. Births attended by skilled  staff:Reflects health service delivery and access to skilled maternal care — an indicator of healthcare quality.
6. Antenatal Care  Coverage:Represents health service utilization (the proportion of pregnant women receiving prenatal care) — an input for improved maternal outcomes.
### Health Outcome
Reflects the actual results of health interventions or the state of health of a population — the end results of healthcare policies, services, or behaviors.
Examples:
1. Life expectancy:Reflects the end result of population health and overall healthcare effectiveness — a summary measure of longevity and wellbeing.
2. Maternal mortality:Measures deaths due to pregnancy-related causes — a result of healthcare access, quality, and maternal care outcomes.
3. Under 5 mortality:Indicates child survival and reflects the outcome of child health interventions, nutrition, and access to healthcare.
4. HIV Prevalednce:Reflects the actual health status of the population — the percentage of people living with HIV.

## Classification of the indicators
### Health outcomes
1. Life expectancy
2. Under 5 mortality
3. Maternal mortality
4. HIV prevalence
### Health System Indicators
1. Health expenditure per capita
2. Measles immunization rate
3. Antenatal Care Coverage
4. Births attended by skilled staff
### Demographic indicators
1. Population Growth Rate
2. Total population
3. Birth rate
### Socioeconomic indicators
1. GDP per capita
2. Urban population percentage
3. Adult literacy rate
### Disease Burden
1. HIV prevalence
2. TB prevalence
3. Malaria prevalence

## Problem Statement
Despite improvements in healthcare access and outcomes across Sub-Saharan Africa, data gaps and limited integration of health statistics hinder evidence-based decision-making.
Policymakers and researchers often struggle to integrate data from multiple sources to uncover relationships between factors like health expenditure, immunization coverage, and child mortality.
This project addresses the problem by developing a data-driven framework that integrates health data from multiple open APIs, cleans and analyzes the datasets, and visualizes patterns to provide actionable insights on health progress and disparities across the region.

## Area of study
## One continent,two realities 
<img width="950" height="937" alt="image" src="https://github.com/user-attachments/assets/2b50dfbb-586f-4531-80dc-82a97dda1ee3" /> 

Africa is the most diverse continent, and aggregated data obscures massive regional disparities, particularly in health outcomes. 
This project focuses exclusively on Sub-Saharan Africa (SSA) because it faces a disproportionate global burden of disease, requires distinct policy interventions, and shares a unique set of socioeconomic and epidemiological realities that are fundamentally different from those in North Africa. Using continental-level averages would mask the profound health inequalities that exist.
## The Stark Disparity in Health Outcomes
<img width="852" height="550" alt="image" src="https://github.com/user-attachments/assets/8dad1839-6561-4bda-baea-3ccb15f48f82" />

## Why Sub-Saharan Africa Deserves Focused Analysis
Africa is home to 1.4 billion people spread across 54 countries, but the continent is far from uniform.
There are stark differences in economic development, healthcare systems, and disease burden between the Northern, Southern, Eastern, and Western regions.
While North Africa has relatively advanced healthcare infrastructure, higher GDP, and lower disease burden, Sub-Saharan Africa (SSA) continues to face disproportionate health challenges.
Sub-Saharan Africa accounts for over 65% of global maternal deaths, more than 50% of HIV infections, and the world’s highest under-5 mortality rate.
These contrasts make it vital to study SSA as a distinct region rather than blending it into a continental average that hides inequalities.
## Analytical Justification — Why SSA Needs Its Own Focus
1. Health Inequalities:Averaging health data for all of Africa conceals regional disparities. For example, North Africa’s life expectancy exceeds 70 years, while several SSA nations are below 60.
2. Policy relevance:Most international health programs (WHO, UNICEF, Global Fund) treat SSA as a unique operational region because it faces similar socioeconomic and epidemiological realities.
3. Development gaps:SSA countries share lower income levels, weaker healthcare systems, and higher dependency on external aid — making comparative analysis across SSA more meaningful.
4. Data Consistency:Many global health datasets (e.g., World Bank’s “region=SSF”) are structured specifically for SSA, allowing cleaner, more consistent API retrieval and analysis.
5. Research Impact:By isolating SSA, we can develop targeted insights and recommendations that directly address the needs of the region — instead of generalizing across an entire continent.

## Objectives
### Main Objective
To explore and analyze key health indicators and outcomes across Sub-Saharan Africa using open-source APIs and data visualization tools.

### Specific Objectives
1. To collect and integrate health-related datasets from multiple open APIs such as the World Bank and World Health Organization (WHO).
2. To clean, transform, and merge these datasets into a unified analytical format suitable for exploration.
3. To analyze regional trends in core health indicators like life expectancy, child mortality, maternal mortality, and health expenditure.
4. To visualize health trends and disparities across countries using interactive dashboards in Tableau.
5. To generate insights that can inform public health planning, policy decisions, and progress tracking toward SDG 3 (Good Health and Well-being).

## Research Questions
### Overall Health Progress (Trend & Ranking)
1. How have key health outcomes (life expectancy, under-5 mortality, maternal mortality) changed in Sub-Saharan Africa from 1980–2023?
2. Which countries have achieved the greatest improvements in life expectancy and mortality reduction over time?
3. Are health improvements evenly distributed across regions (East, West, Central, Southern Africa)?
### Health Investment vs. Outcomes
1. Does higher health expenditure per capita correlate with better health outcomes (life expectancy, maternal mortality)?
2. Are countries investing more in health seeing faster improvements in outcomes over time?
3. Is there a spending efficiency gap — countries spending the same amount but achieving different results?
### Maternal and Child Health
1. What is the relationship between births attended by skilled staff and maternal mortality rates?
2. Do countries with higher antenatal care coverage have lower under-5 mortality?
3. How has immunization (e.g., measles coverage) impacted child survival rates across SSA?
### Disease Burden (HIV Focus)
1. How has HIV prevalence evolved across SSA countries since 1990?
2. What is the relationship between HIV prevalence and life expectancy?
3. Which countries have successfully reduced HIV prevalence the most?
### Socioeconomic Context
1. How does GDP per capita relate to health expenditure and life expectancy?
2. Do more urbanized countries show better health outcomes?
3. How does literacy rate correlate with maternal and child mortality?

## Stakeholders and  Beneficiaries
1. Public Health Policymakers and Government Agencies:Identify gaps and target interventions efficiently.
2. International Health Organizations (WHO, UN,WB):Track SDG 3 progress and assess program impact.
3. Researchers and Data Analysts:Use for further modeling, forecasting, and health system studies.
4. NGOs  e.g AMREF,MSF:Design targeted community-based programs.
5. General public & Advocacy groups:Data visualizations and dashboards make information accessible to citizens and advocacy groups, encouraging data-driven dialogue and accountability in health governance.

## Data Sources
This project relies on publicly available datasets from reputable open data platforms:
1. WorldBank API
Region Code: SSF (Sub-Saharan Africa).Indicators retrieved:Life Expectancy, Under-5 Mortality, Maternal Mortality, Health Expenditure per Capita, HIV Prevalence, 
Measles Immunization Rate, Birth Rate, Population Growth Rate, Total Population, Antenatal Care Coverage & Births Attended by Skilled Staff.
2. WHO API (Global Health Observatory)
Indicators retrieved:Life Expectancy at Birth, Maternal Mortality Ratio, Under-5 Mortality Rate, Health Expenditure (% of GDP) & Immunization Coverage

## Methodology
The workflow involves:
1. Collecting data through APIs
2. Cleaning and merging datasets using Python
3. Uploading processed data to Google BigQuery
4. Creating interactive dashboards in Tableau
## 1. Data Collection
Data was fetched directly from WHO and World Bank APIs using Python’s requests and pandas libraries.Each dataset was filtered to include only Sub-Saharan African countries.
## 2. Data Cleaning and transformation
Both datasets will be loaded into Python using pandas.
Steps to beperformed:
1. Removing duplicates and missing values
2. Renaming columns for consistency (Country_Name, Country_Code, Year, etc.)
3. Standardizing country names across both datasets
Cleaned datasets from both sources will be merged on:
1.Country_Name
2.Country_Code
3.Year
The merged dataset provides a holistic view of health indicators for each Sub-Saharan African country.

## 3.Loading into big query
After merging, the dataset will be uploaded to Google BigQuery for efficient querying and integration with Tableau.

## 4.Visualization in Tableau
Designing dashboards to visualize:
1. Trends in life expectancy across Sub-Saharan countries (2010–2023)
2. Maternal and under-5 mortality by region
3. Correlation between health expenditure and outcomes
4. HIV prevalence trends
### Data Pipeline overview
        +--------------------+
        | WHO API (GHO Data) | +
        | World Bank API     |
        +--------------------+
           
        +--------------------+
        | World Bank API     |
        +--------------------+
                   |
                   v
        +--------------------+
        | Python (pandas)    |
        | - Clean & merge    |
        | - Handle missing   |
        | - Standardize cols |
        +--------------------+
                   |
                   v
        +--------------------+
        | Google BigQuery    |
        | - Storage & Inter- |
        | gration with Tablu|
        +--------------------+
                   |
                   v
        +--------------------+
        | Tableau Dashboards |
        | - Visualize trends |
        | - Explore insights |
        +--------------------+


## Tools used
1. Python: Data extraction, cleaning, transformation
2. Pandas:Data transformation and preprocessing
3. Requests: API data fetching
4. Excel:Preliminary data review
5. Google Bigquery: Cloud data storage and querying
6. Tableau:Visualization and dashboard creation

## Limitations
1. Some countries had incomplete data for certain indicators.
2. Indicator definitions may vary slightly between WHO and World Bank.
3. API access depends on internet stability and endpoint availability.

## Expected Outcomes
1. A cleaned, unified dataset combining WHO and World Bank indicators.
2. Interactive Tableau dashboards illustrating key trends in SSA health.
3. Data-driven insights to inform health policies and international development goals.

## Future work
1. Incorporate more data sources (e.g., UNICEF, Our World in Data).
2. Apply machine learning models to predict health outcomes.
3. Expand the analysis beyond SSA for global comparisons.
