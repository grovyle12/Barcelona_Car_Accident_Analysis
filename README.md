# Barcelona Car Accident Analysis
- Final Classification Analysis Project: Python Tableau Files included
- In addition, each .xls/.csv files used for each analysis is provided
- For each folder provided, the respective analysis file along with the paired .xls/.csv

### Purpose of Project
- Clean, analyze and present results of analysis of car accidents from Barcelona, Spain, from the years 2020-2021
- Develop the optimum regression model to predict target (price). .ipynb files contains comparison of all possible regression models with Linear Regression and K-Nearest Neighbors.
- Use Tableau to garder further insights, such as using a density map to visualize 

### Problem Definition
-Data: The data set consists of information on some 22,000 car accidents provided by Barcelona's City Hall Open Data Service.  The dataset consisted of people who have been involved in an accident, managed by the Police in the city of Barcelona, whom have suffered some type of injury ( slightly wounded, serious injuries or death). It includes a description of the person (driver, passenger or pedestrian), sex, age, vehicle associated person if the cause was pedestrian as well as the locations of the victim's accident, such as on the crosswalk or sidewalk. (Note: Some features were dropped)

- district code: code of the district
- district name: name of the district (Note: some district are close in proximity to one another, thus 2 district can share the same district code)
- neighborhood name: name of neighborhood
- street code: code for street
- day of week: the day of the week the accident occured
- year: year of accident
- month name: month in which accident occured
- day of month: day of month in which accident occured
- type of shift: shift type responders were on at the time of accident (morning, noon, and night)
- time of day: time of day the accident occured
- desciption of cause by pedestrian: desciption of location of accident by pedestrian
- vehicle type involved: type of vehicle which was the involved in either the pedestrians accident, or the vehicle in use by driver
- gender: gender of victim
- age: age of victims (where victim age is 0, we consider it to be a child under a year old)
- type of person involved: driver, pedestrain, or passenger
- pedestrian hit and run location: location of accident, such as sidewalk or crosswalk
- reason for travel driver: Reason for driver traveling 
- accident result: outlook of victims, which rangers from unharmed to death within 24 hours of accident
- longitude: longitudinal coordinates of accident
- latitude: latitudinal coordinates of accident


### Methodology
- General exploration of data, Feature Extraction, general data cleaning/column dropping, checking for null values
- Exploratory Data Analysis
- Data Transformation/Outlier Removal
- Numerical/Categorical Transformation
- Results
- Tableau Results

### Description of data
- Name of the data: Historic data of houses sold between May 2014 to May 2015, from Seattle, Washington 
- Number of data points: 21,814
- Number of features: 20
- Target attribute: Accident Result

### General data cleaning, translating dataset, exploration of data/visualization 
