# Health Indicators and Outcomes Analysis in Sub-Saharan Africa: A Data-Driven Approach Using Open Source APIs
## Introduction
Health outcomes in Sub-Saharan Africa remain a critical area of concern due to persistent disparities in access, quality, and financing of healthcare services.
Despite global efforts to improve health systems, the region still faces high maternal and child mortality, low life expectancy, and limited healthcare infrastructure.
Analyzing key health indicators — such as life expectancy, health expenditure, GDP per Capita and mortality rates — provides vital insights into progress and challenges.
This project leverages open data from the World Health Organization (WHO) and the World Bank (WB) APIs to integrate, clean, and analyze health indicators across Sub-Saharan Africa using Python, Google BigQuery, and Tableau.
## Concept clarification
### Health indicator
A health indicator is a measurable variable used to describe and monitor specific aspects of a population’s health status or determinants of health.
Examples:
1. Health Expenditure (per capita / % GDP):Represents the input or determinant — how much a country invests in health systems. It influences outcomes but is not itself a result.
2. Birth rate:Represents a demographic measure — number of births per 1,000 population. It affects planning but not a direct health outcome.
3. Population Growth rate:Represents a demographic measure — number of births per 1,000 population. It affects planning but not a direct health outcome.
4. Births attended by skilled  staff:Reflects health service delivery and access to skilled maternal care — an indicator of healthcare quality.
5. Antenatal Care  Coverage:Represents health service utilization (the proportion of pregnant women receiving prenatal care) — an input for improved maternal outcomes.
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
2. Antenatal Care Coverage
3. Births attended by skilled staff
### Demographic indicators
1. Population Growth Rate
2. Total population
3. Birth rate
### Socioeconomic indicators
1. GDP per capita
2. Urban population percentage
3. Adult literacy rate

## Problem Statement
Despite improvements in healthcare access and outcomes across Sub-Saharan Africa, data gaps and limited integration of health statistics hinder evidence-based decision-making.
Policymakers and researchers often struggle to integrate data from multiple sources to uncover relationships between factors like health expenditure, immunization coverage, and child mortality.
This project addresses the problem by developing a data-driven framework that integrates health data from multiple open APIs, cleans and analyzes the datasets, and visualizes patterns to provide actionable insights on health progress and disparities across the region.

## Area of study
<img width="1024" height="1050" alt="image" src="https://github.com/user-attachments/assets/1b47be98-6e44-4736-970e-13123cd1dba6" />

Sub-Saharan Africa, which excludes the North African countries, is the part of Africa that lies below the vast Sahara Desert — a region consisting of 48 countries, home to over a billion people, and rich in cultural heritage and natural resources.
Despite its potential, SSA has historically experienced slower economic growth, higher poverty levels, and weaker health outcomes compared to North Africa and the global average.

## One continent,two realities 
## Why Sub-Saharan Africa Deserves Focussed Analysis
<img width="859" height="547" alt="image" src="https://github.com/user-attachments/assets/08330317-75d0-4829-9908-284149daf856" />
<img width="841" height="547" alt="image" src="https://github.com/user-attachments/assets/ef5ec016-c74c-438b-9869-dc676aca4ca4" />

Africa is the most diverse continent, and aggregated data obscures massive regional disparities, particularly in health outcomes. 
This study focuses specifically on Sub-Saharan Africa (SSA) rather than the African continent as a whole in order to produce a more accurate and meaningful analysis.
Africa is highly diverse, and combining all regions—particularly North Africa, which has significantly higher GDP per capita, stronger economic growth, and better health indicators—creates averages that do not reflect the realities experienced in SSA.
Including wealthier North African countries would artificially inflate the continental averages and mask the structural economic and health disparities that characterize most SSA countries.
By isolating SSA, the analysis concentrates on a more homogeneous region with similar socio-economic challenges, enabling clearer identification of trends, more valid comparisons, and more policy-relevant insights.

## Research Questions
### Descriptive  Research Questions
1. What is the overall trend of life expectancy in Sub-Saharan Africa over the years?
2. Which countries have the highest and lowest life expectancy in SSA?
3. How does life expectancy vary across countries in a single selected year?

### Diagnostic research questions (Why is it happening)
4. What is the relationship between life expectancy and under-5 mortality in SSA?
5. How does health expenditure per capita relate to life expectancy?
6. Does economic performance (GDP per capita) influence life expectancy?
7. Which countries are outliers in the relationship between life expectancy and health expenditure?
8. Are there countries that perform better or worse than expected given their GDP levels?

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

## Results
https://public.tableau.com/app/profile/clare.simba/viz/D1HealthTrendsRanking/D1HeathtrendsRanking?publish=yes
https://public.tableau.com/app/profile/clare.simba/viz/D2HIVSocioeconomiccontext/D2HIVSocioeconomiccontext?publish=yes
https://public.tableau.com/app/profile/clare.simba/viz/D3MaternalChildHealth/D3MCH?publish=yes
https://public.tableau.com/app/profile/clare.simba/viz/D4HealthInvestmentvsOutcome/HealthInvestmentvsOutcome?publish=yes


## Future work
1. Incorporate more data sources (e.g., UNICEF, Our World in Data).
2. Apply machine learning models to predict health outcomes.
3. Expand the analysis beyond SSA for global comparisons.
