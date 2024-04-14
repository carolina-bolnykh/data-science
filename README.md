Link to File 1: https://www.kaggle.com/datasets/victorsoeiro/netflix-tv-shows-and-movies/data?select=titles.csv 

Dataset 1 Description: 
The dataset titles.csv found on Kaggle contains around 5 thousand unique titles on Netflix with 15 columns containing their information, including movie id, title, show type, description, release year, genre, imbd score, imbd votes, tmbd score, and tmbd popularity. 

Link to File 2:
https://www.kaggle.com/datasets/victorsoeiro/netflix-tv-shows-and-movies/data?select=credits.csv 

Dataset 2 Description: 
The credits.csv dataset contains almost 78 thousand records detailing actors and directors for TV shows and movies on Netflix. The dataset also states which character each actor played in the movies or TV shows they acted in.

Summary of current understanding of the data-wrangling/data-merging issues: 
In order to meaningfully merge the above 2 datasets, the key feature that we will merge on will be the Movie or Show ID column for titles.csv and the Title ID for the credits.csv. This column contains the unique ID for the TV show or movie on JustWatch. We will also continue to use this column as the unique ID column since the other columns contain repeats. A data merging issue we have is that each row in the credits.csv data set is an actor, and we want each row of our analysis dataset (and each row in titles.csv) to be for movies. We will group by Title ID and create a list of actors and directors per movie. Other than that issue, since there are no missing values for the movie id attribute in either dataset, there should be no challenges when merging.

In terms of the analysis part of our project, we aim to analyze movie ratings in respect to the other attributes (actors, directors, description, runtime) to detect clusters and relative importance. We hope to answer questions such as: “Does the presence of XYZ actor tend to give their movies a higher overall average rating?”, “Does runtime or genre affect the IMDB rating more?” and “What are the similarities in actors and age certification in the highest performing cluster of movies?”. This will inform our data cleaning and wrangling decisions in these ways. 
Cleaning: If the IMDB rating, the TMDB popularity, and the TMDB score, we will drop the row, as we are using these attributes to measure popularity
Wrangling: We will be dropping some columns from titles.csv that are extraneous, like IMDB votes or IMDB ID (since we already have a unique ID variable). 
Wrangling: We may derive attributes from the credits.csv dataset such as the number of directors that worked on a project (Is multiple directors working on a project correlated with a higher rating?)


to-do:
1.) feature engineering for movies
2.) fix training/testing split for movies
3.) feature engineering for shows