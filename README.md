# -WebScraping_HousePricePrediction

We captured the information of houses in 12 different cities in Turkey. We had to write a working bot to pull this data from a site that is prohibited from extracting data. However, we cannot share this bot due to privacy.

There are 6895 unedited data in this data set. As housing information; price, city, district, announcement date, property type, square meter information, number of rooms, building age, etc.

When we examine the data set, it can be observed that there are a few errors due to the changes seen in the advertisements during data extraction. Because this is a data set obtained from real advertisements. That's why we first take a look at the contents of the variables one by one.

![image](https://user-images.githubusercontent.com/58051004/147223667-812baa56-77e9-4de0-a208-2d0f67e521e2.png)

We then observe this dataset using some of the appropriate visualization techniques. Then we move on to the process of cleaning the outliers seen here. After we clear these outliers, we create a few more variables by Feature Engineering.

After going through these processes, we now insert the data set into the machine learning model. We introduce categorical variables into the model by trying 2 different methods. We use LabelEncoder as the first method, and then we look at the default results by inserting it into 10 different models. Then we try to get the best result by putting 3 different models that give the best results into the tune process. After this process, the model that gives the best test data result is CatBoost with 72.5%.

However, after these results, we try to use GetDummies on categorical variables this time, and we see that the model that gives the best result is CatBoost with 74.7% by applying the tune process to the top 3 models as a result.

As a result of these modeling processes, we decide that the CatBoost model produced using GetDummies gives the best result with 74.7%. This result is not high enough, but in such an unedited house price dataset, this is the best result.
