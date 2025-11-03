# Health Indicators and Outcomes Analysis in Sub-Saharan Africa: A Data-Driven Approach Using Open Source APIs
## Introduction
Health outcomes in Sub-Saharan Africa remain a major global concern, with persistent disparities in access, quality and health financing.
Analyzing key health indicators such as life expectancy, child mortality, and maternal health provides valuable insights into regional progress and challenges.
This project leverages open-source data from the World Bank and World Health Organization (WHO) to explore trends and relationships among health indicators across Sub-Saharan African countries using Python, SQL, 
Excel, Tableau, and BigQuery.

## Problem Statement
Despite improvements in healthcare access and outcomes across Sub-Saharan Africa, data gaps and limited integration of health statistics hinder evidence-based decision-making.
Policymakers and researchers often struggle to integrate data from multiple sources to uncover relationships between factors like health expenditure, immunization coverage, and child mortality.
This project addresses the problem by developing a data-driven framework that integrates health data from multiple open APIs, cleans and analyzes the datasets, and visualizes patterns to provide actionable insights
on health progress and disparities across the region.

## Area of study
Sub-Saharan Africa was chosen because it faces unique health challenges, shares similar socioeconomic characteristics, and is often treated as a distinct region in global health reporting — making the 
analysis more focused, relevant, and impactful.

## Main Objective
To explore and analyze key health indicators across Sub-Saharan Africa using open data sources.

## Specific Objectives
1. To collect and integrate health-related datasets from multiple open APIs such as the World Bank and World Health Organization (WHO).
2. To clean, transform, and merge these datasets into a unified analytical format suitable for exploration.
3. To analyze regional trends in core health indicators like life expectancy, child mortality, maternal mortality, and health expenditure.
4. To visualize health trends and disparities across countries using interactive dashboards in Tableau.
5. To generate insights that can inform public health planning, policy decisions, and progress tracking toward SDG 3 (Good Health and Well-being).

## Stakeholders and  Beneficiaries
1. Public Health Policymakers and Government Agencies: They can use the insights to evaluate progress, identify gaps, and allocate resources more effectively toward improving health outcomes.
2. International Health Organizations e.g WHO:The analysis supports monitoring Sustainable Development Goal (SDG) 3 — Good Health and Well-being.
3. Researchers and Data Analysts
4. NGOs  e.g AMREF,MSF:They benefit by identifying regions or populations needing more targeted interventions.
5. General public & Advocacy groups:Data visualizations and dashboards make information accessible to citizens and advocacy groups, encouraging data-driven dialogue and accountability in health governance.

## Data Sources
This project relies on publicly available datasets from reputable open data platforms:
1.WorldBank API
2.WHO API
## Limitations
Additional sources such as UNICEF and Our World in Data were explored, but access restrictions or connectivity issues limited their inclusion.

## Methodology
The workflow involves:
1. Collecting data through APIs
2. Cleaning and merging datasets using Python
3. Uploading processed data to Google BigQuery
4. Creating interactive dashboards in Tableau
## 1. Data Collection
### a.World Bank API
Data was extracted using the requests(API data retrieval) and pandas(Data manipulation and DataFrame conversion) libraries.
The API endpoint https://api.worldbank.org/v2/ was used to fetch development indicators for Sub-Saharan African countries (region code = SSF).
The following indicators were retrieved: 
1. Life_Expectancy 
2. Under5_Mortality 
3. Maternal_Mortality
4. Health_Expenditure_per_Capita
5. HIV_Prevalence
6. Measles_Immunization_Rate
7. Birth_Rate
8. Population_Growth_Rate
9. Total_Population
10. Antenatal_Care_Coverage
11. Births_Attended_by_Skilled_Staff

### b. WHO API
WHO data was accessed through the Global Health Observatory (GHO) API
Key indicators included:
1. Life expectancy at birth (years)
2. Maternal mortality ratio (per 100,000 live births)
3. Under-5 mortality rate (per 1,000 live births)
4. Immunization coverage (%)
5. Health expenditure (% of GDP)
6. HIV prevalence (% ages 15-49)
7. TB incidence per 100,000
8. Malaria incidence

## 2.Data Cleaning and transformation
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

## Tools used
1. Python: Data extraction, cleaning, and merging
2. Pandas:Data transformation and preprocessing
3. Requests: API data fetching
4. Google Bigquery: Cloud data storage and querying
5. Tableau:Visualization and dashboard creation

## Limitations
1. Some countries had incomplete data for certain indicators.
2. Indicator definitions may vary slightly between WHO and World Bank.
3. API access depends on internet stability and endpoint availability.

