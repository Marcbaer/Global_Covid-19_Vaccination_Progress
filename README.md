# Analysis of the Global Covid-19 Vaccination Progress

This Project analyzes the progress of covid vaccination in different countries by investigation the [COVID-19 World Vaccination Progress Dataset](https://www.kaggle.com/gpreda/covid-world-vaccination-progress) from [Our World Data](https://ourworldindata.org/).
The data is enriched with [GDP per Capita Information](https://data.worldbank.org/indicator/NY.GDP.PCAP.CD) provided by the world bank and [country population information](https://population.un.org/wpp/Download/Standard/CSV/) provided by the United Nations.
The enriched data allows insights into the demographic and economic situations of the analysed countries and their progress on vaccinating their citizens.
The data is being transformed to optimize the analytical insights.

The notebook is structured as followed:

* **Data Cleaning and Merging**: Reading and merging the collected datasets
    * Drop unused columns
    * Clean columns with missing values
    * Transform categorical values
    
    
* **Exploratory Data Analysis**: Deliver insights into the data by analysing the following questions:
    * Recent Daily Vaccinations per million citizens per country
    * US Daily Vaccination Rate
    * Association between GDP per Capita and percent of vaccinated citizens
    * Association between population size and percent of vaccinated citizens
    * Regression Coefficients for population size, GDP per Capita and population density
    * Vaccines Analysis: Are there vaccines mainly accessible for countries with a high GDP per Capita?
	
## Environment

* python 3.6
* pandas 1.0.5
* numpy 1.18.5
* matplotlib 3.2.2
* seaborn 0.11.1
* sklearn 0.23.1

## How to run the analysis

The notebook [EDA_Covid_Vaccination.ipynb](EDA_Covid_Vaccination.ipynb) contains the ETL and Analysis process.

## Results

**Association between GDP per Capita and percent of vaccinated citizens**
<img src="GDP_vs_PercVacc.png">

**Association between population size and percent of vaccinated citizens**
<img src="PopSize_vs_PercVacc.png">

**Regression Coefficients for population size, GDP per Capita and population density**

Running a linear regression for total percentage of vaccinated citizens resulted in the following coefficients:
* **Population Size: (Negative)** -1.63475623e-06
* **GDP per Capita: (Positive)** 2.32138617e-05
* **Population Density: (Positive)** 2.81426369e-04

**Vaccines Analysis: Are there vaccines mainly accessible for countries with a high GDP per Capita?**
<img src="Vacc_plot.png">


## Evaluation

Countries with a high GDP per Capita seem to be able to vaccinate their citizens faster than other countries. However, given the regression coefficent the population density plays an even more important role. It seems that countries with a high population density give strong effort in vaccinating their citizens as fast as possible. For countries with a total population above 100 Million, the logistics and organisational hurdles seem to slow down the process of vaccinating the citizens agains Covid-19.
Additional insights was provided by analysing the different vaccines. While Moderna is mainly used by North American and Western European countries, Sinovac and Sinopharm is popular in Asia.