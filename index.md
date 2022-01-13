
# **What Makes a Song Popular?**
Music is a tool that has unifying characteristics. Even though we all have different tastes and preferences, we can all talk about which songs we listen to when we are happy or which ones help us go through an exceptionally difficult time. That’s how our group came together: by discussing which songs we liked more than the others and why. Once we realised we have multiple favourite songs in common, we started asking each other: what makes a song popular?
Introducing our team members:



![group members](https://user-images.githubusercontent.com/91847452/149316564-aff0f924-8e3b-4dd9-923b-77fa90141bf3.png)

# Brief Overview // Executive Summary

## Motivation

Exploring what makes a song hit the top charts is a fascinating study that caught our eye, as the study is a great mix between data analysis, sociology, and art. We are interested in the possibility of predicting, using the popular streaming platform Spotify, if there exists a set pattern which makes a song climb up the music charts. We aim to study audio features, which we can pull from Spotify’s API, of top music of the last few years. Is there a pattern? Are some audio features directly connected to others? Is there a defining audio feature that is prominent in all top songs? Is there a collective music taste, or are all the top songs different? We hope to answer these questions. 

## Data

We used the top 25 songs in the month of November of 2018, 2019, 2020, 2021. Our group went to an outside source for this, which was spotifycharts.com. We obtained 100 songs' data through Spotify’s API on danceability, speechability, valence, tempo, energy, and loudness. 

## Methods 

We compiled the data we found on 100 songs in an Excel spreadsheet, and then found the mean, median, maximum, minimum, and finally standard deviation. 

By obtaining descriptive statistics, we used simple linear regression (SLR) and multiple linear regression (MLR) to determine whether there is a relationship between any audio features.

## Results 

Summary of our results

## Conclusion 

Summary of Conclusion 


In further detail, Here is what we found: 

## _**Purpose**_

Music is a tool that has unifying characteristics. Even though we all have different tastes and preferences, we can all talk about which songs we listen to when we are happy or which ones help us go through an exceptionally difficult time. That’s how our group came together: by discussing which songs we liked more than the others and why. Once we realised we have multiple favourite songs in common, we started asking each other: what makes a song popular? Furthermore, we realised that songs have scientifically proven healing and pleasing properties.

Starting from our general question “What makes a song popular?”, we wondered if predicting song popularity is possible. Hit Song Science (HSS), a term that was first used by Mike McCready, is about exploring whether song popularity can be predicted through audio features put into machine learning. While the validity of HSS continues to be a debate in the music industry, producers and record label companies are hopeful that a song’s popularity can be predicted through its audio features. 


## _**Overview**_
Our project’s aim was to use Spotify’s API to obtain data on audio features of top songs in order to analyse what makes a song popular. Our data sample is the Global Top 25 songs of every November from the years 2018 to 2021. We used SpotifyCharts.com to obtain these songs.

Now, we want to familiarise you with the audio features we concentrated on. 

The features that we chose have to do with the mood and production properties of the song. We feel that these features (tempo, danceability, valence, energy, speechiness, loudness, and instrumentalness) really contribute to what attracts the average ear to top songs. 

Here is a description of the audio features we have used: 


![audio features](https://user-images.githubusercontent.com/91847452/149315531-c69e90ee-c404-40e3-b1b3-48f80e005629.png)

**Danceability**: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity.

**Energy**: Energy represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy.

**Loudness**: The overall loudness throughout the entire track.

**Speechiness**: Speechiness detects the presence of spoken words in a track. 

**Tempo**: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration

**Valence**: Valence describes the musical positiveness conveyed by a track. 


# _**Justification**_

Understanding what makes a song popular will have great influence on business models that depend on popular music, such as radio stations, online audio streaming services (such as Spotify), and record labels. Hit Song Science will have a significant impact on the music industry. If the popularity of a song can be predicted before its release, it would create a commercial opportunity. Songwriters and composers will be able to focus on key elements that predict the song's popularity, and the budget will be better allocated. According to computer science students at Stanford University, HSS is a problem that the music industry is currently working on to solve (). Their research shows which audio features are the most influential elements that make a song popular. Inspired by their research, we wanted to establish a foundation for understanding whether predicting song popularity would be possible in the future. 



<img width="468" alt="Justification picture 1" src="https://user-images.githubusercontent.com/91945641/149319286-875a37bf-12ee-416d-9d86-f07c473dc43d.png">

<img width="468" alt="justification picture 2" src="https://user-images.githubusercontent.com/91945641/149319560-f3d6555d-6f07-4065-b396-5b9e570afe24.png">
Given the commercial significance of a success formula, there are media narratives on song popularity. These are some articles talking about which combination of audio features make a song popular. Notice how they say all songs sound the same - well does Easy on Me and Taki Taki sound the same to anyone? Conversely, while they have very different compositions of audio features, they are only two examples of megahit songs, so are they outliers? 

The second excerpt has a highlighted portion - songs that made the charts were more danceable, party going and tend to be happier. In terms of their translation to audio features, danceable is self-explanatory, party going is probably tempo and happier is higher valence

 This sentence assumes two things: firstly, the audio features are impacting positioning and secondly, there is a sort of relationship between the audio features - in the sense they are rising all at the same time. Hence, it is important for us to investigate to what extent these assumptions hold true: Our results contribute to reconstructing media narratives and commercial music production value for music executives and artists alike.


# _**Aim**_

Our project’s aim is to gain more insight on the factors that make a song popular. We want to see if there exists a formula that artists can comply with that will make their song reach the top charts. Another aspect of our aim is to see if popular music has any significant relationships among audio features. 


# _**Data**_

Using SpotifyCharts as a reference, we turned to Spotify's web API, Spotipy. After we created a Spotify web developer account, we created an APP and obtained our Client ID and Client Secret. Moving onto audio feature analysis, we first need to retrieve each individual track’s URI. We used Spotipy’s search feature, requested an Oauth token, and then proceeded with individual track’s data. We inputted the track’s name under “Q”, “track” under “Type”, and Spotipy produced a long list of code. After copying a track’s URI, we utilised the audio feature search tool, and the API gave us a list of all the different audio features already analysed by Spotify. We recorded these values in an excel sheet, and repeated the steps with the other tracks. 

We gathered a total of 100 data points, 25 songs over 4 years worth of charts. We compiled the data points into a singular excel sheet. These songs were the 25 songs on Spotfiy Global with the highest weekly streams for the first week of November. 

We extracted six audio features for our data analysis - tempo, valence, danceability, energy, loudness and speechiness. All the audio features except tempo have values between 0 and 1 with 1 being the highest level and 0 being the lowest. Values for loudness range between -60dB and 0, with 0 being no volume at all. With tempo being a measure of beats per minute, the range of values for tempo could theoretically be nonexistent.


## Examples

We want to show you some top songs, so you can get an idea how the audio features values manifests in a top song. 

## **Taki Taki (with Selena Gomez, Ozuna, and Cardi B)** _By DJ Snake_

![Taki taki album](https://user-images.githubusercontent.com/91945641/148683880-55de9461-db89-44cf-9cd4-e81e3ae32ba5.png)

https://audio.jukehost.co.uk/rmjuk0Xw6LjAvn3EUBj9wFNPyOOSxIJP 


<img width="405" alt="Screen Shot 2022-01-13 at 11 43 51 AM" src="https://user-images.githubusercontent.com/91945641/149324475-355f2bc5-ceb3-4798-a8a5-093171887717.png">



## **Easy on Me** _By Adele_ 

![adele album](https://user-images.githubusercontent.com/91945641/148683866-a03af351-6d1e-4abc-a390-cc5b551bcbec.jpeg)

https://audio.jukehost.co.uk/TpHi7dPjFewH4z1FxUExLBNEsc5RMCUc 

<img width="405" alt="Screen Shot 2022-01-13 at 11 44 59 AM" src="https://user-images.githubusercontent.com/91945641/149324568-58b76503-ee95-41c6-9031-0ee1df8f241e.png">


![WhatsApp Image 2021-12-04 at 10 28 24 AM (1)](https://user-images.githubusercontent.com/91945641/148684206-6d948b8d-70f6-48fc-be20-9fdabdc69ef3.jpeg)

![WhatsApp Image 2021-12-04 at 10 28 25 AM](https://user-images.githubusercontent.com/91945641/148684185-c7be63a3-fd2b-4398-bacf-3617e04b76bd.jpeg)

Note: the features listed in the radar charts are a measure between 0 and 1. 

## A Puzzle // Initial Observations

Taki Taki is the number one hit in November of 2018, while Easy on Me is the number one hit in November of 2021. As we can notice with these audio features, the two hit songs are quite different. 

How are they different from a data analyst’s standpoint? “Taki Taki” has a high valence and “Easy on Me” has a lower valence. This shows that any level of valence could climb up the charts. 

Another key difference is the energy levels, as “Taki Taki” clearly has a higher energy standing. 

Also, we see some sort of correlation with energy and danceability, which we want to explore further.

From comparing and contrasting these two #1 songs, we notice an irrelevance of speechiness here. Adele has a very low speechability as opposed to a relatively higher speechability in DJ Snake’s song. But when you listen to the music, it seems like Adele is singing more, while “Taki Taki” seems more instrumental. Our objective for studying speechiness was to see if more or less singing was more desirable to the human ear. But, this analysis shows that speechability measures do not help to explain our objective, as Adele’s top song is characterized by her lyrics. 

The only answer to our initial question that can be drawn from this comparison is that Both songs have high danceability, so that might contribute to the popularity of a song. 

We will explore that further. 

### More Examples

![WhatsApp Image 2021-12-04 at 10 28 24 AM (2)](https://user-images.githubusercontent.com/91945641/148684312-e8f53094-9f5c-4e63-95ae-32ae70ca7752.jpeg)
![WhatsApp Image 2021-12-04 at 10 28 25 AM (1)](https://user-images.githubusercontent.com/91945641/148689454-a1d97e7a-2ca7-4779-910a-dcf493bc3d61.jpeg)

The top song in November of 2019 is "Dance Monkey" by Tones and I and the top song in November 2020 is "positions" by Ariana Grande. 



# _**Methodology**_
After compiling our data into Excel sheets, we ran descriptive statistics utilising Excel’s features. We calculated the mean, medium, maximum & minimum values as well as standard deviation on the audio features we selected I.e. tempo, valence, danceability, energy, loudness & speechiness for 2018-21. 

<img width="1117" alt="Screen Shot 2022-01-13 at 12 34 25 PM" src="https://user-images.githubusercontent.com/91945641/149331116-adc7d7b0-434d-47df-8ed0-b9eea649ea66.png">


By looking at the values, there is a story emerging. The mean, median and standard deviation of tempo, energy and valence increases steadily between 2018 and 2021. This means that your favourite top songs, on average, are more likely to exhibit musical positivity, upbeat rhythms and energy over the years. However, the range of values of these audio features of top songs also expands over the years.

Conversely, the descriptive statistical values for danceability and loudness decreases steadily between 2018 and 2021. This means that your favourite mainstream song is potentially less loud and dancelike and most top songs have similar range of lower danceability and loudness over the years. This contradicts the media article’s assumption that songs rise in danceability over the years. 

The next step would be to investigate whether there is any relationship between the audio features that increase or decrease respectively. To do so, we exported this excel sheet into Stata and R respectively for data analysis. 
	
In order to study the relationship between a track’s position and its audio features, we turned to Stata to use a Simple Linear Regression (SLR) model. Regressions are used to determine the relationship between 2 or more variables, and quantitatively analyse how one variable changes when the other changes. We want to understand whether certain values of audio features will place a track higher or lower on the list. When these values change, we want to see whether their placement changes as well. 

In order to study the relationships between audio features, we used multiple regression analysis(MLR). MLR allows us to test relationships between multiple independent variables and a single dependent variable. For instance, we can test the direction and strength of relationship between danceability (dependent) with tempo, energy, valence, loudness i.e. all audio features. And we did! We constructed multiple MLR relationships to define each audio feature as y and rest as x: this is get a full combination of every single relationship possible over 4 years. Many times multiple factors affect one variable linearly in real life even if they are correlated with each other: None can make a song with just a single audio feature. Testing relationships allow us to explore common themes and interesting threads of popular music.

## Visualising Each Year’s Mean Value 

![WhatsApp Image 2022-01-13 at 9 32 57 AM](https://user-images.githubusercontent.com/91945641/149321816-ec868527-7174-4c2d-a9ec-d180605a53e9.jpeg)

Add a description

# _**Results**_
As illustrated above, the top 2 songs of two different years have drastically different makeup of audio features. However, they share a similarity of high danceability. Upon discovering this, we examined whether we can predict a track’s placement on the top 25 by its audio features.

## Simple Linear Regression (SLR) 

With the Simple Linear Regression approach, we estimate the following equation:


<img width="630" alt="Screenshot 2022-01-12 at 18 04 00" src="https://user-images.githubusercontent.com/92088621/149196699-d34068b1-e9ea-49d1-b9e2-9435a66ebcd9.png">

The track’s position is the dependent (y) variable, and danceability is the independent (x) variable. β0 is the constant, ie. what is the track’s position when danceability equals 0. For the purposes of our project, we disregard β0. β1 serves as the coefficient in front of danceability. In other words, when the danceability increases by 1 unit, by how much does a track shift up on the charts. Ei serves as the error term for our equation, accounting for any confounding factors or errors in our estimation. 

<img width="839" alt="Screenshot 2022-01-12 at 17 43 58" src="https://user-images.githubusercontent.com/92088621/149193693-03c26b38-f3e6-42ad-926e-aa29ac8b0515.png">

Table 1 shows the Simple Linear Regression with our main explanatory variable, danceability, on chart placement. We find that at an aggregate level, danceability has a negative relationship with a track’s chart placement. A one unit increase in danceability is estimated to shift a track up by 8 positions on the top charts(in this case, a lower number, for example 1 or 2, translates to a higher position). A higher danceability value is associated with a higher placement on the charts. However, this coefficient is not statistically significant, ie. the results are likely to occur by chance. We wanted to examine how the 4 different years contributed to this coefficient, thus we broke it down in the following columns. 

In column 2, if a 2018 song has a high danceability value, it is actually positively correlated with their position on the charts. However, this coefficient is not statistically significant. This relationship is also apparent in column 3 with 2019 tracks and 2019 positions.

In column 4, if a song has a high danceability value, it is negatively associated with their position on the charts. Its coefficient is statistically significant at the 5% level; the results are not easily explained by chance alone. The same relationship and same statistical significance applies in column 5 with 2021 tracks and positions. 

On one hand, we obtained 2 years with positive coefficients. On the other hand, we obtained 2 years with negative coefficients. This leads to our negative coefficient in column 1 with no statistical significance overall. 

We observed that the relationship between positions and audio features fluctuate within each year between positive and negative, large and small coefficients. We continued to conduct SLR with other audio features against positions, such as valence and energy, but found danceability to have the most statistically significant results. Consistent with our findings, music is abstract; what makes a song popular has multiple confounding factors.

Danceability has the most significant results, it sounds more intuitive that they will all affect each other equally - why is there a variable relationship, there are differing relationships

## Multiple Linear Regression


<img width="453" alt="MLR" src="https://user-images.githubusercontent.com/91945641/149322485-faae16ca-4a34-41ad-934f-cfc863ac2d1d.png">

Here the table shows the results of meaningful multiple regression results. By meaningful, we mean results which generally have only around 10% chance of being a random error. While statisticians tend to hold only 5% error and we have upheld that principal for SLR results, our sample size is quite limited and the time period for our data collection is very specific. Therefore we recognise that extending error rate can allow us to look at more relationships that may have been statistically significant i,.e. P value les than 0.05, if sample size and time period for data collection was wider. 

The estimate indicates the strength and direction of the relationship. Here all the relationships are positive. An estimate of 0.49 between  energy and danceability in 2018 means that if energy increases by 1 unit, danceability increases by 0.49 unit. The estimates that are 0 are ones that have very negligible non-zero increases in unit. While the relationships vary in strength and statistical significance, some common themes emerge over the years. 

Both energy and tempo have a meaningful relationship with valence in 2019 and the meaningful relationship between tempo and valence continues in 2020 while tempo and energy have a positive meaningful relationship in 2020 and 2021. This provides a more nuanced look into the nature of these audio features which seemed to increase in mean between 2018 and 2021 according to the descriptive statistics. 

The simple linear regression analysis on chart positioning only found a statistically significant relationship between danceability and chart position. Hence, it is important to look from the lens of danceability and see if it has meaningful relationships with other audio features. Here we can see that energy and danceability have a positive meaningful relationship in 2018 and 2021. Valence has a positive meaningful relationship with danceability in 2019 and 2020 while tempo has a positive meaningful relationship with danceability in 2019, 2020 and 2021. 

<img width="1055" alt="Screen Shot 2022-01-13 at 12 42 54 PM" src="https://user-images.githubusercontent.com/91945641/149332317-6ac01586-4a65-4c2c-b967-c4229fbe5019.png">

Key points to note:


1.	The points in the scatter plot are widely dispersed and there is a lot of variance. This makes it difficult to establish a meaningful relationship between the variables. 
2.	The outliers are marked by their album covers. There are a lot of outliers which means even if there is a meaningful relationship there a considerable number of songs that do not fit the mold is it is difficult to generalize, 



# Conclusion 

Our objective was to explore whether we can predict song popularity through its audio features. As a group, we kept asking ourselves, “what makes a song popular?” We analysed…. 

Music is abstract. It makes sense that there was no set pattern, no defining audio features, and no similar songs. All songs are different and all tastes are different. People may listen to a song because they like the lyrics. Or, someone may like the artist or the producer. Perhaps, someone likes the genre placement. After all, most people have a short attention span with music – they get bored of the same song repeatedly. These reasons mean that Spotify’s algorithm for determining audio features cannot tell us what we wanted to hear. There are other factors that make music popular, which cannot be studied through our data analysis. 

Other factors 

- Lyrics 
- Previous work and popularity 
- Genre placement 
- Whether it is innovative/original
- Music is abstract 


It is important to refer to the limitations we have faced that require further research. First of all, we analysed the top 25 most globally streamed songs for our research. If we were to evaluate a specific country’s top 25 most streamed songs, we might have gotten different results. Secondly, we analyse a small sample of songs from a short period of time. We only look over the top 25 songs from 4 consecutive years: 2018, 2019, 2020 and 2021. Next, with the wide presence of social media, song popularity can be altered according to the social influence we receive. According to Pachet, “[kn]owing that a song is a hit…influences our liking” (2012). One social media platform that comes to mind is TikTok. We noticed that the majority of songs we analyzed are (or were at one point) widely used songs on TikTok. Lastly, a change of website where we acquired our data might cause different results. There are other websites such as Billboard that also provide the same type of data. With these limitations in place, our result is that it is not possible to predict song popularity. 
	Moving forward, further research is needed to eliminate the limitations mentioned above. Once predicting song popularity is accomplished, we can investigate whether automatic generation of hit songs is possible through the same audio features we analysed. 


# Appendix 

# References 

https://www.pnas.org/content/116/9/3793

https://www.researchgate.net/publication/220723429_Hit_Song_Science_Is_Not_Yet_a_Science


# Thanks for listening!
