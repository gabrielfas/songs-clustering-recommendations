# Songs Clustering Recommendations

A content-based music recommendation system based on cluster analysis

### Objective

- Developing a Spotify playlist builder with a songs recommender using KMeans algorithm.

### How it's done

- First, it's created a dataset with songs presents in the "Browse" area in Spotify. These songs will be used to train the algorithm that will recommend the songs.
- Then, Using Spotifys API to collect those songs and users songs in their playlists. The code used to collect the songs is in a [jupyter notebook](https://github.com/gabrielfas/songs_clustering_recommendations/blob/master/Collect%20songs.ipynb), and the methods to retrieve the songs are made by [Eduardo](https://github.com/edujtm) on his repository [diversify](https://github.com/edujtm/diversify).
- After collecting the songs, it will be preprocessed both main and users datasets, and applied in the KMeans algorithm to generate the clusters, the KMeans methods used were train (main dataset) and predict (users datasets).
- Knowing to which cluster belong each of the user songs, it's discovered the percentage of songs in each cluster. Then, it's applied to the main dataset to retrive a random sample of songs based on the proportion of the user songs in each cluster. By the end, creating a new playlist with at maximum 100 songs from the main dataset recommended by the algorithm.

### How to use

- First, the notebook named [Collect songs](https://github.com/gabrielfas/songs_clustering_recommendations/blob/master/Collect%20songs.ipynb) is used to retrive the songs for the training dataser and user dataset. So, you need to release the access to the Spotify's API, after that you can collect the songs saved for the user logged into the API and get any users playlists songs.

- After collecting the datasets, you can use the [Cluster songs](https://github.com/gabrielfas/songs_clustering_recommendations/blob/master/Cluster%20songs.ipynb) notebook passing both the train dataset (to train the clusters) and the users dataset (to predict the clusters and make recommendations).

### Requirements

- Python 3.7
- Jupyter Notebook
- [Pandas](https://pandas.pydata.org/)
- [Numpy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [scikit-learn](https://scikit-learn.org/stable/)
- [Missingno](https://github.com/ResidentMario/missingno)
- [Diversify](https://github.com/edujtm/diversify)
