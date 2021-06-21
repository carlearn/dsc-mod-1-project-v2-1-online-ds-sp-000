# Module 1 Final Project - Movie Industry Analysis

For: Microsoft Inc. June 2021

By: Carrie Liu



## Overview

Most big companies are creating original video contents recently. Microsoft wants to launch a new movie studio and join the game of making movies. Our team is charged with data analysis on the movie industry. The review period is 2010 - 2019, a decade pre-pandemic. 



## Objectives

* What types of films are doing best at the box office?
* When is the best time to release films?
* Who are the directors and actors to consider for the new film?
* What are the challenges the new studio will face?



## Approach

1. Datasource: 

First, we will use TMDb API to retrieve movie details data including: 'id', 'imdb_id', 'original_title', 'title', 'genres', 'release_date', 'budget', 'revenue', 'popularity', 'vote_average', 'vote_count', and 'runtime'. Next, we will join the IMDb datasets provided to get the crew (including directors and actors) details.


2. Clean the Data: 
* check whether there's any missing data and duplicates
* convert dtypes
* split the column of 'genres' to get respective movie category
* convert money values into million: including columns 'revenue' and 'budget'
* create a new column 'profit'

3. Exploratory Data Analysis:
* use groupby function to get the relationship between genres and profits / popularity
* use groupby function to analyze the seasonality of respective movie genres
* use merge to join TMDb and IMDb data frames
* use matplotlib and seaborn to visualize the data

4. Summarize the recommendations, challenges and next steps



## Table of Contents

1. Readme: 

    * [README.md](https://github.com/carlearn/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/README.md)
    

2. Jupyter Notebook: 

    * [student.ipynb](https://github.com/carlearn/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/student.ipynb): 
    
    The complete code include importing data, cleaning data, exploratory data analysis, data visualization and summary.
    
    * [dataset test.ipynb](https://github.com/carlearn/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/dataset_test.ipynb): 
    
    Import the datasets provided including: Box Office Mojo, IMDb, Rotten Tomatoes, TheMovieDB.org, and The Numbers. However, there’s a problem with joining datasets from multiple sources, as formats are almost never standardized across the sources. The best solution is to use API to find out whether there’s a unique key that we can join on. Please refer to the blog below for detailed analysis on how to find the right datasets.
    
    
3. Presentation:

    * [Presentation slides](https://github.com/carlearn/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/Presentation.key)
    
    * [Presentation record]


4. Blog: 

    * [Movie Industry Analysis](https://carlearn.github.io/movie_industry_analysis)
    
    This blog is a fomratted summary of movie industry analysis (i.e. Module 1 project summary).
    
    * [How to Find the Datasets for Movie Analysis](https://carlearn.github.io/how_to_find_the_right_datasets)
    
    This blog covers an interesting but important topic regarding joining different dataframes and using APIs.



## Project Summary

### What types of films are doing best at the box office?

> Most Profitable Genres of Movies

![](https://github.com/carlearn/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/images/profit_by_genres.png)

> Most Popular Genres of Movies

![](https://github.com/carlearn/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/images/popularity_by_genres.png)


### When is the best time to release films?

> Seasonality of Film Release

![](https://github.com/carlearn/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/images/seasonality_by_genres.png)


### Who are the directors and actors to consider for the new film?

> Top 5 Directors

![](https://github.com/carlearn/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/images/top_5_directors.png)

> Top 5 Actors

![](https://github.com/carlearn/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/images/top_5_actors.png)



## Recommendation

#### 1. Genres
The new studio that Microsoft will launch shall produce the movies in genres of Adventure, Animation and Science Fiction from the profitability and popularity perspective.

#### 2. Seasonality
The best months to release these genres of movies should be: June, November/December (summer and holiday seasons)

#### 3. Best Crew
The best crew to hire are determined by movie genres. 



## Future Work

The analysis is based on the movie data on TMDb and IMDb for the period between 2010 and 2019 (i.e. pre-pandemic). However, the pandemic has changed the movie industry and especially the movie viewing habits of audience. 

#### 1. Data source:
As an alternative to the theater, people tend to view videos via social media and over-the-top media service (i.e. OTT service, such as Netflix, Hulu, Amazon Prime and etc). Therefore, our data sources should be expanded and cover more channels instead of theater box office numbers alone. 

#### 2. Movie genres:
Pandemics may have changed people's appetite to the genres of movies. Parents may spend more time with their kids to watch Animation, Family and History movies, while young people staying at home may prefer Action, Thriller and Horror movies to get excitement. We may reconsider which genre of movies is making more profits or getting more popular. Accordingly, we need to reevaluate the crew (including directors and actors) to hire.

#### 3. Release time:
As people tend to watch movies via OTT service, the release time may be more flexible. 

#### 4. Big IP / Series Movies:
On the other hand, the profits and top crews are largely determined by big IP movies. As a new studio, we should take the impact of big IPs into consideration. 
