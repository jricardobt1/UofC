# **A Data-Driven Exploration of the Substance Abuse Crisis**

An analysis of Opioids and Stimulants in Canada
This project was completed as a group project for the University of Calgary course DATA601 – Working with Data and Visualization. Our team members are:

*	Ruby Nouri Kermani (3026132)

*	Joao Ricardo Targino (30271085)

## Introduction

In recent years, Canada has faced a growing public health emergency: the opioid and stimulant crisis. Data from the Canadian Institute for Health Information (CIHI) reveals a sharp rise in deaths and hospitalizations linked to these substances. Synthetic opioids like fentanyl and stimulants such as methamphetamine are driving the crisis, compounded by deeper issues like poverty, mental illness, and limited access to treatment. 

This project seeks to explore key dimensions of this crisis by addressing four guiding questions:
*	What is the growth percentage of incidents by province from 2016 to 2023?

*	Is there a specific demographic group (age, sex) in which the growth was more prevalent?

*	Is weather relevant to the number of incidents?

*	What is the share of intentional deaths and hospitalizations overall, and is it increasing or decreasing?

## Dataset
Our first dataset is the **Opioid and Stimulant-Related Deaths and Hospitalizations** which is sourced from Health Canada. This dataset spans from 2016 to 2023, includes variables such as geographic location, demographic information, and contextual factors like intentionality. 

We also explored the **Incident-based crime statistics, by detailed violations, police services in the Atlantic provinces** dataset which is sourced from Stat Canada. This dataset spans from 2019 to 2023 and includes key metrics such as the percentage of homicides linked to organized crime gang.

## Packages

*	Pandas

* NumPy

*	Seaborn

*	Matplotlib

*	Regex


## Data Cleaning and Wrangling
Our data comes in a .csv format that is very much clean and free of missing data. We dropped the column PRUID in our first dataset. In order to be able to check regions in both datasets, we grouped some territories to _Canadian Territories_. 

## Exploratory Data Analysis (EDA)

**Guiding Question 1.**
![image](/DATA601/Project/Figuers/CAGR_opioids_stimulants.png)

After we calculated the **Compound Annual Growth Rate (CAGR)** for opioids and stimulants, we understood that the highest growth in opioid deaths occurred in Manitoba and Saskatchewan with a CAGR of **17.5%**

#### Opioids:

Three provinces with a large population share — Alberta (AB), British Columbia (BC), and Ontario (ON) — had growth rates of around 15%. Quebec, despite being the third most populous, saw growth similar to smaller regions like Atlantic Canada and the Territories - approximately 10%. Nationally, Canada’s CAGR for opioid deaths from 2016 to 2023 was **14.8%**.

#### Stimulants:

imilar to opioids, stimulant-related deaths were notably higher in Central Canada, where growth rates exceeded 30%. Nationally, Canada’s stimulant death growth was about half that rate. British Columbia and Quebec were exceptions, with growth rates under **5%**. Canadian Territories figures while concerning, have to be taken with caution because the size of the sample and population, but a **45%** Growth increase is always concerning.

This highlights regional differences in stimulant-related deaths, with Central Canada seeing the largest increases, while British Columbia and Quebec experienced more less aggressive trends.

**Guiding Question 2.**

![image](/DATA601/Project/Figuers/Age_group_death_opioids_stimulants.png)

The data indicates that individuals aged 30 to 39 years are the most affected, followed closely by those aged 40 to 49 years. Notably, the presence of young adults (0–19 years) in these statistics is concerning, with 2% of opioid-related cases and 1% of stimulant-related cases. Additionally, there is a growing impact on the 60+ age group, with opioid-related cases rising from 9% in 2016 to 11% in 2023. The trend is even more pronounced for stimulants, where cases in this age group increased by 50% (from 8% to 12%). Given the overall rise in substance-related deaths, the increasing impact on both older adults and younger individuals is a significant public health concern.

![image](/DATA601/Project/Figuers/Gender_death_opioid_stimulants.png)

There is a clear male predominance in substance-related deaths, with males consistently representing over 70% of cases. While opioid-related fatalities among females declined slightly from 30% in 2016 to 28% in 2023, the opposite trend is observed for stimulants, where the proportion of female cases increased from 24% in 2018 to 26% in 2023.

![images](/DATA601/Project/Figuers/Gender_age_opioid_death.png)

The charts above illustrate that the 30-39 and 40-49 age groups are predominantly male, consistently accounting for over 80% of victims. This aligns with earlier findings on age and gender distribution.

However, the proportion of female victims in younger age groups have risen significantly in recent years. In the youngest group, the female share increased from 25% to over 50%, while in the next group, it grew from 22% to nearly 40%. Among those aged 60 and older, the percentage of female victims increased in 2023 compared to 2022 but remains lower than in the early years of the dataset, when it was around 25%.

![images](/DATA601/Project/Figuers/Gender_age_stimulants_death.png)

Similar to Opioids, Stimulant-related deaths among females have increased in younger age groups. The percentage of female victims in the 0-19 age group doubled, rising from 24% to 48.1%, while the 20-29 group saw an increase from 30% to 37%. In contrast, other age groups remain largely male-dominated with consistent averages over time.

**Guiding Question 3.**

Q1 (January - March): Winter (cold, snow, shorter daylight hours)

Q2 (April - June): Spring (mild, transitioning to warmer weather)

Q3 (July - September): Summer (warmest, longer daylight hours)

Q4 (October - December): Fall (cooling temperatures, shorter daylight hours)

![images](/DATA601/Project/Figuers/average_death_hospitalization_quarter.png)

Death rate: Q4 > Q2 > Q3 > Q1

Deaths related to opioid and stimulant use are highest in the fourth quarter (October-December) and lowest in the first quarter (January-March).

Hospitalization rate: Q3 > Q2 > Q4 > Q1

Hospitalizations related to opioid and stimulant use are highest in the third quarter (July-September) and lowest in the first quarter (January - March).

![image](/DATA601/Project/Figuers/death_hospitalization_quarter_year.png)

There is a notable growth observed around the years 2020 and 2022, a period that coincides with the COVID-19 pandemic. We believe that the pandemic escalated the opioid and stimulant crisis in several ways.

![image](/DATA601/Project/Figuers/average_total_death_region_quarter.png)

![image](/DATA601/Project/Figuers/average_hospitalizations_region_quarter.png)

Both plots exhibit some seasonal variations in deaths and hospitalizations, with deaths tending to peak in the fourth quarter (October-December) and hospitalizations often highest in the third quarter (July-September). These patterns may be attributed to factors such as weather, social gatherings, and holiday seasons, which can influence substance use behaviors.

British Columbia and Ontario show the highest average death and hospitalization rates, indicating more severe crisis of opioids and stimulants compared to other regions.

**Guiding Question 4.**

![image](/DATA601/Project/Figuers/opioid_stimulant_ratedeath_Region.png)

The death-to-hospitalization rate is a critical metric for understanding the trajectory of this crisis. While we observe growth in this rate (as shown on Guiding Question #1), a rate lower than 1 suggests that hospitalizations are outpacing deaths, offering a chance to save more lives. However, the data from the past three years across all regions, including Canada, indicates that the rate has consistently exceeded 1 in all provinces except Territories. For instance, in 2023, Manitoba had twice as many deaths as hospitalizations, while Alberta had a rate of 1.5.

A concerning trend is the increase in this rate across all regions from 2016 to 2023, especially during the pandemic years (2020-2022). This points to a worsening situation that will likely be more difficult to control than before. Education on harm reduction and guidance on treatment options in hospitals and other healthcare facilities are key to reducing this rate, saving lives, and improving the overall situation.

**Guiding Question 5.**

![image](/DATA601/Project/Figuers/opioid_stimulant_ratedeath_age.png)

The death-to-hospitalization rate for males remains above 1 across all age groups, highlighting a severe issue—many cases are beyond recovery. While higher rates in middle-aged groups are expected, the alarming fact is that both young individuals (under 19) and older adults (over 60) also exhibit these high rates. This raises critical concerns about what preventive measures can be taken to address the issue in these vulnerable groups.

For females, the trend is somewhat similar; however, the oldest age group shows a rate below 1, indicating a slightly less severe situation. Additionally, the peak values for females are significantly lower than those for males, which aligns with the 70/30 case distribution observed earlier.

![image](/DATA601/Project/Figuers/opioid_stimulant_ratedeath_age_gender.png)

The death-to-hospitalization rate for stimulants presents an even more alarming scenario. Among males, the 50–59 age group has maintained a rate above 10 for the past three years, meaning that for every one hospitalization, there are ten fatalities. Even more concerning is that the 60+ age group also approaches this critical threshold. Authorities must investigate the underlying causes behind such extreme substance abuse in these demographics. For instance, if a particular occupation or social factor is contributing to this crisis, targeted awareness campaigns could help mitigate the issue. Unlike the trend observed with opioids, there is no significant decline in stimulant-related fatalities from 2022 to 2023, indicating that the crisis remains severe and unresolved.

**Guiding Question 6.**

![image](/DATA601/Project/Figuers/opioid_stimulant_death_vs_homicide.png)

We see that in 2019, the combined numbers were significantly lower compared to 2022 and 2023. This suggests a positive correlation, as the numbers have increased together over time. 

![image](/DATA601/Project/Figuers/opioid_death_vs_homicide_region.png)

![image](/DATA601/Project/Figuers/stimulant_death_vs_homicide_region.png)

Since both substances (Opioids and Stimulants) are illegal, we can observe a correlation between gang-related homicides (a proxy for gang activity in a province) and substance-related deaths. As seen in the death statistics (Guiding Questions 1 and 4), this trend has surged dramatically over the past two years. In most provinces, crime rates have been rising at a similar pace. Looking at the charts for British Columbia, Ontario, and Manitoba for Opioids and BC and ON for Stimulants, we see clear spikes in both deaths and gang-related homicides in 2022 and 2023, highlighting this alarming trend seen in previous questions.

![image](/DATA601/Project/Figuers/reletive_number_opioid_death_vs_homicide_region.png)

Alberta experienced consistent growth in both metrics from 2020 to 2023, with the only exception being in 2022. Manitoba in contrast, saw a sharp increase in homicide rates in 2022 and 2023, despite having much lower rates in previous years, even though opioid-related deaths remained high. On the other hand, the less populated regions of the country, including Saskatchewan, the Atlantic provinces, and the Territories, have been witnessing a decline in both homicide and opioid-related death rates in recent years.

![image](/DATA601/Project/Figuers/reletive_number_stimulant_death_vs_homicide_region.png)

When examining the relative data for stimulants, troubling patterns emerge once again. Manitoba and British Columbia have seen an increase in both rates over the years, suggesting higher activity in these provinces. In contrast, Saskatchewan, Atlantic Canada, and Ontario (only in 2023) have experienced a decline in these rates. Notably, Alberta has not disclosed data on stimulant-related deaths.

## Conclusion

The analysis of opioid and stimulant-related harms in Canada reveals significant regional and demographic trends. The highest growth in opioid-related deaths occurred in Manitoba and Saskatchewan, while stimulant-related deaths were more prevalent in central Canada. The most affected demographic was males aged 30-39, though stimulant-related deaths among younger females have shown a concerning increase. Seasonal patterns were evident, with the highest number of deaths occurring in Q4 (October–December) and the lowest in Q1 (January–March). Notably, the years 2020–2022 saw a sharp increase in deaths related to both substances, likely exacerbated by the COVID-19 pandemic. Geographically, British Columbia and Ontario reported the highest average death and hospitalization rates for opioids and stimulants. Additionally, Manitoba had a death-to-hospitalization rate twice as high as Alberta, highlighting regional disparities in the severity of the crisis.

## Refrences

* Canadian Centre on Substance Use and Addiction. Opioids. Available at: https://www.ccsa.ca/opioids#:~:text=Canada%20is%20experiencing%20a%20drug,involved%20stimulants%20or%20other%20substances.

* Public Health Agency of Canada. (2023). Opioid- and Stimulant-related Harms in Canada [Dataset]. Health Infobase. https://health-infobase.canada.ca/substance-related-harms/opioids-stimulants/

* Statistics Canada. (2023). Homicides in Canada, by province/territory and link to organized crime or street gangs. https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=3510017801

