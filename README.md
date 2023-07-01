# Retails-Sales-Pridiction-
Abstract:

Sales forecasting is the process of estimating the demand for a product or its sales over a specific period of time. Sales forecasts are used by businesses to determine the revenue they can generate in a given timespan, which empowers them to develop powerful and strategic business plans. Important business decisions such as budgets, hiring, incentives, goals, acquisitions, and other growth plans depend on the revenue the company is projected to generate in the coming months. Therefore, it is crucial for sales forecasts to be accurate to ensure that these plans are effective. It is important to note that sales forecasts are different from sales goals. Sales goals refer to what a company desires to achieve in order to execute their future business plans, whereas sales forecasts predict what is likely to happen based on past records, data, trends, and improvement measures.
This study aims to predict the sales of a drug store chain in the European market for a six-week time period using various machine learning algorithms. The results of 


these algorithms, including EDA, correlation, decision tree, random forest, regression, and forecasting, will be compared to determine the best method for sales prediction.

Keywords: EDA, Correlation, Decision Tree Random Forest, Regression, Forecasting

Problem Statement:
Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. 


Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied. You are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

Introduction: 
The demand for a product is not static and can fluctuate over time. In order to achieve financial growth, it's imperative for businesses to accurately assess customer interest and anticipate future demand. Sales forecasting is the process of predicting the sales or demand of a particular product over a specific period of time. In order to create an accurate sales forecast, it's crucial to have a reliable dataset. Past sales records, trends, and patterns observed for a particular store are essential factors in creating a sales forecast. Variations in demand can be caused by multiple factors. Companies regularly undertake sales forecasts to improve their business plans and strategies.
Sales forecasting models play a crucial role in a company's decision-making process, growth strategies, and plans. The goal of this project is to create machine learning models to predict the sales of 1115 drug stores across the European market and compare their performance. Additionally, the project aims to identify the features that contribute to higher sales and those that lead to lower sales, which will inform future improvement plans. Through this Retail Sales Prediction project, the team will analyze the contributing factors of sales performance and explore opportunities for growth.
Approach:
To ensure the quality of the data, the approach adopted involves checking the integrity of the data and understanding the features involved. The following steps were carried out:
● Understanding the business problem and the datasets.
● Data cleaning and preprocessing, which involved identifying and handling null values by imputing them with appropriate values. Categorical values were converted to appropriate data types, and the provided datasets were merged to obtain a final dataset for analysis.
● Exploratory data analysis, which included analyzing the categorical and continuous variables against the target variable.
● Data manipulation, which involved feature selection and engineering, feature scaling, outlier detection and treatment, and encoding categorical features.
● Modeling, where a decision tree was chosen as the baseline model, considering that the features were mostly categorical, with only a few having continuous importance.
● Model Performance and Evaluation:

After building the machine learning models for sales forecasting, their performance was evaluated on the basis of several metrics such as Mean Absolute Error (MAE), Root Mean Square Error (RMSE), and R-squared (R2) score. The models were also compared with each other to find the best performing model. The evaluation results showed that the Random Forest regression model outperformed other models with the lowest MAE and RMSE values and the highest R2 score.

●Store-wise Sales Predictions:

Using the best performing Random Forest model, sales predictions were made for 1115 drug stores across the European market for the next six weeks. These predictions helped the company to make informed decisions regarding inventory management, sales strategies, and revenue forecasting.

● Conclusion and Recommendations:

In conclusion, sales forecasting plays a vital role in the growth and success of a business. Machine learning algorithms provide a powerful tool to accurately forecast sales and help companies to make informed decisions. In this project, we successfully built and evaluated machine learning models for sales forecasting, with the Random Forest model performing the best. The predictions made by the model can be used by the company to improve its inventory management, marketing strategies, and revenue forecasting.

Based on the findings, we recommend that the company should invest in improving its dataset and collecting more relevant data to further improve the accuracy of the sales forecasting models. It is also important to regularly update the models and adapt to changes in customer demand and market trends to ensure continued success.


Understanding the Data
The initial step in data analysis involves understanding the data by answering some basic questions such as the type of data, the number of rows or observations, the number of features, the data types, and whether there are any missing values. In this case, the dataset comprises two csv files. The first file contains historical data, consisting of 1017209 rows or observations and 9 columns with no null values. The second file contains supplementary information about the stores, with 1115 rows and 10 columns, but with several missing values in some columns. The data types present in the dataset are integer, float, and object.

Let’s define the features involved: 
● Id - an Id that represents a (Store, Date) duple within the set 
● Store - a unique Id for each store 
● Sales - the turnover for any given day (Dependent Variable) 
● Customers - the number of customers on a given day
● Open - an indicator for whether the store was open: 0 = closed, 1 = open 
● StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
● SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools
 ● StoreType - differentiates between 4 different store models: a, b, c, d 
● Assortment - describes an assortment level: a = basic, b = extra, c = extended. An assortment strategy in retailing involves the number and type of products that stores display for purchase by consumers. 
● CompetitionDistance - distance in meters to the nearest competitor store 
● CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened 
● Promo - indicates whether a store is running a promo on that day 
● Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
 ● Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
 ● PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store
Data Cleaning and Preprocessing:
Handling missing values is an important skill in the data analysis process. If there are very few missing values compared to the size of the dataset, we may choose to drop rows that have missing values. Otherwise, it is better to replace them with appropriate values. It is necessary to check and handle these values before feeding it to the models, so as to obtain good insights on what the data is trying to say and make great characterisation and predictions which will in turn help improve the business's growth. The historical records dataset had no null value
 

The dataset had a lot of nulls in the following columns: 


● CompetitionOpenSinceMonth 
● CompetitionOpenSinceYear 
● Promo2SinceWeek
 ● Promo2SinceYear
 ● PromoInterval






● ‘CompetitionDistance’ - Competition Distance is the distance in meters to the nearest competitor store. The Competition Distance distribution plot shows the distances at which generally the stores are opened
