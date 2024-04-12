# Capstone--Project

## Team Members

-  Mayank Gudadhe
-  Amiya palai 
- Vishal singh sangral
- Richa Rani


# Play store app review analysis
# Introduction

Hey In this project we are going to perform Exploratory Data Analysis , in this we are exploring and analyzing the data to explore the key factor which is responsible for app engagement and success , in this analysis process we use two data set that is given to us one is Play Store Data.csv and second one is User Review.csv, we are gone through both of it and understand what kind of insight we are taken from it in the first csv file we observe that there is 13 columns and 10841 Rows in it but when we deep die into it and understand each columns properly we observe that many of the columns are object Data type but actually the data in this columns are float and int type , before changing its data type we check for duplicate and null value after removing missing and null value we have to change data type of Reviews , Installs , Price , Last Updated columns and hence our Data cleaning , preprocessing of Play Store Data .csv file is analysis ready after cleaning our row count is 9648 rows and columns count is 13 and now the same operations perform with second csv file in this csv file total 5 columns and 64295 rows in this we observe that there is no such issue of data type but there is maximum null values which is common in 3 data type so our task is to remove that so that our data is clean , so in this csv we find null and missing values and analyze them it is really necessary or not , then our cleaning , preprocessing is completed and now our csv file contains 5 columns and 37427 rows in it , now our both csv files are ready now we are going extract useful insights from this datasets , now we are plotting graph whatever insight we are understand we are plotting it on graph so that it is easily understandable.




![Logo](https://techcrunch.com/wp-content/uploads/2022/03/GettyImages-1235737290.jpeg)


## Problem statement
1. Popular Apps category on playstore?

2. Are the vast majority of apps free or paid?

3. How essential is the application rating?

4. What audience segments should the app be based on?

5. Which classification has the most installations?

6. What impact does the most recent update have on the rating?

7. How do ratings change if an app is paid for?

8. Reviews and ratings: How are they connected?

9. Let's talk about the subjectivity of sentiment.

10. Are subjectivity and polarity inversely correlated?

11. What is the review sentiment percentage?

12. How does the polarity of emotion differ between premium and free apps?

13. What impact does content rating have on the app?

14. Does the date of the most recent update affect the rating?

15. what are the most used words for all type of sentiment?![Logo](https://media.licdn.com/dms/image/C4D12AQH3wdBztxsxTw/article-cover_image-shrink_720_1280/0/1607186430192?e=2147483647&v=beta&t=cgKRMvrCmEEQim-np4xn5f7MokY57tgfbolaYm2DLO0)
## Business Objective
Data scientists use exploratory data analysis (EDA) to examine data sets for patterns and abnormalities (outliers), formulate hypotheses based on our understanding of the information, and describe their key characteristics.

Data visualisation techniques are frequently used in exploratory data analysis. In any project involving data analysis or data science, it is a crucial stage.

It assists in deciding how to best modify data sources to obtain the desired results.

In order to better comprehend the data and make it more visually appealing and appealing, EDA entails producing summary statistics for the dataset's numerical data.

The many steps in the EDA process are as follows:

Problem statement: We will discuss and analyse the provided data set. We'll examine the traits it has and attempt to conduct a philosophical examination of their significance for this issue.

Hypothesis:Studying the attributes in the data base will help us establish some fundamental hypotheses that we can use to play around with the data and see what interesting outcomes we can find.

Univariate Analysis: Univariate analysis is the most basic type of data analysis. In order to start, we would choose just one quality and thoroughly examine it. It deals with no co-relation whatsoever, and its primary goal is to describe. Data is taken, summarised, and patterns are discovered within the data.

Bivariate analysis: This type of analysis focuses on causality and the connection between two variables. We shall make an effort to comprehend how qualities are interdependent.

Multivariate Analysis:When more than two variables must be studied at once, multivariate analysis is used.

Data Cleaning:Data cleaning - We'll purge the dataset of errors, outliers, and category variables.

Testing Hypothesis: We will determine whether our data complies with the presumptions needed by the majority of multivariate procedures.
![Logo](https://cloudfront-us-east-1.images.arcpublishing.com/coindesk/OIVY4TP3IRC7LP3G4RF3KHX5UU.jpg)
## After Dataset first view What we know about dataset
1. After reviewing the data set I saw that there are 10841 rows and 13 columns in the play store Data.csv file.

2. Many of the columns in that dataset doesn't have the right data types,the price column has the type 'object' but the column element in that column is numeric type so we have to change that type to int or float. Similarly, there is some column which does not have the right type so we have to change them.

3. After checking the duplicate value we saw that the total no of rows come out is 10358 which means we have many duplicate rows in the dataset.

4. After counting the null/missing value and visualizing the data we saw that there are 5 columns consist null values that are 'Rating', 'Type', ' Content Rating', 'Current ver' and ' Android ver'. Among these 5 column Rating column have the highest number of null values and Type and Content Rating column have the less number of null values.

5. In the case of the User Reviews dataset, we saw there are 64295 numbers of rows and 5 columns in the dataset.

6. The type of all the variables is in the correct form so no need to change that.

7. In the whole data set, there are 30679 non-duplicated rows present which means there are so many duplicate rows present in the dataset, and also after counting the null value and visualizing the dataset, we found that every column have numbers of null values except the 'app' column, if we calculate the percentage then it's almost 42% of the total rows present in every column

## After understanding variable
![Logo](https://outlookmoney.com/public/uploads/story/c10f34539618b11a5d9e9eeedc18f70d.jpg)
Variable description of DF1
There are total 13 variable:-

1. App:- Name of the applicatons.

2. Category:- Apps that comes under which category that is given in this columns.

3. Rating:- Rating of the app between 1-5.

4. Reviews:-Number of app reviewed.

5. Size:- Size of the app many times it varies with device.

6. Installs:- Number of installs of the app.

7. Type:- The app is paid or free type.

8. Price:- How much price you have to pay for paid apps.

9. Content rating:- App content is available for Everyone or Teen or other.

10. Genres:- App is belong to which genres wheather it is belong to Art&Design or other genres. 11.Last Updated:- When the app is lastly updated.

12. Current Ver:- App current ver various times it varies with device.

13. Android Ver:- Perticular app supported in which android version.

Variable description of DF2
1. App:- App content App name.

2. Translated_Review:- It content review about App

3. Sentiment:- Sentiment related to what the emotions users provide while using the app weather it is positive , negative or neutral.

4. Sentiment_Polarity:- Sentiment_Polarity refers to the strength of users opinion weather it is strongly positive or negative , polarity lies the range between [-1,1]

5. Sentiment_Subjectivity:-Sentiment_Subjectivity lies between the range of [0,1],it is a users personal opinion , judgment it belongs to users which they personally involve in this object.
## Facts that we understand till the point
1. After calling the nunique() method which gives us the number of unique values present in a particular column, we found that there is a total of 9660 unique apps present in the data frame and it is divided into 40 unique categories .

2. There is 3 type of unique values present in the 'Type' columnn but we know that there is only 2 type of apps we use that is paid or free but we have a extra value present in the type columns , so we have to replace or remove that one.

3. After checking the unique values in the 'Size' column we found that all the value contain 'M' and 'K' in it (M for MB and K for KB) and also contain a unique value named 'varies with device', so in the data cleaning section we have to remove that 'M' and 'K' and convert all the values in MB form and there is no need to change the 'varies with device' value.

4. Like 'Size' column 'Install' column has '+'and ',' symbol in it and also the 'Price' column has Dollar symbol in it, so for changing the dtype we have to remove the '+' and ',' symbolfrom Installs Column and '$' symbol from 'Price 'Column

5. In content rating, there are 6 unique values and null values

6. In the case of the user review data set, there is a total of 1074 unique apps .that means a lot of people give their opinion about these apps only so we can say a lot of people use these apps, and there are 3 types of sentiments that are positive, negative and neutral.
## Manipulations that we have done and insights that we have found
![Logo](https://uploads-ssl.webflow.com/60e3caa50ec2a701bbf83598/61403461d84400840af96cb6_60c0475cd317d3690406ad29_5dddf71006fb58ed20d46b05_3.jpeg)
For Play Store Data
1. So in this data wrangling section at first we clean and do some changes in the play store dataset and after that we do the same with user review dataset.

2. In the case of the play store Dataset,first we deal with the null values present in every column.

3. In the previous, we use the isnull() and sum() method to know exactly how many null values present in every column and we found that there is only 1 null value present in both 'Type' and 'Content Rating' column,8 null values present in the 'Current Ver' column,3 null value is in the 'Android Ver' column and the highest no of null values (that is 1474) are in the 'Rating' column.

4. Firstly we deal with the columns having a lesser number of null values that is 'Type' and 'Content Rating', so in the Type column we saw that there is 3 unique values (that is free, paid, and 0), there are 10039 numbers of 'Free' type,800 number 'Paid' type and only one '0' type but we know that zero is not a type and if we analyze that column only, then we also saw that in the same row, the 'Rating' column has '19.0' as a value, and we know that is not the right value that means this row is an outlier and also both 'Content Rating' and 'Android Ver' have null values so we have to remove this row permanently.

5. So for the type column, the null value will replace with the value 'Free' cause the most number of apps are 'Free' type.

6. After the 'Type' column, we have to deal with the Android ver column, and as we know previously that there are only 3 null values present in the Android Ver column.

7. After deeply analyzing that column we find that we can't replace the null values with the mean or median, and also the outlier row which we find when we analyze the 'Type' column also present there so we have to remove all these 3 columns from the dataset. 8. we use the pandas drop() method for removing these columns and set 'iplace=True' for permanent changes in the data frame.

9. Now if we call isnull() and sum() methods we can see that only the 'Rating' and 'Current Ver' columns have null values. now we have to deal with these 2 columns.

10. In the case of the 'Current Ver' column we have to remove all the rows containing null values cause like the 'Android Ver' column we can't replace the null value of 'Current Ver' with the mean or median.

11. After dropping all null values we have only one column which contains the null values that are in The 'Rating' column. As we can see there are 1470 numbers of null values in this column, so we can't just remove these rows cause it's a very huge amount of data. so we have to replace these data with the mean of the column. 12. Without including NaN values, the mean of 'Ratings' column is calculated to be 4.2.

13. The median of the items in the "Rating" column is 4.3. This indicates that 50% of the apps have an average rating above 4.3 and the remaining 50% have a rating below 4.3.

15. The ratings are left biassed, as seen in the distplot representations. We are aware that if a variable is skewed, the values at the extreme ends of the distribution will affect the mean. As a result, the median provides a more accurate depiction of the vast majority of values in the variable.

16. So, we will use its median to impute the NaN values in the Rating column.

17. For finding the median of the column we use the median() function with nonnull values of that column.After finding the median we replace all the null values with the median.

18. After these operations we can see there is no null value present in the data frame and we got 10830 rows and 13 columns.

19. After null values, we have to work on the dtype of all columns, so as we have seen previously that there are some columns (like Reviews, Size, Installs, Price, and Last updated) which needs some changes.

20. Firstly for the 'Reviews' column, we know that it contains numeric type data so we have to change the dtype of this column .for changing dtype we use astype() method.

21. After the 'Reviews' column, we find that the 'Size' column consists of data in mb and kb format (m for mb and k for kb) so we have to remove the 'm' and 'k' sign from the data and convert the data to mb if it is in kb. for that we write a function that takes the data of the 'Size' column as an argument and returns the data without 'm' and 'k' signs.

22. After writing the function we pass the 'Size' column inside the lambda function with the help of apply() method and stored the new value in place of old values.

23. After this operation, if we call the head() method and we can see that the 'Size' column contains the new value without 'm' and 'k' sign and all the kb data is converted into mb.

24. Like size column 'Install' column have some special symbols like '+' and ',', so for removing that symbol and converting the dtype we write a function named replace which takes the data of the 'Install' column as an argument and returns the same data without '+' and ',' symbol and int type. like 'Size', we pass the 'Install' column inside the lambda function using apply() method and got the column updated .

25. Now if we call the info() method we can see that the values in the 'Install' column got updated and the dtype is also changed.

26. After the 'Size' and 'Install' column it's time for the 'Price' column, so for the 'Price' column ,first we check how many rows there ,which have some price, and then we found that there is 797 row that has some price, not 0, and also one more thing we found that all these data contain a Dollar symbol in it so we have to remove the Dollar symbol for changing the dtype. for that, we write a function named 'remove_dollar' which takes the values of the 'Price' column as an argument and return the same value with float type and without '$' symbol.

27. Like 'Size' and 'Install' we use apply () method and lambda function to do this operation.

28. At last, We changed the type of the 'Last Updated' column from object to datetime by using datetime.strptime () function inside the lambda function and use apply() method on it.

29. Now if we call the info() method then we can see that all the columns mention above is updated with its dtype and values

For User Review Data
1. In the case of the user review data set, we know that there are many null values present in every column except the 'App' column.

2. After checking the null values we saw that if the 'Translated_Review' column has a null value then the 'Sentiment', 'Sentiment_Polarity' and 'Sentiment_subjectivity' columns also have null values

3. This happens because of the unavailability of reviews, If a person did not give any review then it's impossible to find the 'Sentiment', 'Sentiment_polarity' and 'Sentiment_subjectivity', but we found some exception data in the data frame which didn't follow this rule so we have to delete all the rows consist null values because we don't want that rows which didn't have any review.

4. After deletingthe null values there are only 37427 data present in our data frame.
## After all visualizations Solution to Business Objective
We have worked on a number of metrics as part of this study to analyse play store applications that would helps the client launch their apps successfully.
![Logo](https://www.zuken.com/en/wp-content/uploads/sites/2/2018/10/team-celebrating-high-five-1510x731.jpg)
- In order to give them the best results from our study, we concentrated more on the issue descriptions and data cleaning in the initial phase.

- The Client has to concentrate more on:

- Creating applications for the least-explored categories. like things like beauty.

- As the majority of applications are free, emphasising free apps is more crucial.

- In order to achieve the largest install rates, you should concentrate more on content that is accessible to everyone.

- Companies should concentrate on continuously updating their apps to attract new users.

- They should pay greater attention to the wants and features of the user because the user's feelings will change as they use the app.

- The most competitive category is family, while the category with the highest average app installs is games. The percentage of free apps is 92%, and the percentage of no age-restricted apps is 82%.

- With 1906, 926, and 829 apps respectively, the top three categories are family, games, and tools.

- The leading genres are tools, entertainment, education, business, and medicine.

- There are 8783 apps that are under 50 MB in size. Both types of apps are included in the 7749 apps with ratings greater than 4.0.

- Almost a billion people have downloaded a specipic 20 free applications.

- The only paid app with more than 10M installations is Minecraft. Also, this app has generated the most money only from the installation price. The category with the highest average installation cost for paid apps is: lifestyle

- The average app size in the Google Play store is 12 MB. The apps with the highest average number of installs are those whose size varies by device.

- The largest number of average user ratings are found in apps larger than 90 MB, indicating that they are much more popular than the others.

- The game with the most good reviews is Helix Jump, whereas the game with the most negative reviews is Angry Birds Classic.

- The combined dataset's overall sentiment score is 64% positive, 22% negative, and 13% neutral.
## Conclusion 
1. First of all Data cleaning was one of our biggest challenges.

2. 13.60% of the reviews had NaN values, and even after combining the two dataframes, we were unable to make any significant deductions to fill them. So we had to abandon them.

3. There were only 816 common apps in the combined data frame from the Play Store and user evaluations. We could have provided a more insightful analysis if we had at least 70% to 80% of the cleaned data available in the merged dataframes, which is only 10% of the total data.

4. The User Reviews column had 13.60% NaN values, which may have been filled by using the 42% NaN values to better grasp the attitudes within each category.

5. There is so much more to learn about. As an example, we have the current version and the Android version available, which can be investigated in greater detail and lead to additional analysis where we can explain how these things affect and need to be considered when designing apps for users.

6. We can investigate the impact of the app's size and Android version on the quantity of installs.

7. By creating models that can help us interpret even better, machine learning can assist us in deploying more insights. Although this is something we can work on, we have left it for later.
