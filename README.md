# Econ-388-Data-Project-3
Data Project 3: Estimating the effects of covid on the housing prices

	In this Readme file, I detail where I got my data for my project and what I did to merge it.

Source 1: Age Demographics by County
Link: https://www.census.gov/data/tables/time-series/demo/popest/2020s-counties-detail.html
From this data set, I used the columns titled “STNAME, YEAR, CTYNAME, STATE, COUNTY, AGE65PLUS_TOT”, which include data on the state name, city name, state, county, and total number of residents over the age of 65. The reason for the use of the total number of residents over the age of 65 is to calculate the percentage of the population above the retirement age. This is used to try and estimate the effects of age density on housing prices.

Source 2: Race Demographics by County
Link: https://www.census.gov/data/tables/time-series/demo/popest/2020s-counties-detail.html
This data set was acquired from the same place as the Source 1. I used to columns titled “STNAME, YEAR, CTYNAME, STATE, COUNTY, TOT_POP, WA_MALE, WA_FEMALE, BA_MALE, BA_FEMALE, IA_MALE, IA_FEMALE, AA_MALE, AA_FEMALE, NA_MALE, NA_FEMALE” which include some of the same data points as the first source as well as total population numbers for male and female residents of different races. This is used to estimate the effects of different areas having different racial density and the fact that this could also be correlated with housing price.

Source 3: HPI Data
Link: https://www.fhfa.gov/DataTools/Downloads/Pages/House-Price-Index-Datasets.aspx
The data from this data set was used to form our dependent variable of 2021 HPI values and an independent variable for 2020 HPI values. The 2020 HPI values were used to test for level one serial correlation.

Source 4: Regional Classification Data
Link: https://www.fhfa.gov/DataTools/Downloads/Pages/House-Price-Index-Datasets.aspx
This data was found using a link on Github. It helps classify the states based on region which is then used as a categorical variable to compensate for reginal differences in HPI.

Source 5: U.S. Covid Data
Link: https://www.nytimes.com/article/coronavirus-county-data-us.html
This data was acquired from the New York Times and has data on numbers of Covid deaths per county on the United States. This was used to calculate the covid mortality rate per county in 2020. The data was filtered to use only the year 2020. 

	This data was used to estimate the impact of the covid mortality rate in 2020 on housing prices in 2021. The code organizes and parses the data into one clean final dataset and then runs a regression on it.
![image](https://user-images.githubusercontent.com/102060119/232672594-b2613f7c-a27e-4750-90d7-c0ef1a12bbd4.png)
