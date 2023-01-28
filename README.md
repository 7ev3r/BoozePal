# **BoozePal**
for ![image](https://www.whiskybase.com/images/logos/default@2x.png)
## Overview

Goal of this project is to build "BoozePal" (assistant in choosing) and help to pick best whiskey for user. 
Using [Whiskeybase.com](https://www.whiskybase.com) for [top 1000](https://www.whiskybase.com/whiskies/top1000) rated whiskies and [newly released](https://www.whiskybase.com/whiskies/new-releases) to get : user ratings, user names, and the whiskeys to build BoozePal.

*Please see below for how **BoozePal** works.

## Scraper:

[scraper.ipynb](//github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/scraper.ipynb)

Using Selenium and BeautifulSoup to log in and to grab the necessary data :
- the users
- the ratings provided by the users
- the price from a specific whiskey product webpage
- the url links for each whiskey page

Adding the data to a dataframe and moving to a csv's

Result :
**Whiskey_New_Release_Data.csv**
**Whiskey_Top_1000_Data.csv**

## Data clean :

[cleaning_data .ipynb](https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/cleaning_data%20.ipynb)

Consolidating the datasets and remove NaN values/duplicates , moving to a csv

Result :
**Clean_whiskey_data.csv**

*looks good , moving forward

## Running local MySQL server and uploading data from .csv to created DB

![image](https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/XAMMP_mysql_server.jpeg)

Checking with MySQL Workbech table content

![image](https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/View%20table%20contents%20in%20Mysql%20workbench.jpeg)

*looks good , moving forward

## Creating an API

*not done yet ! sorry

## Initial EDA

After consolidation the datasets and removing NaN values/duplicates, checking how the users were rating the whiskies :

[EDA.ipynb](https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/EDA.ipynb)

*final dataframe has 1009 unique users, 463 unique whiskies, and 37567 total reviews

![image](https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/df_screen.jpeg)

Most of the users rated the whiskies fairly highly as a majority of reviews range from mid 80's to 100. 
*because whiskies are part of the top 1000 rated whiskies.

![image](https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/Ratings.jpeg)

Majority of users reviewed many different types of whiskies

![image](https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/Users_reviewed.jpeg)

![image]()
![image]()

## Initial Models

Using [Google Colab](https://colab.research.google.com/drive/1ePdNEIjuDbF8JMM9RPl9X-yOfEBSdxp0#scrollTo=t7MW5F3WghyP) notebook :

[Train_ML_model.ipynb](https://github.com/7ev3r/Midterm_assignment_v2/blob/d6806a113699a518bcd3b0573d9b4a3cc8263724/Train_ML_model.ipynb)

*somehow cant use Surprise as Python scikit for building and analyzing recommender systems that deal with explicit rating data in VS Code

- Compared different models with Surprise : SVD, KNN_Basic,KNN_Baseline
- Testing the model
- Getting result : notperfect but working BoozePal

Results of all 3 models were close with a RMSE around 1.8 

## Conclusion

- **BoozePal** recommends whiskies by user budget after evaluation.
- **BoozePal** also provides URL links to give additional information , in case the user decides to get more information about recomendet whiskey 
