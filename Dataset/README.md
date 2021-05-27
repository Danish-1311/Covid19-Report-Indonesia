# Indonesia Covid-19 Datasets

In the Dataset directory, there are several datasets that we have been collecting and/or aggregating, such as:
- __owid_covid_data__: This dataset originally have been collected from [Our World in Data (OWID)](https://ourworldindata.org/) for over country. As of 26 January 2021 the dataset columns are the columns are: 
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
(For more details, please check it out at [our syntax](/Syntax/Covid19_ID_owid.ipynb). The columns are same as the __owid_covid_data__ dataset.

- __covid_prov_id__: This dataset orginally have been collected from [Our World in Data (OWID)](https://covid19.go.id/)

- __covid19_inndonesia_complete_version__:
