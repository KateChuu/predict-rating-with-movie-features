# predict-rating-with-movie-features
This is the project of the subject "Introductin to Machine Learning", aiming to find if adding the release year of movies is beneficial for predicting movie ratings using text features.
I used part of the features - `title`, `release_year`, `overview`, `tagline` and `production_companies` to build two models to predict the rating of the movies.

-----------------
## Code

a2.ipynb: includes complete code for pre-processing data, training and evaluating models, plotting and making predictions for the test set.
All the results of the models can be found in this file.


-----------------
## Data Files 

**1. TMDB_train.csv**
   
This file contains the movie features and labels for training instances.
- Number of instances: 100,000
- Number of columns: 44

The columns are (the column names are in the first row):
`id`, `title`, `release_year`, `overview`, `tagline`, `runtime`, `budget`, `revenue`, `adult`, `original_language`, `popularity`, `production_companies`, `genre_Action`, `genre_Adventure`, `genre_Animation`, `genre_Comedy`, `genre_Crime`, `genre_Documentary`, `genre_Drama`, `genre_Family`, `genre_Fantasy`, `genre_History`, `genre_Horror`, `genre_Music`, `genre_Mystery`, `genre_Romance`, `genre_Science Fiction`, `genre_TV Movie`, `genre_Thriller`, `genre_War`, `genre_Western`, `product_of_Canada`, `product_of_France`, `product_of_Germany`, `product_of_India`, `product_of_Italy`, `product_of_Japan`, `product_of_Spain`, `product_of_UK`, `product_of_USA`, `product_of_other_countries`, `vote_count`, `rate_category`, `average_rate`

The columns title, overview, tagline and production_companies contain the raw text data of these features.

The class label is in the last two columns: rate_category and average_rate. rate_category has 6 possible levels: 0, 1, 2, 3, 4 or 5.


**2. TMDB_eval.csv**
   
This file contains the movie features and labels for evaluation instances.
- Number of instances: 20,000
- Number of columns: 44

The columns in this dataset are similar to the training instances. I am going to use these instances to check the performance of my models.


**3. TMDB_test.csv**
   
This file contains the movie features for test instances.
- Number of instances: 20,000
- Number of columns: 42

The columns are (the column names are in the first row):
`id`, `title`, `release_year`, `overview`, `tagline`, `runtime`, `budget`, `revenue`, `adult`, `original_language`, `popularity`, `production_companies`, `genre_Action`, `genre_Adventure`, `genre_Animation`, `genre_Comedy`, `genre_Crime`, `genre_Documentary`, `genre_Drama`, `genre_Family`, `genre_Fantasy`, `genre_History`, `genre_Horror`, `genre_Music`, `genre_Mystery`, `genre_Romance`, `genre_Science Fiction`, `genre_TV Movie`, `genre_Thriller`, `genre_War`, `genre_Western`, `product_of_Canada`, `product_of_France`, `product_of_Germany`, `product_of_India`, `product_of_Italy`, `product_of_Japan`, `product_of_Spain`, `product_of_UK`, `product_of_USA`, `product_of_other_countries`, `vote_count`

I am going to use your developed model to predict the label for these instances and upload my results to the Kaggle Inclass competition.


-----------------
## Written report 

report.pdf: Contains the process of data pre-processing, training and making prediction, as well as the hypotheses and discussion.


-----------------
## Requirements

Make sure you can run the following code and download these toolkits for text pre-processing.

````
import nltk
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('punkt')
nltk.download('omw-1.4')
````
