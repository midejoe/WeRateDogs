# WeRateDogs
Analysis of WeRateDogs Twitter page

## Context
WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage.

## Objective
The goal of the this project is to wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. The Twitter archive is great, but it only contains very basic tweet information.


## Dataset
In this project, three datasets was used.

`Enhanced Twitter Archive`

The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything.

`Additional Data via the Twitter API`

Back to the basic-ness of Twitter archives: retweet count and favorite count was extracted using twitter api.

`Image Predictions File`

It comprises of a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).


Project Details
Real-world data rarely comes clean. With the help of Python and its libraries, I had to gather, assess and clean the data, in other for it to be used for analysis and visualization.

The tasks for this project were:

1. Data Wrangling, which consists of:
 Gathering data
 Assessing data
 Cleaning data
2. Storing, analyzing and visualizing the wrangled data.
3. Reporting on data analyses and visualizations.


# Gathering Data for this project
The data for this project was in three different formats as mentioned above.

Twitter Archive File- WeRateDogs: It was extracted programmatically and a twitter_archive_enhanced.csv to use.

Image Predictions File: This file(image_predictions.tsv) was hosted on Udacity's servers and downloaded programmatically using the Requests library.

Twitter API & Tweet JSON File: By using the tweet IDs in the WeRateDogs Twitter archive, I queried the Twitter API for each tweet's JSON data using Python's tweepy library and stored each tweet's set of JSON data in a file tweet_json.txt file.

# Assessing the Data
After gathering the data, three tables were saved and assessed visually and programmatically. The assessments helped to find dirty data with content issues and messy data with structural issues. Both Tidiness and quality issues was sort after.

Visual Assessment provided issues such as the explanability of column names in the image_predictions table. It included columns like p1,p2,etc. Columns like 'doggo', 'floofer', 'pupper', 'puppo' should be a single column in the twitter archive table.

Programmatic Assessment provided the most of quality issues that were present in the three datasets. I separated the issues in two groups, quality and tidiness issues. I applied the technique Define, Code and Test to solve this issues. I also checcked for completeness, validity, accuracy and consistency.

# Cleaning Data for this Project
Clean each of the issues you documented while assessing. Perform this cleaning in wrangle_act.ipynb as well. The result should be a high quality and tidy master pandas DataFrame (or DataFrames, if appropriate).

# Storing, Analyzing, and Visualizing Data for this Project
Store the clean DataFrame(s) in a CSV file with the main one named twitter_archive_master.csv. If additional files exist because multiple tables are required for tidiness, name these files appropriately. Additionally, you may store the cleaned data in a SQLite database.

Analyze and visualize your wrangled data in your wrangle_act.ipynb Jupyter Notebook. At least three (3) insights and one (1) visualization must be produced.
