# heatstress
Here is my repository with the data and code behind my story on the effect of heat on milk production.  
## Analysis of USDA milk production and NOAA temperature data, 2006 to 2026

This repository contains data, analytic code, and findings. I did not publish the article as my findings did not match my hypothesis. 

## Question

Heat stress, which is measured with the heat index (a combination of temperature and humidity), reduces how much milk cows produce. As heat waves become more frequent and severe with climate change, I wanted to know whether rising summer temperatures were visible in milk production data. I expected to find production falling as temperatures rose.


## Data

This analysis uses three spreadsheets from two sources.

 **USDA National Agricultural Statistics Service (NASS):** (https://quickstats.nass.usda.gov)
  * Arizona milk: Monthly milk production per cow by state since 2006 (state production divided by number of cows) in Arizona https://docs.google.com/spreadsheets/d/110E_P_dDfr7Fj4Uh9zGJzABNGiVzNvpRR6xPYKGbHBk/edit?usp=sharing 
  * New Mexico milk: Monthly milk production per cow by state since 2006 (state production divided by number of cows) in New Mexico
https://docs.google.com/spreadsheets/d/1y6tV4S2syDx13DvyeQ3IQNo-_GnVERLwX8vlKnKxhew/edit?usp=sharing
  * Texas milk : Monthly milk production per cow by state since 2006 (state production divided by number of cows) in Texas
  https://docs.google.com/spreadsheets/d/1AioW9NauQKgSoJgqqfRaWq3KINv6O0LD1pesYUz343A/edit?usp=sharing

* **NOAA National Centers for Environmental Information (NCEI):**
  * `Tab 3 of each csv`: Monthly average temperature by state for the third quarter (July, August and September). 



Each of the spreadsheets contain, among others, the following columns relevant to the analysis:

- `Sum of milk prod Q3` — milk production of the month of July, August and September by each state. 
- `Temperature` — Average temperature of the month of July, August and September by states. 

## Methodology

The notebook [notebook milk production.ipynb] performs the following analyses:

**Part 1: Preparing and combining the data**

* Loads the USDA milk production data for Texas, New Mexico and Arizona, which all showed rising average temperatures over 20 years and are also milk-producing states.
* Uses average temperature rather than maximum temperature, because maximums turned out to be outliers.
* Merges the milk and weather data by state and month.

**Part 2: Isolating summer (Quarter 3)**

* Filters to Q3 (July, August, September), the months with complete data, and compares production and temperature from 2006 to 2026.
* Pivot tables in Google Sheets were used to isolate Q3 and chart the trends. There is one sheet per state:
  * [Arizona heat and milk](https://docs.google.com/spreadsheets/d/110E_P_dDfr7Fj4Uh9zGJzABNGiVzNvpRR6xPYKGbHBk/edit?usp=sharing)
  * [New Mexico heat and milk](https://docs.google.com/spreadsheets/d/1y6tV4S2syDx13DvyeQ3IQNo-_GnVERLwX8vlKnKxhew/edit?usp=sharing)
  * [Texas heat and milk](https://docs.google.com/spreadsheets/d/1AioW9NauQKgSoJgqqfRaWq3KINv6O0LD1pesYUz343A/edit?usp=sharing)


## Findings

In all three states, milk production per cow increased over time even as average summer temperatures also rose. Two Cornell Cooperative Extension researchers suggested two explanations:

1. Demand is growing, driven in part by new processing plants (such as Chobani in Rome, N.Y. and Fairlife), which pushes producers to raise yields.
2. Heat stress is hard to see in state-level aggregate data. It would more likely show up at the scale of an individual farm.

## Limitations and open questions

* State-level averages can hide heat stress that happens on individual farms.
* Average temperature is not the same as the heat index, which also accounts for humidity. This analysis does not include humidity.


## Outputs

The notebook outputs three spreadsheets, which contain the combined milk and temperature data for each state. The links are higher in the README. 


## Running the analysis yourself

You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3
- The Python libraries specified in [`requirements.txt`](requirements.txt)

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). The data file in the output/ directory is available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license. All files in the data/ directory are released into the public domain.



## Feedback / Questions?

Contact Apolline Lamy at apolline.lamy@gmail.com.
