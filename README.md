# Evaluating-snapchat-political-ads
Mini Project #2

Dataset Background: The data set I chose was the 2020 snapchat political advertisements library. I chose to analyze this data because I was interested in how political campaigns target my age demographic, and how different factors contirubted to the success of these advertising campaigns.
Data Anlysis: I performed this analysis by manipulating the data set to extract the independant variable values for the number of dollars (in USD) spent on an ad, and the number of days the ad ran. I then performed a single regression analysis for each of these independent variables, and a multiple regression analysis for both variables. 
Findings: I found that neither variable had a strong correlation with the number of impressions, especially the number of days run. This means that advertisers should not rely on the number of dollars spent or the length of the run to ensure a high number of impressions. In pursuing this matter further, I believe it may be helpful to research information on other factors that go into digital media advertising. For example, advertising on certain stories or channels on snapchat's platform may result in vastly different numbers of impressions. 

Data Vizualizations:
![](Screen%Shot%2020-02-28%at%11.34.20%AM.png)
![](Screen%Shot%2020-02-28%at%11.34.29%AM.png)

Business Question: What independent factors contribute the most to the success of a snpachat political advertisement?
Data Question: What is the correlation between number of dollars spent/number of days run and number of impressions for a snapchat political advertisement?
Data Answer: Both independant variables had poor regression model outputs. Run length was determined to be a non-significant variable, and the number of dollars spent variable showed low R^2 and high standard error of regression.
Business Answer: Neither number of dollars nor number of days had a high correlation with the number of impressions. We must do more research into other metrics that may determine the amount of people who view a snapchat advertisement.

Snapchat Political Ads Data Set:https://github.com/Miya-herman/Evaluating-snapchat-political-ads/blob/master/PoliticalAds.csv
Political Ads Analysis: https://github.com/Miya-herman/Evaluating-snapchat-political-ads/blob/master/Analysis_of_political_ads.xls

Step by Step:
Maipulating the data:
1) I added filters to the country code column so that I could narrow down the data to only advertisements in the U.S.
2) In order to determine the amount of days each advertisement ran, I had to subtract the StartDate column from EndDate. However, the date cells included time values, which prevented me from performing this operation initially. I had to create two new colums which held the correctly formatted dates without the time values, which I did by using the =Left command and only selecting the yyyy/mm/dd characters. 
3) I was then able to subtract the dates using =DATEDIF to create the run_length column
Single Linear Regression:
4) I copied Spend and Impressions into a new sheet, and inserted a scatterplot of the data
5) I then inserted a trendline, and formatted it to make it more visible against the data. I inserted the R^2 value and trendline equation onto the chart
6) I repeated steps 4-5 using run_length and Impressions
Multiple Linear Regression:
7) When I attempted to perform a regression data analysis of both independent variables, I was getting an error that reported the fields contained non-numeric values. I ensured there were no blanks or text fields in either column, but the error persisted. I was able to resolve this error by copying each desired column (Impressions, run_length, and Spend) into a new sheet, which then allowed me to perform the regression analysis
8) I clicked on the data analysis tool box, selected regression, and input Impression for the y-value, and run_length and Spend in the x-value box. I then ran the regression and the outputs appeared in a new sheet.
9) After performing the regression, the P-value for the run-length variable was .1, which is higher than the significance benchmark of .05. In other cases, I would delete this variable and run the regression again. However, since this was the only other variable besides Spend, I decided to keep the variable in and simply note that it would impact the effectiveness of the regression model. 
