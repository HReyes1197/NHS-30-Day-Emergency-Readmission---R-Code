# NHS-30-Day-Emergency-Readmission---R-Code
This highlights a personal project I have been working on, analyzing the effects of sex and deprivation quintile on the 30-day emergency readmissions documented by the NHS England. Please find the full executive summary at my linkedin: www.linkedin.com/in/hannah-reyes-03 


The evaluation of disparities in persons readmitted to a hospital less than 30 days after discharge
NHS UK Readmission Data
Stakeholder
The National Health Service (NHS) in England is a publicly funded healthcare system seeing approximately 1.3 million people a day. The NHS aims to improve health and care outcomes. As part of that aim, the NHS measures several health indicators to assess the quality of care the public receives through their services. Based on these responsibilities and the self-produced indicators, this study aimed to provide the NHS with additional information to address disparities for health indicator 3.2. This indicator “measures the percentage of emergency admissions to any hospital in England occurring within 30 days of the most recent discharge from a hospital.”
Summary of Findings
There was a significant difference in percent of 30-day readmissions by sex.
There was a significant effect measure modification of sex on the percent of 30-day readmissions by sex.
After stratifying for sex, 
The least deprived quintile of males had 11.4% lower odds of a 30-day readmission compared to the males in the most deprived quintile.
The least deprived quintile of females had 14.1% lower odds of a 30-day readmission compared to the females in the most deprived quintile.

Introduction
30-Day Emergency Readmissions
The indicator measuring the percentage of emergency admissions to any hospital in England occurring within 30 days of the most recent hospital, or the 30-day emergency readmission percentage, is a key metric for assessing healthcare quality and patient outcomes. A low readmission rate may suggest that patients receive effective treatment during their initial hospital stay, appropriate discharge planning, and post-discharge support. A high readmission rate may suggest potential issues in the quality of care, such as an early discharge, inadequate treatment, or insufficient post-discharge support. 

Disparities
Social factors, and deprivation levels have been well-documented to lead to negative healthcare outcomes over the years. Notably, in November 2024, a British Red Cross study found that people who frequently attended the Accident and Emergency (A&E) department in Dorset were “72 percent more likely to live in an area of deprivation.” This recent article begs the question of comparing potential deprivation quintiles across England. More data describing the effect deprivation indicators may have can provide new insight into 30-day emergency readmission rates.
Goals
The study aimed to fill the void of recent studies examining 30-day readmission rates across England by sex and deprivation quintile to provide additional information to the NHS in England by examining the NHS 30-Day Emergency Readmission data.

Methods
Data Source and Sample
The data source for this study is from the NHS emergency readmissions to hospital within 30 days of discharge published 26 November, 2024. This indicator calculates the standardized percentage of emergency admissions to any hospital in England. The data excludes cancer and obstetrics admissions as these readmissions may be part of the patient’s care plan. 2 
The NHS in England utilizes the Hospital Episode Statistics for Admitted Patient Care (HES APC) linked as Continuous Inpatient (CIP) Spells for the denominator and numerator for this indicator. These values for the denominator were collected up to the 31st of March in the 2023-2024 financial year. The values for the numerator were collected up to 30 days after the end of the 2023-2024 financial year.
The NHS in England utilizes the Index of Multiple Deprivation (IMD) Quintiles. The IMD measures deprivation for small areas in England, by assessing seven main indicators: Income, Employment, Education, Health, Crime, Barriers to Housing and Services, and Living Environment. The most deprived quintile is the 1st quintile and the least deprived is the 5th quintile.

Variables 
Outcome
30-day Emergency Readmission
Primary Exposure
Indices of Deprivation
Other Covariates of Interest
Sex

Statistical Analysis
Demographic characteristics of the sample were described by 30-day emergency readmission percentage, reporting frequencies and percentages for categorical variables. 
Differences in demographic characteristics by percent of 30-day readmissions were calculated using a two-proportion z-test for categorical variables due to the large population size. 
The independent associations between sex and 30-day readmission rate were tested using logistic regression. 
Effect modification of sex was tested using outcome*indices of deprivation interaction terms. (Where indices of deprivation is equal to IMD)
All statistical analyses were performed using RStudio 2024.12.1+563  at α=0.05 significance level.


Results
The NHS emergency readmissions data included 6,340,538 participants. The data was stratified for sex and then separated into persons who were readmitted within 30-days compared to those who were not readmitted within 30-days.
There was a statistically significant difference in 30-day readmissions between males and females. (Table 1)
There was a significant difference in the relationship between deprivation quintile and 30-day readmission risk by sex, indicating effect modification by sex. (Table 2)
The least deprived quintile of males had 11.4% lower odds of a 30-day readmission compared to the males in the most deprived quintile. (Table 3)
The least deprived quintile of females had 14.1% lower odds of a 30-day readmission compared to the females in the most deprived quintile. (Table 3)

Limitations
This analysis was limited to publicly available aggregated datasets, limiting the amount of other covariates of interest that could be analyzed at one given time. Future studies should test the significance of other covariates such as the region of England, age, and race. Furthermore, this study is limited in its ability to provide clinical insight lto the statistically significant differences observed. A longitudinal analysis assessed the trends across clinical areas leading to the 30-day emergency readmissions from 2006 to 2016. This study found large variations in trends across clinical areas, so overlaying deprivation quintiles over clinical areas could prove to be interesting. Lastly, this study is limited in its definition of sex. The datasets available are limited to the definition of male and female, not specifying the diverse spectrum that comes along with gender. More research on these changing trends in clinical areas should be done for more recent data.

Public Health Relevance
In this project, an association between deprivation factors and a 30-day emergency hospital readmission was found. Specifically, persons in the most deprived group have higher odds of being readmitted to the emergency room within 30-days of their discharge. Notably, sex was found to be an effect modifier. This means that a person's sex affects their 30-day readmission odds. Though the odds ratios for males and females followed similar patterns, females showed a slightly greater reduction in readmission odds as deprivation decreases.

This information can be used by the NHS to promote health and encourage healthcare teams to provide appropriate discharge planning and post-discharge support. Patients undergoing stressors in one or more of the seven deprivation indicators (income, employment, education, health, crime, barriers to housing and services, and living environment) may be provided additional support to ensure a successful discharge and reacclimation to daily life. Increasing these educational initiatives for healthcare teams may result in fewer emergency hospital readmissions within the first 30-days of discharge.
