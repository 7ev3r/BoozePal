# BoozePal

## Overview

Goal of this project is to build "BoozePal" (assistant in choosing) and help to pick best whiskey for customer. 
Using Whiskeybase.com for top 1000 rated whiskies and newly released to get : user ratings, user names, and the whiskeys to build BoozePal. Please see below for how our recommender system works.

## Scraper:

//github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/scraper.ipynb

Using Selenium and BeautifulSoup we log in and grab the necessary data through selenium and beautiful soup
- the users
- the ratings provided by the users
- the price from a specific whiskey product webpage
- the url links for each whiskey page
- adding the data to a dataframe and moving to a csv's :

Whiskey_New_Release_Data.csv
Whiskey_Top_1000_Data.csv

## Data clean :

https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/cleaning_data%20.ipynb

- consolidation the datasets and removing NaN values/duplicates , moving to a csv : 

Clean_whiskey_data.csv

- looks good , moving forward

## Running local MySQL server and uploading data from .csv to created DB

https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/XAMMP_mysql_server.jpeg

- checking with MySQL Workbech table content

https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/View%20table%20contents%20in%20Mysql%20workbench.jpeg

- looks good , moving forward

## Creating an API ( not done yet :/ )

- moving forward

## Initial EDA

After consolidation the datasets and removing NaN values/duplicates, checking how the users were rating the whiskies

https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/EDA.ipynb

- final dataframe has 1009 unique users, 463 unique whiskies, and 37567 total reviews

https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/df_screen.jpeg

Most of the users rated the whiskies fairly highly as a majority of reviews range from mid 80's to 100. 
Mostly because whiskies are part of the top 1000 rated whiskies.

https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/Ratings.jpeg

Majority of users having reviewed many different types of whiskies

https://github.com/7ev3r/Midterm_assignment_v2/blob/742bc3a1980443d46c188bf2093d426414c8c162/Images/Users_reviewed.jpeg

img -
img -

## Initial Models
- to be continued

## Conclusion

BoozePal recommends whiskies by user budget after evaluation - 3 whiskies. Throughout the entire process, our system is BoozePal provides URL links to give additional information in case the user decides to get more information about recomendet bottle of whiskey 
