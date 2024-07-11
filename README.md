## Introduction

Sustainergy Advisory Firm has a mission to help EU countries to fasten renewable energy adoption, so, they can reach European Union's ambitious goal to make up 42% renewable energy by 2030. 

We aim to approach the right government in EU countries as our future client who is still left behind in reaching that target. In order to find the right client with right approach, we identify these problem statements and hypotheses:

**Problem 1**: our company doesn't know which government to approach.
**Hypothesis 1**: Our future client will be a country with high GDP but low renewable energy adoption.

**Problem 2**: our company doesn't know what best renewable energy source we could suggest to our future client.
**Hypothesis 2**: the best renewable energy source will be related to natural resources which depends on country's geographic and climate conditions.

**Problem 3**: our company needs to know whether the reason of low renewable energy adoption is related to low investment on innovation in technology.
**Hypothesis 3**: Countries that invest more in research and development (R&D) in renewable energy technologies demonstrate faster growth in renewable energy production.

## Data

* Global Electricity Production: [Kaggle](https://www.kaggle.com/datasets/sazidthe1/global-electricity-production) (121k rows, 6 columns)
* Area of EU Countries: [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/reg_area3__custom_11352231/bookmark/table?lang=en&bookmarkId=fabcfca6-4abb-4a84-ac1c-7bb335af436a)
* Population of EU Countries: [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/DEMO_GIND__custom_7127262/default/table)
* GDP per Capita of EU Countries: [Word Bank](https://data.worldbank.org/indicator/NY.GDP.PCAP.CD)
* R&D investments of EU Countries: [Internationl Energy Agency](https://www.iea.org/data-and-statistics/data-tools/energy-technology-rdd-budgets-data-explorer)
* Average Annual Solar Radiation: [Article by M. Uyan & O.L. Dogmus](https://www.researchgate.net/figure/Average-annual-global-solar-radiation-in-Europe-20_fig2_366202104)

## Hypothesis 1


## Hypothesis 2
Countries with more favorable geographic and climate conditions (e.g., sunlight for solar, wind patterns for wind energy) have higher proportions of renewable energy production. Due to limited time resources, we reduced the scope to solar electricity production and its correlation to the countries' solar radiation exposure.

#### Country Solar Radiation Categorization
Each considered country is categorized by its solar radiation exposure following data on the average annual GHI (Global Horizontal Irradiance) in the period between 1994 and 2016. The map below dsiplays the countries in a color depending on their respective category. Green represents countries with low solar radiation, and red represents countries with high solar radiation.

![Country Solar Categorization](/img/country_categorization_by_solar_radiation.png)

#### Average Annual Solar Net Electricity Production per Category
In order to verify the hypothesis, the average annual electricity production exploiting solar radiation per squarekilometer is calculated for each country in the EU. The figure below displays the data aggregated per radiation category.

Countries categorized for higher radiation tend to have higher solar electricity production rates. Countries in the category "low", however, on average have a higher solar electricity production rate than countries in the categories "medium" or "high".

![Solar Production per Area by Category](/img/solar_production_per_country_radiation_categories_aggregated.png)

#### Average Annual Solar Net Electricity Production per Country
In order to investigate the above findings further, the figure bwloe shows the same data, but without category aggregation and separately for each country instead.

It can be seen, that the "low"-radiation countries' solar electricity production rates are dominated by three countries: Netherlands, Belgium and Germany. Each one of these show a higher rate than the "very high"-radiation countries Spain and Cyprus. In the "very low"-radiation category, Denmark shows a solar rate comparable to the ones of "medium"-radiation. The country with the highest solar rate per area by far is the "very high"-radiation country Malta. 

![Solar Production per Area by Category](/img/solar_production_per_area.png)

## Hypothesis 3
In this section, we would like to understand whether the reason of low renewable energy adoption is related to low investment on innovation in technology.

We need three dataframes to prove Hypothesis 3 which consist of:
- dataframe of renewable energy production of the EU countries for the past 10 years.
- dataframe of R&D budget of the EU countries for the past 10 years.
- dataframe of EU population.

The figure below shows correlation between renewable energy production and R&D budget per capita in the past 10 years of some European countries. It is shown that there is positive correlation between them. 

![Correlation between RE Production and R&D Budget per Capita](/img/RE production vs RnD budget.png)

