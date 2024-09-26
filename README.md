# Overview

This movie recommender system is based on the TMDB Movies dataset from Kaggle. Since I love watching and appreciating films of different genres and time periods, the goal of this project is to leverage the TMDB movies database and Machine Learning techniques to create a dynamic system that recommends a list of movies to users based on their unique tastes. As an example use case, for someone who loves watching and analying films from different genres and eras,
a recommendation system powered by machine learning can help me decide the perfect movie to watch depending on their mood. Using big data, this recommender system can also help users find those hidden gems they may have never heard of before but would be great fun to watch. 

Here are the two Kaggle datasets I used to train my model:

1. The Movies Dataset by Rounak Banik: https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset
2. Full TMDB Movies Dataset 2024 (1M Movies) by asaniczka: https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies

The two datasets are first being merged together to have a better range of movies covered. Then, the 
original data is being filtered down with thresholds on votes_count since audience ratings can be somewhat unreliable when the vote base is too little. More processing are being done to standardize rows into suitable datatypes for further analysis. Stemming was being applied to the keywords to ensure that different forms of the same word are represented accurately. Moreover, irrelevant and outlier data were also carefully checked and filtered out of the base dataset. 

To understand the how these movies relate to one another, I applied the Frequency-Inverse Document Frequency (TF-IDF) vectorizer and cosine similarity to calculate the similarity between each movie's plot description and keywords string. In this process, I found the most challenging part to be accurately representing the overall tone and style of the movie with the given data, since solely using plot description and keywords string can sometimes lead to ill-suited results because of a specific word (such as an object that was important to the plot, or two movies both have a character with the same name). To mitigate this, the model also took other metadata values such as genres, production country, and ratings similarity into consideration, and the results are more generalized.



