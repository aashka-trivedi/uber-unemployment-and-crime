# uber-unemployment-and-crime

This is the code repository for the course project for CSCI-GA 3033-029 Social Networks taught by Prof. Bud Mishra. In this project we explore the effects of introducing web-app based taxi services on the unemployment rate and the crime rate of that state. 

## Data Files

### Source Data
1. `StateUnemploymentRatesYYYY.csv`  : there are 9 such files holding the statewise unemployment rates from the year 2009-2017. These 
2. `crime_rates_processed_data.csv` : contains the preprocessed crime rate data
3. `Uber-introduction-date.csv`: contains the month and year when uber was introduced in all states. Note that in Florida, Lyft was introduced before Uber, so Lyft's introduction date is used.

### Analyzed Data
1. `unemployment_data.csv`: contains the unemployment rate for each state for the following months:
    1. The month when uber was introduced
    2. 3 months before the introduction of uber
    3. 6 months before the introduction of uber
    4. 12 months before the introduction of uber
    5. 3 months after the introduction of uber
    6. 6 months after the introduction of uber
    7. 3 months after the introduction of uber
    
    Since we only have data from 2009-2017, there are a few states where all of these fields do not exist. In that cse, the values are replaced with the average unemployment rates of the state, for a period of 2 years (1 year before and after the introduction of Uber).
 2. `unemployment_counts.csv`: contains the number of states that had an increase\decrease in the unemployment rate for a period of 3,6, and 12 months befoe and after Uber was introduced. the `Final Calculation` is the adjusted count: here a state is said to have a decrease in the unemployment rates x months after uber was introduced only if it had an increase in unemployment rates x months prior to when uber was introduced.
 3. `crime_data_calculation.csv`: same as above, but for 7 types of crime rates.
 
 ## Code Files
 1. `Unemployment.ipynb`: code to preprocess unemployment data, and generate the unemployment counts.
 2. `Usocial_networks_project_crime_rate_analysis.ipynb`: code to preprocess crime data, and generate the crime counts.
