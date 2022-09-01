# Barcelona Car Accident Analysis
- Final Classification Analysis Project: Python Tableau Files included for each specific machine learning model
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

- In my research, wanted to analyze a dataset that could have an impact on someone's quality of life. MY first task was to assemble the 2 years worth of data. Due to some columns not being available in one, and certain time-date column redundancies, we drop columns which did contain valuable information, but for sake of analysis, we did not include them.
- I first translated each dataset's column names, and changed errors in the age (-1 was a data point, an invalid value for age). We then combined both datasets once each column matched in data types, and then converted those data types that would be better suited as categorical data, such as streetcode for the streets of Barcelona
- We also lightly checked for and replaced null values, such as with age, latitude and longitude. We also quickly checked for duplicates.
- We then dropped a few columns for redudancy, those that have too large number of cateogorical unique values, and other location coordinates: `neighborhood_code`,`month_id`,`neighborhood_code`,`x_coordinate_utm_format`,`y_coordinate_utm_format`
Finnaly, I thought it would be a good moment to practice appending dictionaries with for loops, and apply that to translating the entire dataset. I first attempted to use googletrans, but found it much faster to do it 'by hand', using google translate throught the browser and making a list of translating vehicle names, months, and accident results. 
- After translation, I wanted to take a quick look at 3 columns which contained alot of 'unknown' values, and if the majority of those columns are occupied by unknowns, I thought it best to drop that column. I would later for the exploratory data analysis to make that decision.
- 
### Exploratory Data Analysis
- I made a few visualizations to get a better look at the data. one of them includes a stacked bar chart, which gives us the count of total accidents pertaining to a certain vehicle type, as well as the ration of types of accidents that occured with said vehicle. I also constructed stacked bar graphs with month and time, with each proportition of every accident type show as well. I also developed 2 pie graphs, for the highest half of accident-prone vehicle, and another for the lower half.
- I also constructed some boxplots and made an interesting discovery: Whether it was day of the week, month, or accident type, the medium age of every vicitim was around 40 years old. Another insight was viewed in a density plot, where it is most probable for a woman in her early 20's, while men tend to have a bimodel occurance of early 20's and very early 40s 
-Through visualization, although the `reason for travel pedestrian` is a useful column, over 97% of the data is of the 'unknown', i decided to drop it.  
- As a last drop of data, 'death following 24 hours after the accident' and 'unknown' variables within the column 'accident result', did not produce enough occurances to make SMOTE viable, which I would later discover was necessary for my model. This led me to drop any rows with these specific variables. 
### Normalization/Encoding/Results
 - In my logistic regression model, i used 4 different transformations for my numerical data, with each interation giving me 4 similar scores, for my Normalizer, StandardScaler, MinmaxScaler, and MaxAbsScaler. For my K-nearest neighbors model, it gave me my worse performance, with on average 55% accuracy. My decision tree model and random forest model showed the best promise, which each giving me an accuray of 80% and 89%, respectively. The largest change that helped each model overall was implementing SMOTE. My target was largely unbalanced, thus after implementing SMOTE, the increase in accuracy was very apparent, and I feel I could have done this much sooner.
-
### Conclusion/Areas of improvement/References
Overall, I feel satisfied with my analysis and machine learning model outcomes. I would have liked to have had time to implement a new machine learing model I had never used before, such as Naive Bayes classifier, and I would have liked to implement VIF (Variance Inflation Factor) to take a better look at correlation within my data set. Lastly, gridsearching to hyper tune my parameters would have been essential, unfortunately, due to hardware limitations, I was unable to do so effectively. 
I used various resources to assist in this code, and my teacher, Himanshu Aggarwal, assisted me a great deal. In general, I used stack overflow for various references. Should you have any questions about this project please contact me at mauricio.ruiz93@outlook.com





















