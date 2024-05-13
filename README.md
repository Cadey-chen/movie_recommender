# Overview

This movie recommender system is based on the TMDB Movies dataset from Kaggle. The goal is to create a dynamic system that recommends a list 
of movies to users based on their unique tastes. As someone who loves watching and analying films from different genres and eras,
a recommendation system powered by machine learning can help me decide the perfect movie to watch depending on my mood. I developed this 
program in hopes that it can give users that exact movie they might want to watch at that specific moment.

Data is first being processed so the genre and keywords fields can be used as parameters when recommending to the user. Then, the 
original data is being filtered such that only movies with more than 34 votes is being considered (the 75% quantile of the number 
of votes) to remove the bias where very few users gave a movie very high rating when we recommend based on average user ratings. 

Users can obtain a list of movies they like by supplying the program with a genre (e.g. Comedy, Family, Romance) and a parameter to 
rank the movies by. The can pick between ranking by the movie's popularity (number of people who rated the movie), average user rating, 
and a Bayesian average of the previous two measures.

To see the program in action, please watch the video here!

https://github.com/Cadey-chen/movie_recommender/assets/77594578/9a4fc209-ba3a-4557-be76-19569f188618

