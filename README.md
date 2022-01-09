# **What Makes a Song Popular?**

<img width="911" alt="Screen Shot 2022-01-09 at 1 24 34 PM" src="https://user-images.githubusercontent.com/91945641/148684009-aebdf365-4b97-4ad3-bd8a-a154a3f1662f.png">


Exploring what makes a song hit the top charts is a fascinating study that caught our eye, as the study is a great mix between data analysis, sociology, and art. We are interested in predicting, using the popular streaming platform Spotify, if there exists a set pattern which makes a song hit the top charts. Some professional musicians claim they know exactly how to compose a top chart song. Psychologists say that dopamine is released when humans listen to their favorite song. So audio features, such as loudness and danceability, might play a role in higher levels of good feelings in the human brain. We are inspired to see if these claims are true, through our study of Spotify’s audio features. So, What makes a song Popular? 

## _**Overview**_
Our project’s aim was to use Spotify’s API to obtain data on audio features of top songs in order to analyse what makes a song popular. Our data sample is the Global Top 25 songs of every November from the years 2018 to 2021. We used SpotifyCharts.com to obtain these songs.

Now, we want to familiarise you with the audio features we concentrated on. 

<img width="911" alt="Screen Shot 2022-01-09 at 1 26 05 PM" src="https://user-images.githubusercontent.com/91945641/148684062-cce15468-bd63-4c10-8e61-c659ab319e9c.png">

The features that we chose have to do with the mood and production properties of the song. We feel that these features (tempo, danceability, valence, energy, speechiness, loudness, and instrumentalness) really contribute to what attracts the average ear to top songs. 

The description of audio features we have used, which we got from Spotify For Developers’ website, as follows:

Acousticness: A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic. 
Danceability: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.
Energy: Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy.
Instrumentalness: Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context.  The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content.
Speechiness: Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.
Tempo: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration
Valence: A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).



## _**Examples**_

We want to show you some top songs, so you can get an idea how the audio features values are manifested for a top song. 

# **Taki Taki (with Selena Gomez, Ozuna, and Cardi B)**
_By DJ Snake_

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



## **Easy on Me**
_By Adele_ 

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
![WhatsApp Image 2021-12-04 at 10 28 24 AM (2)](https://user-images.githubusercontent.com/91945641/148684324-50b454f2-1b7b-4363-a318-79edc095abc7.jpeg)

The top song in November of 2019 is "Dance Monkey" by Tones and I and the top song in November 2020 is "positions" by Ariana Grande.

