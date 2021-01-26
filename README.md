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