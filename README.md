# Video-Game-Sales-Analysis
This project composes of 5 main subsections. Data Preperation, Attribute Analysis, Trend Plotting, Statistical Analysis, and Machine Learning Models.

In the Data Preperation section, some background information had to be researched. Specifically, when the data was obtained, as this would be required during a future forecasting section in the project. The data was web-scrapped off of a website sometime in the middle of 2016, thus only about half a year of data existed for that year. The forecasting would not be accurate if it was working off of half a year of data, thus it was excluded from the dataset and further analysis. Furthermore, null values and duplicate values were removed.

Summary of Data Preperation:
1. Dataset had null values in the 'Year' and 'Publisher' columns (271 and 58 respectively)
2. The null values were removed and the dataframe was renamed to vg (video games)
3. The 'Year' attribute datatype was changed from float to integer
4. Data after the year '2015' was removed

---

In the Attribute Analysis, multiple univariate analyses and multivariate analyses were performed. In the Univariate Analysis section, the unique values in singular attributes will be studied and analyzed. An example of this analysis would be determining which Genre of game has the most title releases. In the Multivariate Analysis section, 2 or more attributes will be paired together and an analysis between both columns will be done. An example of this is where the Genre and Global Sales columns are paired and we can see which game genres generated the most revenue over the years.

Summary of Attribute Analysis:
1. Most of the games in the dataset fall under the "Action" and "Sports" genres.
2. Most of the games in the dataset were published by the Electronic Arts (EA) and Activision companies.
3. Most of the games were released on the Nintendo DS and Playstation 2 Consoles.
4. Need for Speed: Most Wanted was released on the most platforms. NOTE: Two completely different versions of the game exist, but under the same name.
5. Most of the game titles were released in the year 2009, followed by 2008.
6. The most profitable game title was Wii Sports.

---

In the Trend Plotting section, the following lineplots will be set up to show trends relating to different aspects of the dataset. An example of one of the line plots would be how sales in different regions varied for the Nintendo brand. Trends that were analyzed include Sales by Top Publishers, Sales by Top Genres, and Sales by Various Console Families through multiple generations.

Summary of Trend Plotting:
1. The general trend that can be seen is that when a newer generation console is released, the previous console's title sales see a decline, while the newer generation console's title sales increase.
2. Each generation of the console, regardless of console family, sees a peak in their sales during a certain time prior to title sales declining. The newer generation consoles are always released once the previous generation sees a considerable decline in sales.

---

Statistical tests will be utilized to determine if the below factors contributed to statistically proving if global sales were different, or not different from each other. The null hypothesis, H0, will be that the factors are not statistically different, while H1 is that they are statistically different. An alpha value of 0.05 will be utilized. The SciPy library will be generally utilized in this section to undergo the statistical tests. Features were engineered to better define possible factors affecting global sales of video games.

The questions that were answered in this section are:
Are global sales statistically different across platform groups?
Are global sales statistically different across different decades?

Two new attibutes, PlatformGroup and DecadeGroup were engineered and added as attributes to the dataframe (and utilized in later model creations).

Summary of Statistical Tests:
Observations:
1. Amongst the three platform giants, the sales were generally the same. Although Nintendo had started its reign in the industry far before Playstation and XBox, the sales amongst these platforms were statistically the same.
2. The 1980's generally saw the most profits amongst video game sales. This was interesting as I hypothesized that with inflation in later years, along with the release of multiple new games, that the newer generation games would have had more sales. The 80's admittedly had more iconic games that withstood the test of time. As a result, the sales amongst each decades were statistically different.

---

In the Machine Learning Models section, multiple regression models were created in order to predict a dependant variable, Global_Sales. Some issues had arisen simply due to the nature of the dataset. The Global_Sales attribute could easily be predicted by the model by simply summing up the NA Sales, EU Sales, JP Sales, and Other Country Sales, thus the following question was formed. Can we accurately predict the global sales for each game by only utilizing the sales data of a single region?

As a result, every attribute in the dataset was fed into the model, excluding EU Sales, JP Sales, and Other Country Sales. The attributes were fed into their respective feature transformation pipelines respective of their data types (numerical and categorical).

Summary of Machine Learning Models:

 Ridge() 
 Model Accuracy: 86.26%

 Lasso() 
 Model Accuracy: -0.04%

 KNeighborsRegressor() 
 Model Accuracy: 46.12%

 RandomForestRegressor() 
 Model Accuracy: 91.32%

 DecisionTreeRegressor() 
 Model Accuracy: 85.02%

 AdaBoostRegressor() 
 Model Accuracy: -17.79%

 GradientBoostingRegressor() 
 Model Accuracy: 2.28%

The Random Forest Regression model output the most accurate predictions for this dataset.

---

In a later version of this project, the models could be further improved by implementing hypertuning and looking into further engineering of attributes. Forecasting can also be done to predict future sales for future global sales.




