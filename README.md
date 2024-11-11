This project involves an in-depth analysis of YouTube data to uncover insights about viewer sentiment, emoji usage, engagement levels, and trending categories. By applying various analytical techniques and visualizing the results, this project sheds light on audience behavior and content trends on the platform

Project Overview
This YouTube Data Analysis project is designed to analyze YouTube comment data to determine:

* Viewer sentiment towards specific videos
* Emoji usage and frequency
* Word cloud analysis to identify frequently discussed topics
* Popular and trending video categories
* Engagement levels to assess if audiences are actively interacting with content


Pandas - 1d structure - array/list. 2d structure - dataframe
	
Why do you add r in pd.read_csv():
You convert it to raw string and python reads it as such

Extracting data:



	

Transform data in acceptable form:
Check if we having any missing value or not:


The value is not a missing value, if true then its missing. 

Sum of missing values:

	

If there are few missing values we can drop it:



The inplace = True will ensure that that file will be the original and is so memory efficient 


Perform sentiment analsyis:

Analysing the sentiment of the user.
User1 -> videos are quite helpful 
User2 -> I am unable to understand concept
[-1->0->1]

User1 ->1
User1 ->-1

Polarity[-1,1]

Use textblob


This is returning 0 so the phrase is neutral. 

Use for loop to iterate through the comments and use a try except block:

Fetch a sample to save time



Adding a new column for polarity:

	
Wordcloud analysis:
Graphical representation of text frequency of most important keyword. 
Positive keyword = positive polarity keyword.

This is a filter:





Stopwords = meaningless words so exclude them


Stopwords in the package:




Convert the series which is this:



Into a string:



Generating a positive wordcloud:






Generating a negative wordcloud:



Emoji analysis:

Use list comprehenstion



Counts of the emoji:



Plot it using bar chart:
Using the list comprehension 





Collect entire data of YouTube:

Listing current directory:



Only choosing the csv files in that directory:




Ignore warnings:


Create a big data frame to add in the csv files on mac:



Check if any instances are duplicated:



Filter to see how many are duplicated:




Duplicates are defaulted to first. If you want to remove all the duplicates, you can use duplicate = False



Export the above data to csv and json:



Exporting in the database, you have to create an engine:



Analysing the most liked category:

Unique category Id:









Removing bad data:

Create a box plot:





Target audience is engaged or not:

Metrics to consider:
Like rate, Dislike rate, comment count ratio to views

Make these columns:




Boxplot 





View multiple columns:



Seeing correlation:


Heatmap:




Which channels have the largest number of trending videos.

Following will return a frequency counts:



Can also achieve the above using group by function:



Reset the index to get a dataframe:




Rename the column:




Creating a bar chart:




Does punctuations have an impact on the views, likes and the dislikes?
Import new package:



Use the len function:








The above shows the like rate.



The below shows the likes:





![image](https://github.com/user-attachments/assets/d586e9f2-cce1-4554-877d-e8e6b2b749ba)


