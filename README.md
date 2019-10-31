# Songs Clustering Recommendations

A content-based music recommendation system based on cluster analysis

### Objective

- Developing a Spotify playlist builder with a songs recommender using KMeans algorithm.

### How it's done

- First, it's created a dataset with songs presents in the "Browse" area in Spotify. These songs will be used to train the algorithm that will recommend the songs.
- Then, Using Spotifys API to collect those songs and users songs in their playlists. The code used to collect the songs is in a [jupyter notebook](https://github.com/gabrielfas/songs_clustering_recommendations/blob/master/Collect%20songs.ipynb), and the methods to retrieve the songs are made by [Eduardo](https://github.com/edujtm) on his repository [diversify](https://github.com/edujtm/diversify)
- After collecting the songs, it will be preprocessed both main and users datasets, and applied in the KMeans algorithm to generate the clusters, the KMeans methods used were train (main dataset) and predict (users datasets).
- Knowing to which cluster belong each of the user songs, it's discovered the percentage of songs in each cluster. Then, it's applied to the main dataset to retrive a random sample of songs based on the proportion of the user songs in each cluster. By the end, creating a new playlist with at maximum 100 songs from the main dataset recommended by the algorithm.
