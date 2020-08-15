# Linear Regression Analysis of Auckland House Prices
Sakyawira Nanda Ruslim, July 2020.

## Executive Summary
The dataset is housing details in Auckland. The 2018 Census population is
downloaded from koordinates.com, the 2018 Deprivation Index is downloaded from
University of Otago’s website. The rest of the data is provided by Microsoft Student
Accelerator. The dataset contains the number of bedrooms, number of bathrooms,
the address, the land area, CV (Capital Value), latitude, longitude,number of
populations in certain ages, population number, and deprivation index. There were
only 3 null values in the 1051 rows dataset. After exploring the data by visualizing the
correlation between each numerical variable, no highly correlated variables are
found. Linear Regression algorithms have been tested for this train dataset and have
a score of 0.167.

## Initial Data Exploration
The initial exploration of the data began with some summary for each attribute’s
minimum, maximum, mean, median, standard deviation, and distinct count. The
results were taken from a cleaned dataset with 1048 entries, as shown here:
<img src="https://github.com/Sakyawira/auckland-house-prices/blob/master/Images/Summary.png?raw=true" width="1000" height="200" />
<img src="https://github.com/Sakyawira/auckland-house-prices/blob/master/Images/summary2.PNG?raw=true" width="1000" height="200" />
It should be noted that some attributes have standard deviations of 3 or more, in
particular: the land area, CV (Capital Value), number of populations in certain ages,
population number, and deprivation index (Score format).

## Correlation and Relationships

The correlation between the numeric columns were calculated and observed in the
below correlation plot. (The right color bar indicated the correlation values. For
example, dark red means correlation value is 1 and light beige means correlation
value is negative 0.25)
<img src="https://github.com/Sakyawira/auckland-house-prices/blob/master/Images/Cor.PNG?raw=true" width="1160" height="824" />
The graph shows that bedrooms number, bathrooms number, land Area, latitude,
and number of population of 50-59 years old have strong positive correlation with
the Capital Value of the houses. On the other hand total number of population,
Deprivation Index, and number of population of 0-49 years old have strong negative
correlation with the Capital Value of the houses.

## Analysis
Three null values were found in the dataset with 1051 entries, therefore dropping the
rows that contain them is considered to have no significant impact in the model
fitting. The Land area attribute has ‘m^2’ concatenated inside the values, therefore
conversion from string to float was done.
Previously there were also attributes such as Address and Suburb but they were
dropped because Linear Regression only works with numerical attributes. Numerical
attributes that represent IDs have also been dropped.
In this analysis, a Linear Regression algorithm was used. These algorithms were
trained with 70% of the data. Testing the model with the remaining 30% of the data
yielded 0.16.

## Conclusion
This analysis has shown that the Capital Value of a house can not be confidently
predicted from the number of bedrooms, number of bathrooms, the land area,
latitude, longitude,number of populations in certain ages, population number, and
deprivation index. In particular, the Linear Regression algorithm only has a score of
16%.
