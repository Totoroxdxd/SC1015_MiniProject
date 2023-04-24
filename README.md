# SC1015 Mini-Project
![coverimage](https://user-images.githubusercontent.com/120243245/233890752-2eddb92b-4543-4a84-9a9e-e3f81eed2121.png)


## Motivation: Song Popularity Prediction
As aspiring songwriters, we want to find out if the music we write will be a hit before releasing.

Spotify is the most popular music streaming platform as of 2023, thus the popularity of a song on Spotify could be a good indicator of a song's success. As such, we will be using a Spotify music related dataset to do our popularity prediction.  

**This brings us to our problem definition:** “What are the key song attributes that would determine if a song would become popular on Spotify?”

## Dataset
CSV: [Spotify Song Features](SpotifyFeatures.csv)
Dataset is taken from Kaggle thanks to Zaheen Hamidani who made it avaliable: https://www.kaggle.com/datasets/zaheenhamidani/ultimate-spotify-tracks-db.

The dataset contains details from 232,725 song tracks across 26 music genre. In addition, after cleaning this dataset, we have also created a subset of this dataset with song lyrics added. (Check our jupyter notebook for details on why we created a seperated dataset)

Check out our [data description file](data_description.md) for brief descriptions of each data variables.

Detailed description of the dataset could be on [Spotify's API](https://developer.spotify.com/documentation/web-api).

## Jupyter Notebook
You can view the Jupyter Notebook of this project [here](SongPopularityPrediction.ipynb).

---

## Machine Learning Models and Libraries Used

### For Data Manipulation
- pandas
- numpy

### For Data Visulisation
- matplotlib.pyplot
- seaborn  

### For Web Scrapping
- requests
- bs4  

### For Natural Language Processing
- json
- nltk
- fasttext

### For Machine Learning
- sklearn


## Outcome and Conclusion
Our model has an accuracy of about 35% when predicting song popularity into 5 classes, which is slightly better than random chance (20%).

It turns out song popularity is not that easy to predict and there must be many factors outside of what Spotify can provide us with.

Perhaps the artist names has a correlation to popularity, however that was not our focus since we wanted a model that we could use to predict the songs that we write.

With the help of lyrics scrapping, we managed to get a better working model, which tells us the lyrics of a song does affect it's popularity to a certain extent. However, the 35% accuracy also mean that lyrics does not contribute as much to the song's performance. This is to be expected as many people listen to songs for their melody and pay little to no attention to the lyrics.

This gives us an idea for our next DSAI project: perhaps we can analyse the audio data of songs and see if that helps with popularity prediction.

---
  

  

## Slides
[Click Here](SC1015_MiniProjectPresentationSlides.pdf) to view our slides




## What have we learnt
This project allowed us to gain many new knowledge outside of the classroom.

## Data Cleaning
We learnt to clean data based on context.
For example, since we are interested in writing pop and country songs, we narrowed the scope of the dataset by focusing only on pop and country songs. In addition, we have also experienced how to identify what data to clean while doing EDA. Such as removing duplicated values and replacing values.

## Class imbalance
We learnt how imbalanced classes would result in our machine learning model to have large differences between the accuracy of our test and train model while doing the project. As such, we try to make our response variable (categorical) to be as balanced as possible.

### Webscrapping
Due to the lack of good predictors, we were forced to come add a new predictor to our dataset: lyrics.

In order to do this we needed to learn how to scrape sites using BeautifulSoup.


### Natural Language Processing
This is our first time working the unstructured data that is natural language.

In order to process the lyrics into structured data, we had to learn NLP concepts such as
- Tokenization
- Stop Words
- Stemming
- Lemmatization
- Bag-of-Words Model
- N-grams
- Parts-of-Speech
- Document-Term Matrix

Since this is our first NLP project, we decided to use a basic Bag-of-Words Model without N-grams or Part-of-Speech analysis.
### Machine Learning
In the interest of reducing the number of words/features needed to train our model, we implemented Dimensionality Reduction techniques.

We ended up using the **Chi-Squared Test** to pick the most "influential" words to use.

#### Model Selection
We also learnt about the various models that are usually used in NLP. For example, the Naive Bayes model that we ended up using.

Furthermore, we also learnt to test multiple model and choose the best one by performing a 5-Fold **cross-validation** instead of just a simple train-test split analysis.

---


# Contributors
Ye Chuan  
Elaine

---

# Presentation Video link
[Click Here](https://youtu.be/3QPJ165z1Vg) to view our presentation video.


# References

  Genius:  https://genius.com/  
  Spotify API for developer: https://developer.spotify.com/documentation/web-api  
  Spotify for Artist: https://artists.spotify.com/home

---
