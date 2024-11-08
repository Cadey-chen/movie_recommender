# Overview

Since I love watching and appreciating films from different genres and time periods, the goal of this project is to leverage Machine Learning techniques and movies big data in TMDB to create a dynamic system that recommends a list of movies to users based on their unique taste and mood. 

For users who loves watching different types of films for every special occasion and is searching for something new to watch, maybe something melancholy for a cozy autumn night or something funny and quirky to watch with friends, they can get relevant recommendations by telling this ML-powered recommender their unique mood and feeling at that moment, or enter the name of a movie they love already and find movies that are similar. Powered by big data, this recommender system can help users find those hidden gems they may have never heard of before but are great fun to watch. 

Here are the two amazing TMDB movie datasets I found on Kaggle I trained the ML model with:

1. The Movies Dataset by Rounak Banik: https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset
2. Full TMDB Movies Dataset 2024 (1M Movies) by asaniczka: https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies

The two datasets are first being merged together to have a better range of movies covered. Then, the 
original data is being filtered down with thresholds based on votes_count and audience_rating since audience ratings can be somewhat unreliable when the number of people who voted is too little, and we want to recommend users high or medium quality movies. 

More processing are being done to standardize rows into suitable datatypes for further analysis. Stemming was being applied to the keywords to ensure that different forms of the same word are represented accurately. Moreover, irrelevant and outlier data were also carefully checked and filtered out of the base dataset. 

To understand the how these movies relate to one another, I applied the Frequency-Inverse Document Frequency (TF-IDF) vectorizer and cosine similarity to calculate the similarity between each movie's plot description and keywords string. 

In this process, I found the most challenging part to be accurately representing the overall tone and style of the movie with the given data, since solely using plot description and keywords string can sometimes lead to ill-suited results because of a specific word (such as an object that was important to the plot, or two movies both have a character with the same name). To mitigate these, the algorithm also took other metadata values such as genres, production country, and ratings similarity into consideration, making the results more generalized.



