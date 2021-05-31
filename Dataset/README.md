# Indonesia Covid-19 Datasets

In the Dataset directory, there are several datasets that we have been collecting and/or aggregating, such as:
- __owid_covid_data__: This dataset originally have been collected from [Our World in Data (OWID)](https://ourworldindata.org/) for all countries in the world.
 As of 26 January 2021 the dataset columns are: 
`iso_code`, `continent`, `location`, `date`, `total_cases`, `new_cases`, `new_cases_smoothed`, `total_deaths`, `new_deaths`, 
`new_deaths_smoothed`, `total_cases_per_million`, `new_cases_per_million`, `new_cases_smoothed_per_million`, `total_deaths_per_million`, `new_deaths_per_million`, 
`new_deaths_smoothed_per_million`, `reproduction_rate, icu_patients`, `icu_patients_per_million`, `hosp_patients`, `hosp_patients_per_million`, `weekly_icu_admissions`, 
`weekly_icu_admissions_per_million`, `weekly_hosp_admissions`, `weekly_hosp_admissions_per_million`, `total_tests`, `new_tests`, `total_tests_per_thousand`,
`new_tests_per_thousand`, `new_tests_smoothed`, `new_tests_smoothed_per_thousand`, `positive_rate`, `tests_per_case`, `tests_units`, `total_vaccinations`, `people_vaccinated`, 
`people_fully_vaccinated`, `new_vaccinations`, `new_vaccinations_smoothed`, `total_vaccinations_per_hundred`, `people_vaccinated_per_hundred`, `people_fully_vaccinated_per_hundred`, 
`new_vaccinations_smoothed_per_million`, `stringency_index`, `population`, `population_density`, `median_age`, `aged_65_older`, `aged_70_older`, `gdp_per_capita`, 
`extreme_poverty`, `cardiovasc_death_rate`, `diabetes_prevalence`, `female_smokers`, `male_smokers`, `handwashing_facilities`, `hospital_beds_per_thousand`, `life_expectancy`, 
`human_development_index`. 
__For more details about the original dataset, please visit__ [Our World in Data (OWID)](https://github.com/owid/covid-19-data/tree/master/public/data)

- __cov19_id_owid__: This dataset originally have been collected from [Our World in Data (OWID)](https://ourworldindata.org/), but filtered for Indonesia region only. 
The original dataset contains missing value, so we handle the missing value with two ways: __(1)__ using ffill method, then __(2)__ fill the rest missing value with 0 
(For more details, please check it out at [Covid19_ID_owid.ipynb](/Syntax/Covid19_ID_owid.ipynb)). The columns are same as the __owid_covid_data__ dataset.

- __covid_prov_id__: This dataset orginally have been collected from [Satgas Penangangan Covid-19](https://covid19.go.id/) for all provinces in Indonesia.
The dataset columns are: `date`, `province`,	`new_cases`,	`new_deaths`,	`new_recoveries`,	`new_hospitalizations`,	`total_cases`,	`total_deaths`,	`total_recoveries`,	`total_hospitalizations`. We have build second page of the dashboard based on this dataset. For more details about how to access the dataset, please check it out at [covid_api_prov.ipynb](/Syntax/covid_api_prov.ipynb)

- __covid19_indonesia_complete_version__: This dataset has been made by merging the __cov19_id_owid__ dataset and [Satgas Penangangan Covid-19](https://covid19.go.id/) for Indonesia daily update dataset. Why we merged these two datasets? it's because we don't have access to get `new_test` covid-19 data from [Satgas Penangangan Covid-19](https://covid19.go.id/) for Indonesia daily update dataset. Then, what if there are different values with the same columns between these two datasets? We use `new_cases`,	`new_deaths`,	`new_recoveries`,	`new_hospitalizations`,	`total_cases`,	`total_deaths`,	`total_recoveries`,	`total_hospitalizations` data from [Satgas Penangangan Covid-19](https://covid19.go.id/) dataset, while the rest of data we use data from __cov19_id_owid__ dataset. For more details, please check it out at [Covid19_Indonesia_Complete_Version.ipynb](/Syntax/Covid19_Indonesia_Complete_Version.ipynb)
