## movie-recommender
![coverage](https://img.shields.io/badge/Python-3.10.9-purple) ![coverage](https://img.shields.io/badge/Framework-PyCharm-orange) ![coverage](https://img.shields.io/badge/API-TMDB-yellow)

# Kaggle database link
https://www.kaggle.com/code/ibtesama/getting-started-with-a-movie-recommendation-system

# How to run the project
1) Clone the repository and run movie-recommender-system.ipynb on jupyter notebook.
2) There are two csv file tmdb_5000_movie.csv tmdb_5000_credits.csv download them from kaggle.
3) Create PyCharm project
4) Add App.py file
5) Run command "streamlit run App.py" in the terminal
   
# Project Overview
For this project I have merge the two files on basis of title of the movie.
I have use genres, id, keywords, title, overview, cast, crew from the database to build the system.
I have first converted all these entity from string to list.
Then concatenated genres, keywords,overview, cast, crew into one single entity as tags.
Now new data frame is created with column names movie_id, title, tags.
I used CounteVectorizer from sklearn feature extraction library to transform tags into vector array.
Use nltk's PorterStemmer library to remove inbetween spaces from the words to avoid anomalous behaviour of the system.
After that sorted data according to cosine similarity which means according to vectors which are closest to given vector array.
Then showed first five movies which are similar to given movie.
Two pickle files are created first is movie_dict.pkl to show all the movies in the list and similarity.pkl is generated to show five similar movies using PyCharm framework.



