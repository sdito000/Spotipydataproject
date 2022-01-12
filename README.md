# Spotipyproject

# **What Makes a Song Popular?**

![iPhone 12, 12 Pro – 1](https://user-images.githubusercontent.com/91847452/149189842-909628f3-08ef-40c3-bc45-de3b0ff0ca8b.png)

Music is something that has an important part in all of our lives. When we listen to our favorite song, we feel good throughout our whole body, since dopamine is released. In fact, listening to music is important to our health. That’s why we wanted to conduct a data science investigation about popular music. What makes a song popular? 

## _**Motivation**_

Exploring what makes a song hit the top charts is a fascinating study that caught our eye, as the study is a great mix between data analysis, sociology, and art. We are interested in the possibility of predicting, using the popular streaming platform Spotify, if there exists a set pattern which makes a song climb up the music charts. We aim to study audio features, which we can pull from Spotify’s API, of top music of the last few years. Is there a pattern? Are some audio features directly connected to others? Is there a defining audio feature that is prominent in all top songs? Is there a collective music taste, or are all the top songs different? We hope to answer these questions. 


## _**Overview**_
Our project’s aim was to use Spotify’s API to obtain data on audio features of top songs in order to analyse what makes a song popular. Our data sample is the Global Top 25 songs of every November from the years 2018 to 2021. We used SpotifyCharts.com to obtain these songs.

Now, we want to familiarise you with the audio features we concentrated on. 

The features that we chose have to do with the mood and production properties of the song. We feel that these features (tempo, danceability, valence, energy, speechiness, loudness, and instrumentalness) really contribute to what attracts the average ear to top songs. 

The description of audio features we have used, which we got from Spotify For Developers’ website, as follows:

**Danceability**: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity.

**Energy**: Energy represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy.

**Instrumentalness**: Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. 

**Loudness**: Loudness describes how loud the track is.

**Speechiness**: Speechiness detects the presence of spoken words in a track. 

**Tempo**: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration

**Valence**: Valence describes the musical positiveness conveyed by a track. 


# _**Examples**_

We want to show you some top songs, so you can get an idea how the audio features values manifests in a top song. 

## **Taki Taki (with Selena Gomez, Ozuna, and Cardi B)** _By DJ Snake_

![Taki taki album](https://user-images.githubusercontent.com/91945641/148683880-55de9461-db89-44cf-9cd4-e81e3ae32ba5.png)

https://user-images.githubusercontent.com/91945641/148683616-e575c3eb-3672-4e8b-8800-92a7fb4a7266.mp4


Tempo
95.881

Danceability
0.842

Valence 
0.617

Energy 
0.801

Loudness
-4.167

Speechability 
0.228



## **Easy on Me** _By Adele_ 

![adele album](https://user-images.githubusercontent.com/91945641/148683866-a03af351-6d1e-4abc-a390-cc5b551bcbec.jpeg)

https://user-images.githubusercontent.com/91945641/148683640-040045ad-3522-4f05-b2ea-a2d7971c671c.mp4



Tempo
141.981

Danceability
0.604

Valence 
0.13

Energy 
0.366

Loudness
-7.519

Speechability 
0.028


![WhatsApp Image 2021-12-04 at 10 28 24 AM (1)](https://user-images.githubusercontent.com/91945641/148684206-6d948b8d-70f6-48fc-be20-9fdabdc69ef3.jpeg)

![WhatsApp Image 2021-12-04 at 10 28 25 AM](https://user-images.githubusercontent.com/91945641/148684185-c7be63a3-fd2b-4398-bacf-3617e04b76bd.jpeg)

Note: the features listed in the radar charts are a measure between 0 and 1. 

## A Puzzle

Taki Taki is the number one hit in November of 2018, while Easy on Me is the number one hit in November of 2021. As we can notice with these audio features, the two hit songs are quite different. 

How are they different from a data analyst’s standpoint? “Taki Taki” has a high valence and “Easy on Me” has a lower valence. This shows that any level of valence could climb up the charts. 

Another key difference is the energy levels, as “Taki Taki” clearly has a higher energy standing. 

Also we see some sort of correlation with energy and danceability, which we wanted to explore further.

From these songs’ data, we notice an irrelevance of speechiness here. Adele has a very low speechability as opposed to a relatively higher speechability in DJ Snake’s song. But when you listen to the music, it seems like Adele is singing more, while “Taki Taki” seems more instrumental. Our objective for studying speechiness was to see if more or less singing was more desirable to the human ear. But, this analysis shows that speechability measures do not help to explain our objective, as Adele’s top song is characterized by her lyrics. 

The only answer to our initial question that can be drawn from this comparison is that Both songs have high danceability, so that might contribute to the popularity of a song. 

### More Examples

![WhatsApp Image 2021-12-04 at 10 28 24 AM (2)](https://user-images.githubusercontent.com/91945641/148684312-e8f53094-9f5c-4e63-95ae-32ae70ca7752.jpeg)
![WhatsApp Image 2021-12-04 at 10 28 25 AM (1)](https://user-images.githubusercontent.com/91945641/148689454-a1d97e7a-2ca7-4779-910a-dcf493bc3d61.jpeg)

The top song in November of 2019 is "Dance Monkey" by Tones and I and the top song in November 2020 is "positions" by Ariana Grande.
