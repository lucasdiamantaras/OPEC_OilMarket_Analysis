# About this project
In this data analysis project I mainly use Power BI and Excel to visualize data about the Petroleum Industry, with data obtained from OPEC (Organization of the Petroleum Exporting Countries).

## Objective:
My main objetive was to have a reasonable macroeconomic view of the global market of crude oil over the last 40 to 50 years.

## Why I chose this data?
I chose to work with a dataset that was related to a variety of subjects that interest me. Those being international markets and  historical analysis,  and some chemistry. Considering pretoleum and it derivates are commodities of high interest and debate over the years, I felt the oil market was a great choice.

## Where is the data from?
I obtained data from [OPEC's website](https://asb.opec.org/data/ASB_Data.php).

From the tables available, we can start looking into important macroeconomic metrics, such as:
- Crude Oil reserves
- Output (production)
- Exports of crude oil and products
- Imports of crude oil and products
- Spot Prices
- Demand for crude oil

## Possible limitations of the data:
It's important to point out that this analysis is subject to any bias present in the raw data, that was provided by a single source, OPEC itself, and the data wasn't evaluated for consistency with other sources. Nonetheless, the data is taken as trustworthy and accurate. 

## The data:

I chose the following tables from the database to create the analysis:
*The original naming convention of the database was maintained*

### Crude Oil

- Table 3.1 World proven crude oil reserves by country (mb).xlsx
- Table 5.6 World imports of crude oil by country (1,000 b/d)
- Table 4.7 World oil demand (downstream industry) by country (1,000 b/d)


<!-- - Table 7.2 Selected spot crude oil prices ($/b)

-->





Many interesting questions can be proposed with the data available, to list a few options for now:


### Country-Specific Analysis:

 Which countries have the most considerable crude oil reserves, and how does that compare with their global standing in terms of output and demand?

 Which countries depend the most of imported oil?




### Important definitions:

Oil reserves are measured in million barrels (mb), and Spot Price in $US per barrel.
The other metrics are given in 1000 barrels per day and is recorded at the end of each year. Therefore, **the data is the average number of barrels per day** produced in that year, divided by 1000 for brevity. The dataset spans from 1960 to 2022. 

**Volume of the barrel:** 42 gallons (US) or 159 liters

**Import data:** Data may include re-exports and volumes of oil in transit.

**Oil reserves:** Oil reserves denote discovered quantities of crude oil that can be profitably produced/recovered from an approved development. - *SPE (2018). Petroleum Resource Management System (revised June 2018) (1.01 ed.).*

**Output/production:** crude oil extracted, part of the upstream operations, same as crude oil production.

**Downstream:** refers to the process of taking crude oil and turning into various derivatives. Thus, refers to demand for raw material from refineries and others. Anything after this is said to be further “downstream”. - “The closer an oil and gas company is to the process of providing consumers with petroleum products, the further downstream the company is said to be.” *- Investopedia* -.

**Upstream:** “Upstream operations include exploring new landscapes for oil potential, discovering the crude oil, drilling and extracting it, and the initial discovery part. Another name for the upstream oil sector is the exploration and production (E&P) sector.” *- Investopedia*.

## Methodology:

I started by reviewing all the files to determine their compatibility with Power BI Desktop. Realizing I could import them directly, I proceeded to use Power BI for data transformations and cleaning, utilizing DAX functions and Power Query.

The initial cleaning involved transforming the data structure from a wide format, with years spread across columns, to a long format where years were un-pivoted into a single column. This was necessary for subsequent analysis.

There was an issue with countries being listed in several tables but not having unique IDs to differentiate them. To address this, I created a bridge table that cataloged all possible country-year combinations and assigned a unique identifier to each pair. This step enabled the creation of one-to-many relationships between this bridge table and all other tables, ensuring data integrity and consistency in the analysis.

With that, with have a database with a star schema, where all tables are related by country and year. 

Now we can create our dashboard using Power BI.

## Results Summary:

## Visuals: 

## Future Work:

For future work, we dive deeper into the data available from OPEC. For that I chose to take a look at oil products, things like gasoline and other crude oil fractions.


 #### Oil products (gasoline and other fractions):
- Table 4.5 World output of petroleum products by country (1,000 b/d).xlsx
- Table 5.3 World exports of petroleum products by country (1,000 b/d).xlsx
- Table 4.6 Oil demand by main petroleum product in OPEC Members (1,000 b/d)
- Table 4.8 World oil demand by main petroleum product and region (1,000 b/d)
- Table 5.7 World imports of petroleum products by country (1,000 b/d)
- Table 5.8 World imports of petroleum products by main petroleum product and region (1,000 b/d)
- Table 5.9 World imports of crude oil and petroleum products by country (1,000 b/d) 
- Table 7.6 Spot prices of petroleum products in major markets ($/b).xlsx
