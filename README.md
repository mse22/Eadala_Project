# Environmental Data Analytics Project by Monisha Eadala

Final project repository for Environmental Data Analytics (ENV 872L) at Duke University, spring 2020

<Instructions: copy and paste this template into your project README file (found in the parent folder of the repository). Fill in relevant information as requested.>

<General notes: add as much information as is relevant for your repository. Some overarching guidelines are provided, but feel free to expand on these guidelines.>
<More resources found here: https://www.dataone.org/all-best-practices>
<Delete the text inside the brackets when formatting your file.>

## Summary

<describe the purpose of this repository, the information it contains, and any relevant analysis goals. What, why, where, when, how?>

The repository contains different aspects and the progress of the final project right from its inception to completion. My goal is to study water quality with the help of the NTL-LTER Lake Datasets provided to us through the Environmental Data Analytics class taught at Nicholas School of the Environment in Spring 2020.

Eutrophication is a phenamenon caused due to excess of nutrients in water and it causes structural changes to the ecosystem in the form of increased production of algae and aquatic plants, depletion of fish species, general deterioration of water quality and other effects that reduce and preclude use. Therefore, it is important to observe and manage lakes and their nutrient loading from time to time to conserve water and other ecosystems dependent on it.

Through this project and its relevant datasets, I hope to understand eutrophication and the correlations between certain elements and nutrients. I intent to answer my research questions through the data wrangling, processing, exploring, and visualization techniques taught in the class. 

## Investigators

<name(s), affiliation(s), contact information, roles (if applicable)>

## Keywords

<add relevant keywords here>

## Database Information

<describe the origin of all data in the repository, including data collected from outside sources and new data generated by the investigator(s). If data was accessed from an outside database, the date(s) of data access should also be included.>

The dataset contains data from studies on several lakes in the North Temperate Lakes District in Wisconsin, USA. Data were collected as part of the Long Term Ecological Research station established by the National Science Foundation. 


## Folder structure, file formats, and naming conventions 

<describe the folders contained in the repository, including what type of files they contain>

<describe the formats of files for the various purposes contained in the repository>

<describe your file naming conventions>

The folders contained in the reposity are: 1. "Data" folder further subdivided into "Raw" and "Processed" folders that each contain their relevant csv files, 2. "Code" folder that contains the three R markdown files - "Processing_Wrangling", "Data_exploration" and "Data_analysis" 3. Final project files in r markdown and PDF formats. The files are either named as per their description of the data, or their function. For example, raw datasets in the initial stage are named "raw", while any dataset that has departed from the raw dataset is named "processed". The R markdown files are named according to the stages of the analysis; for example, the code relevant to the processing and wrangling stages of the project are in the file named "Processions_Wranging" and the code relevant to the data exploration stage of the project is named "Data_exploration". The CSV files will be named according to their default name named by its source, important elements or column names that they contain, and if their raw or processed datasets.

## Metadata

Data were collected from the North Temperate Lakes Long Term Ecological Research website. More information can be found here: https://lter.limnology.wisc.edu/about/overview. Data were collected using the Data tool (https://lter.limnology.wisc.edu/data).

<For each data file in the repository, describe the data contained in each column. Include the column name, a description of the information, the class of data, and any units associated with the data. Create a list or table for each data file.> 

There are three raw data filed in the repository:
1. 'NTL-LTER_Lake_Carbon_Raw.csv' file: This contains data relevant to dissolved organic and inorganic carbon, particulate organic matter, partial pressure of CO2 and absorbance at 440nm. Samples were collected with a Van Dorn sampler. Organic carbon and absorbance samples were collected from the epilimnion, metalimnion, and hypolimnion (upper, intermediate, and lower layers of the stratified lakes respectively). Inorganic samples were collected at depths corresponding to 100%, 50%, 25%, 10%, 5%, and 1% of surface irradiance, as well as one sample from the hypolimnion. Samples for the partial pressure of CO2 were collected from two meters above the lake surface (air) and just below the lake surface (water). Sampling frequenc varies, and the number of site are 14. The file contains the below column names and their relevant details:

Column Name        | Class    | Units   |Relevant Dataset Information
-------------------|----------|---------|----------------------------
lakeid             | factor   | -       | Provides the IDs of the lakes either in the form of capital letters or words; for example, L, R, T, E, Tbog, Roach, Ward, etc. 
lakename           | factor   | -       | Provides the names of the lakes; for example, Paul Lake, Peter Lake, Tuesday Lake, East Long Lake, etc.
year4              | integer  | -       | Provides the year in which its respective data was collected in four digits
daynum             | integer  | -       | Provides the number of the day on which its data was collected from from 1 to 366
sampledate         | factor   | -       | Provides the date on which its data was collected in m/d/y format
depth              | factor   | m       | Provides the depth at which the data sample was collected in meters
depth_id           | integer  | -       | Provides the depth level categorizied from -2 to 7; 1 represents 100% light, 2 represents 50% light, 3 represents 25% light; 4 represents 10% light, 5 represents 5% light, 6 represents 1% light, 7 means Hypolimnion, -1 means Epilimnion/PML, and -2 means Metalimnion
tpc                | numeric  | mg/L    | Provides the total particulate carbon
tpn                | numeric  | mg/L    | Provides the total particulate nitrogen
DIC_mg             | numeric  | mg/L    | Provides the dissolved inorganic carbon measured in milligrams per liter
DIC_uM             | numeric  | uM/L    | Provides the dissolved inorganic carbon measured in micro-mole per liter
air_pco2           | numeric  | uatm    | Provides the partial pressure of CO2 (pCO2) is the amount of free CO2 in air
water_pco2         | numeric  | uatm    | Provides the partial pressure of aqueous CO2 (pCO2) is the amount of free CO2 in water
doc                | numeric  | mg/L    | Provided the dissolved organic carbon concentration
absorbance         | numeric  | Au      | Provides the measure of the capacity of the water to absorb light of a certain wavelength in absorbance units

2. 'NTL-LTER_Lake_ChemistryPhysics_Raw.csv' file: This contains data relevant to physical and chemical variables (such as temperature, dissolved oxygen, and irradiance) that are measured at one central station near the deepest point of each lake. In most cases these measurements are made in the morning (8 to 9 am). It contains the below column names and their relevant details:


Column Name       | Class     | Units   | Relevant Dataset Information
------------------|-----------|---------|-----------------------------
lakeid            | factor    | -       | Provides the IDs of the lakes either in the form of capital letters or words; for example, L, R, T, E, Tbog, Roach, Ward, etc. 
lakename          | factor    | -       | Provides the names of the lakes; for example, Paul Lake, Peter Lake, Tuesday Lake, East Long Lake, etc.
year4             | integer   | -       | Provides the year in which its respective data was collected in four digits
daynum            | integer   | -       | Provides the number of the day on which its data was collected from from 1 to 366
sampledate        | factor    | -       | Provides the date on which its data was collected in m/d/y format
depth             | numeric   | m       | Provides the depth at which the data sample was collected in meters
temperature_C     | numeric   | C       | Provides the water temperature in celcius
dissolvedOxygen   | numeric   | mg/L    | Provides the dissolved oxygen measurement in milligrams per liter
irradiancewWater  | numeric   | uE      | Provides the photosynthetically active radiation measured in the water column in micro-Einstein 
irradianceDeck    | numeric   | uE      | Provies the photosynthetically active radiation measured on the deck of the sampling boat in micro-Einstein
comments          | factor    | -       | Provides the comments noting departure from standard procedure 

3. 'NTL-LTER_Lake_Nutrients_Raw.csv' file: This contains the data relevant to physical and chemical variables (such as total nitrogen, total phosphorius, ammonia and ammonium, nitrite and nitrate, and phosphate concentrations) that are measured at one central station near the deepest point of each lake. In most cases these measurements are made in the morning (8 to 9 am). It contains the below column names and their relevant details:

Column Name        | Class    | Units   | Relevant Dataset Information
-------------------|----------|---------|-----------------------------
lakeid             | factor   | -       | Provides the IDs of the lakes either in the form of capital letters or words; for example, L, R, T, E, Tbog, Roach, Ward, etc. 
lakename           | factor   | -       | Provides the names of the lakes; for example, Paul Lake, Peter Lake, Tuesday Lake, East Long Lake, etc.
year4              | integer  | -       | Provides the year in which its respective data was collected in four digits
daynum             | integer  | -       | Provides the number of the day on which its data was collected from from 1 to 366
sampledate         | factor   | -       | Provides the date on which its data was collected in m/d/y format
depth_id           | integer  | -       | Provides the depth level categorizied from -2 to 7; 1 represents 100% light, 2 represents 50% light, 3 represents 25% light; 4 represents 10% light, 5 represents 5% light, 6 represents 1% light, 7 means Hypolimnion, -1 means Epilimnion/PML, and -2 means Metalimnion
depth              | numeric  | m       | Provides the depth at which the data sample was collected in meters
tn_ug              | numeric  | ug/L    | Provides the total nitrogen concentration in micrograms per liter
tp_ug              | numeric  | ug/L    | Provides the total phosphorus concentration in micrograms per liter
nh34               | numeric  | ug/L    | Provides the ammonia and ammonium concentration in micrograms per liter
no23               | numeric  | ug/L    | Provides the nitrite and nitrate concentration in micrograms per liter
po4                | numeric  | ug/L    | Provides the phosphate concentration in micrograms per liter
comments           | factor   | -       | Provides any additional comments


## Scripts and code

<list any software scripts/code contained in the repository and a description of their purpose.>

## Quality assurance/quality control

<describe any relevant QA/QC procedures taken with your data. Some ideas can be found here:>
<https://www.dataone.org/best-practices/develop-quality-assurance-and-quality-control-plan>
<https://www.dataone.org/best-practices/ensure-basic-quality-control>
<https://www.dataone.org/best-practices/communicate-data-quality>
<https://www.dataone.org/best-practices/identify-outliers>
<https://www.dataone.org/best-practices/identify-values-are-estimated>
