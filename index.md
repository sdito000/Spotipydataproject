
# **What Makes a Song Popular?**

Music is a tool that has unifying characteristics. Even though we all have different tastes and preferences, each of us can talk about which songs we listen to when we are happy or which ones help us go through an exceptionally difficult time. That’s how our group came together, by discussing which songs we liked more than the others and why. Once we realised we have multiple favourite songs in common, we started asking each other, "What makes a song popular?"

*Introducing our team members:*

![group members](https://user-images.githubusercontent.com/91847452/149316564-aff0f924-8e3b-4dd9-923b-77fa90141bf3.png)

## _**Brief Overview // Executive Summary**_

Exploring what makes a song hit the top charts is a fascinating study that caught our eye, as the study is a great mix between data analysis, sociology, and art. We are interested in the possibility of predicting song popularity, using the popular streaming platform Spotify, if there exists a set pattern of features which make a song climb up the music charts. We aim to study audio features, which we pulled from Spotify Web API, of the top music of the last few years. 

We used the top 25 songs of the first week of November of 2018, 2019, 2020, and 2021. Our group went to an outside source, spotifycharts.com, to access the data we needed. We obtained 100 songs' data through Spotify’s API on danceability, speechability, valence, tempo, energy, and loudness. 

We compiled the data we found on 100 songs in an Excel spreadsheet, and then found the mean, median, maximum, minimum, and standard deviation. By obtaining descriptive statistics, we used simple linear regression (SLR) and multiple linear regression (MLR) to determine whether there is a relationship between any audio features.

After running Simple Linear Regressions, we found that over 4 years of data, a high danceability value is associated with a higher position on the charts. According to our Multiple Regression results, there are some relationships that are sustained over a few years. The longest meangiful relationship is the one between tempo and danceability that is sustained for 3 years while valence and energy sustain a relationship with danceability for two years each. 

To answer our question "What makes a song popular?", we came to the conclusion that despite some common themes in viral spotify hit songs, music is an abstract concept. It is difficult to fully predict whether a song will reach the top charts. There is also limitations to our research and the most prominent one is that we had a small song sample. We could tell you what audio features predicted rise of top 25 songs during year-end 2018-2021. However, we cannot confirm that we know how your song will climb the global music charts. We present such a nuanced outlook in our data project below. 


## _**Purpose**_

Starting from our general question “What makes a song popular?”, we wondered if predicting song popularity is possible. _Hit Song Science_ (HSS), a term that was first used by Mike McCready, is about exploring whether song popularity can be predicted through audio features put into machine learning. While the validity of HSS continues to be a debate in the music industry, producers and record label companies are hopeful that a song’s popularity can be predicted through its audio features. 

We want to connect _Hit Song Science_ to data analysis of the Spotify's API. As we defined our project, we started asking new questions: Is there a pattern? Are some audio features directly connected to others? Is there a defining audio feature that is prominent in all top songs? Is there a collective music taste, or are all the top songs different?


## _**Preface**_

Our project’s aim is to use Spotify’s API to obtain data on audio features of top songs in order to analyse what makes a song popular. Our data sample is the Global Top 25 songs of the first week of November from the years 2018 to 2021. We used SpotifyCharts.com to obtain these songs.

Now, we want to familiarise you with the audio features we concentrated on. 

The features that we chose have to do with the mood and production properties of the song. We feel that these features (tempo, danceability, valence, energy, speechiness, loudness, and instrumentalness) really contribute to what attracts the average ear to top songs. 

Here is a description of the audio features we have used (Spotify Web API reference, 2022): 


<p align="center"> <img width="450" alt="audio features" src="https://user-images.githubusercontent.com/91847452/149315531-c69e90ee-c404-40e3-b1b3-48f80e005629.png"></p>


**Danceability**: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity.

**Energy**: Energy represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy.

**Loudness**: The overall loudness throughout the entire track.

**Speechiness**: Speechiness detects the presence of spoken words in a track. 

**Tempo**: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration

**Valence**: Valence describes the musical positiveness conveyed by a track. 


## _**Justification**_

Understanding what makes a song popular will have great influence on business models that depend on popular music, such as radio stations, online audio streaming services (such as Spotify), and record labels. Hit Song Science will have a significant impact on the music industry. If the popularity of a song can be predicted before its release, it would create a commercial opportunity. Songwriters and composers will be able to focus on key elements that predict the song's popularity, and the budget will be better allocated. However, HSS is a problem that the music industry is currently working on to solve (Pham et al., 2015). A research conducted by Stanford University, shows which audio features are the most influential elements that make a song popular. Inspired by their research, we wanted to establish a foundation for understanding whether predicting song popularity would be possible in the future. 

Furthermore, given the commercial significance of a success formula, there are media narratives on song popularity. These are some articles talking about which combination of audio features make a song popular.


<p align="center"> <img width="468" alt="Justification picture 1" src="https://user-images.githubusercontent.com/91945641/149319286-875a37bf-12ee-416d-9d86-f07c473dc43d.png"></p>

<p align="center"> <img width="468" alt="justification picture 2" src="https://user-images.githubusercontent.com/91945641/149319560-f3d6555d-6f07-4065-b396-5b9e570afe24.png"></p>


The article has a highlighted portion - songs that made the charts were more danceable, party going and tend to be happier. In terms of their translation to audio features our interpretations are as follows: "danceable" is danceability, "party going" is tempo and "happier" is higher valence.

The sub-heading assumes two things: firstly, the audio features are impacting positioning and secondly, there is a sort of relationship between the audio features - in the sense they are rising all at the same time. Hence, it is important for us to investigate to what extent these assumptions hold true. Our results contribute to reconstructing media narratives and commercial music production value for music executives and artists alike.


## _**Aim**_

Our project’s aim is to gain more insight on the factors that make a song popular. We want to see if a formula exists that artists can comply with that will make their song reach the top charts. Another aspect of our aim is to see if popular music has any significant relationships among audio features. 


## _**Data**_

Using SpotifyCharts as a reference, we turned to Spotify's web API, Spotipy. After we created a Spotify web developer account, we created an APP and obtained our Client ID and Client Secret. Moving onto audio feature analysis, we first need to retrieve each individual track’s URI. We used Spotipy’s search feature, requested an Oauth token, and then proceeded with individual track’s data. We inputted the track’s name under “Q”, “track” under “Type”, and Spotipy produced a long list of code. After copying a track’s URI, we utilised the audio feature search tool, and the API gave us a list of all the different audio features already analysed by Spotify. We recorded these values in an excel sheet, and repeated the steps with the other tracks. 

We gathered a total of 100 data points, 25 songs over 4 years worth of charts. We compiled the data points into a singular excel sheet. These songs were the 25 songs on Spotfiy Global with the highest weekly streams for the first week of November. 

We extracted six audio features for our data analysis - tempo, valence, danceability, energy, loudness and speechiness. All the audio features except tempo have values between 0 and 1 with 1 being the highest level and 0 being the lowest. Values for loudness range between -60dB and 0, with 0 being no volume at all. With tempo being a measure of beats per minute, the range of values for tempo could theoretically be nonexistent.


### Examples

We want to show you some top songs, so you can get an idea how the audio features' values manifests in a top song:

### **Taki Taki (with Selena Gomez, Ozuna, and Cardi B)** _By DJ Snake_
[Audio Sample of "Taki Taki"](https://audio.jukehost.co.uk/rmjuk0Xw6LjAvn3EUBj9wFNPyOOSxIJP)


<p align="center"><img alt="Taki taki album" src="https://user-images.githubusercontent.com/91945641/148683880-55de9461-db89-44cf-9cd4-e81e3ae32ba5.png"></p>

<p align="center"><img width="405" alt="Screen Shot 2022-01-13 at 11 43 51 AM" src="https://user-images.githubusercontent.com/91945641/149324475-355f2bc5-ceb3-4798-a8a5-093171887717.png"></p>



### **Easy on Me** _By Adele_ 
[Audio sample of "Easy on Me"](https://audio.jukehost.co.uk/TpHi7dPjFewH4z1FxUExLBNEsc5RMCUc).

<p align="center"><img alt="adele album" src="https://user-images.githubusercontent.com/91945641/148683866-a03af351-6d1e-4abc-a390-cc5b551bcbec.jpeg"></p>


<p align="center"><img width="405" alt="Screen Shot 2022-01-13 at 11 44 59 AM" src="https://user-images.githubusercontent.com/91945641/149324568-58b76503-ee95-41c6-9031-0ee1df8f241e.png"></p>

Below are radar charts comparing the values between the two popular songs.

<p align="center"><img width="779" alt="Screen Shot 2022-01-14 at 4 17 56 PM" src="https://user-images.githubusercontent.com/91945641/149548981-9eb52760-3a6d-46f9-afd4-451e90d0f1fc.png"></p>

_Note: The features listed in the radar charts are a measure between 0 and 1._


### A Puzzle // Initial Observations

"Taki Taki" is the number one hit song in the 2018 sample while "Easy on Me" is the number one hit song in the 2021 sample. As we can notice with these audio features, the two hit songs are quite different. 

How are they different from a data analyst’s standpoint? “Taki Taki” has a high valence and “Easy on Me” has a lower valence. This shows that any level of valence could climb up the charts. 

Another key difference is the energy levels, as “Taki Taki” clearly has a higher energy standing compared to "Easy on Me"

Also, we see some sort of correlation with energy and danceability, which we want to explore further.

From comparing and contrasting these two #1 songs, we notice an irrelevance of speechiness. Adele has a very low speechability as opposed to a relatively higher speechability in DJ Snake’s song. But when you listen to the music, it seems like Adele is *talking* more, while “Taki Taki” seems more instrumental. Our objective for studying speechiness was to see if more or less singing was more desirable to the human ear. But, this analysis shows that speechability measures do not help to explain our objective, as Adele’s top song is characterized by her lyrics. 

The only answer to our initial question that can be drawn from this comparison is that both songs have high danceability, so we came to the conclusion that danceability is an essential factor in predicting song popularity. 


### More Examples


<p align="center"><img width="779" alt="Screen Shot 2022-01-14 at 4 19 07 PM" src="https://user-images.githubusercontent.com/91945641/149548971-3420de7e-143f-4200-836b-9bc22bf7c39b.png"></p>

The top song in our 2019 sample is "Dance Monkey" by Tones and I and the top song in our 2020 sample is "positions" by Ariana Grande. 


## _**Methodology**_

After compiling our data into Excel sheets, we ran descriptive statistics utilising Excel’s features. We calculated the mean, medium, maximum and minimum values as well as standard deviation on the audio features we selected I.e. tempo, valence, danceability, energy, loudness & speechiness for the time period of 2018-2021. 


<img width="1187" alt="Screen Shot 2022-01-14 at 4 39 13 PM" src="https://user-images.githubusercontent.com/91945641/149551922-2332e0e1-4419-4800-bb34-6de6d580825b.png">
<p align="center"><em> Table: Descriptive statistics of audio features for 2018-2020 </em></p>

<p align="center"><img width="1117" alt="Screen Shot 2022-01-13 at 12 34 25 PM" src="https://user-images.githubusercontent.com/91945641/149331116-adc7d7b0-434d-47df-8ed0-b9eea649ea66.png"></p>

<p align="center"><em> Table: Boxplots visualising descriptive statistics </em></p>

By looking at the values, there is a story emerging. The mean, median and standard deviation of tempo, energy and valence increases steadily between 2018 and 2021. This means that your favourite top songs, on average, are more likely to exhibit musical positivity, upbeat rhythms and energy over the years. However, the range of values of these audio features of top songs also expands over the years.

Conversely, the descriptive statistical values for danceability and loudness decreases steadily between 2018 and 2021. This means that your favourite mainstream song is potentially less loud and dancelike and most top songs have similar range of lower danceability and loudness over the years. This contradicts the media article’s assumption that songs rise in danceability over the years. 

The next step would be to investigate whether there is any relationship between the audio features that increase or decrease respectively. To do so, we exported this excel sheet into Stata and R respectively for data analysis. 
	
In order to study the relationship between a track’s position and its audio features, we turned to Stata to use a Simple Linear Regression (SLR) model. Regressions are used to determine the relationship between two or more variables, and quantitatively analyse how one variable changes when the other changes. We want to understand whether certain values of audio features will place a track higher or lower on the list. When these values change, we want to see whether their placement changes as well. 

In order to study the relationships between audio features, we used multiple regression analysis (MLR). MLR allows us to test relationships between multiple independent variables and a single dependent variable. For instance, we can test the direction and strength of relationship between danceability (dependent) with tempo, energy, valence, loudness i.e. all audio features. And we did! We constructed multiple MLR relationships to define each audio feature as y and rest as x. Our purpose was to get a full combination of every single relationship possible. Usually multiple factors affect song production in real life: None can make a song with just a single audio feature. Testing relationships allow us to explore common themes and interesting threads of popular music.


### Visualising Each Year’s Mean Values 

<p align="center"><img width="450" alt="WhatsApp Image 2022-01-13 at 9 32 57 AM" src="https://user-images.githubusercontent.com/91945641/149321816-ec868527-7174-4c2d-a9ec-d180605a53e9.jpeg"></p>

<p align="center"><em>Table: Overlapped radar charts of mean audio features</em></p>

The chart is an overlap of radar charts depciting mean values of four audio features - energy, speechiness, danceability, valence -  over four years, 2018 to 2021. As you can see, there is some overlap between the audio features since the radar charts have similar shapes. This entails that on average, the top songs have similar levels of energy, speechiness, danceability and valence to an extent. 


## _**Results**_

As illustrated above, the top 2 songs of two different years have drastically different makeup of audio features. However, they share a similarity of high danceability. Upon discovering this, we examined whether we can predict a track’s placement on the top 25 by its audio features.


### Simple Linear Regression (SLR) 


With the Simple Linear Regression approach, we estimate the following equation:


<p align="center"><img width="630" alt="Screenshot 2022-01-12 at 18 04 00" src="https://user-images.githubusercontent.com/92088621/149196699-d34068b1-e9ea-49d1-b9e2-9435a66ebcd9.png"></p>

The track’s position is the dependent (y) variable, and danceability is the independent (x) variable. β0 is the constant, ie. what is the track’s position when danceability equals 0. For the purposes of our project, we disregard β0. β1 serves as the coefficient in front of danceability. In other words, when the danceability increases by 1 unit, by how much does a track shift up on the charts. Ei serves as the error term for our equation, accounting for any confounding factors or errors in our estimation. 

<p align="center"><img width="839" alt="Screenshot 2022-01-12 at 17 43 58" src="https://user-images.githubusercontent.com/92088621/149193693-03c26b38-f3e6-42ad-926e-aa29ac8b0515.png"></p>

Table 1 shows the Simple Linear Regression with our main explanatory variable, danceability, on chart placement. We find that at an aggregate level, danceability has a negative relationship with a track’s chart placement. A one unit increase in danceability is estimated to shift a track up by 8 positions on the top charts(in this case, a lower number, for example 1 or 2, translates to a higher position). A higher danceability value is associated with a higher placement on the charts. However, this coefficient is not statistically significant, ie. the results are likely to occur by chance. We wanted to examine how the 4 different years contributed to this coefficient, thus we broke it down in the following columns. 

In column 2, it is shown that if a 2018 song has a high danceability value, it means that it is positively correlated with their position on the charts. However, this coefficient is not statistically significant. This relationship is also apparent in column 3 with 2019 tracks and 2019 positions.

In column 4, it is seen that if a song has a high danceability value, it is negatively associated with their position on the charts. Its coefficient is statistically significant at the 5% level; the results are not easily explained by chance alone. The same relationship and same statistical significance applies in column 5 with 2021 tracks and positions. 

On one hand, we obtained two years with positive coefficients. On the other hand, we obtained two years with negative coefficients. This leads to our negative coefficient in column 1 with no statistical significance overall. 

We observed that the relationship between positions and audio features fluctuate within each year between positive and negative, large and small coefficients. We continued to conduct SLR with other audio features against positions, such as valence and energy, but found danceability to have the most statistically significant results. Consistent with our findings, music is abstract; what makes a song popular has multiple confounding factors.


### Multiple Linear Regression

<img width="464" alt="Screen Shot 2022-01-14 at 6 34 27 PM" src="https://user-images.githubusercontent.com/91945641/149567365-7320f01e-3b07-4dcd-9cc2-37ca9912f38e.png">

<p align="center"><em>Table: Meaningful Multiple Regression Results</em></p>

Here the table shows the results of meaningful multiple regression results. By meaningful, we mean results which generally have only around 10% chance of being a random error. While statisticians tend to hold only 5% error and we have upheld that principal for SLR results, our sample size is quite limited and the time period for our data collection is very specific. Therefore we recognise that extending error rate can allow us to look at more relationships that may have been statistically significant i,.e. P value les than 0.05, if sample size and time period for the data collection was wider. 

The estimate indicates the strength and direction of the relationship. Here all the relationships are positive. An estimate of 0.49 between energy and danceability in 2018 means that if energy increases by 1 unit, danceability increases by 0.49 unit. The estimates that are 0 are ones that have very negligible non-zero increases in unit. Thus, while the relationships vary in strength and statistical significance, some common themes emerge over the years. 

Moreover, both energy and tempo have a meaningful relationship with valence in 2019 and the meaningful relationship between tempo and valence continues in 2020 while tempo and energy have a positive meaningful relationship in 2020 and 2021. This provides a more nuanced look into the nature of these audio features which seemed to increase in mean between 2018 and 2021 according to the descriptive statistics. 

The simple linear regression analysis on chart positioning only found a statistically significant relationship between danceability and chart position. Hence, it is important to look from the lens of danceability and see if it has meaningful relationships with other audio features. Here we can see that energy and danceability have a positive meaningful relationship in 2018 and 2021. Valence has a positive meaningful relationship with danceability in 2019 and 2020 while tempo has a positive meaningful relationship with danceability in 2019, 2020 and 2021. 


<p align="center"><img width="1102" alt="Screen Shot 2022-01-14 at 4 41 28 PM" src="https://user-images.githubusercontent.com/91945641/149552223-40cc2e5a-4959-4a6a-9aa0-96b392c03b5c.png"></p>
<p align="center"><em>Table: Scattter plots</em></p>


The above are two scatter plots displayed of two meaningful relationships in two different years. The two plots are depicted to show the common themes, as bullet-pointed below, that are shared by scatter plots depicting all the meaningful relationships that were discovered:


1.	The points in the scatter plot are widely dispersed and there is a lot of variance. This makes it difficult to establish a meaningful relationship between the variables. 
2.	The outliers are marked by their respective album covers. There are a lot of outliers which means even if there is a meaningful relationship there a considerable number of songs that do not fit the mold. Hence, it is difficult to generalize thousands of songs that are released every year or even the hundreds of songs that can become well-known or top hits. 


## Conclusion 

Our objective was to explore whether we can predict song popularity through a song's audio features. As a group, we kept asking ourselves, “what makes a song popular?” We analysed the relationship between a track's position on the charts and their danceability value. Although we found an overall negative relationship, we found mixed results when we divided up the coefficient by year. With two years of negative coefficients and two years of positive coefficients, there is not a clear answer on if there is a stable relationship between the two variables. 

We also analysed whether there are any meangingful relationships between audio features. Given that the SLR results found a statistically signifcant relationship between chart positioning and danceability, it is important to note that danceability and tempo had a meaningful relationship between 2019 and 2021 while valence had a meanginful relationship between 2019 and 2020 and energy in 2018 with danceability respectively. Therefore during these years, songs that were most streamed by the average person had high danceability cressponding with high tempo and valence. This formula could guarantee a viral hit song to an extent and may do so in the future.  

However, these relationships are not everlasting neither can they be generalised to all music given our very limited sample size. Firstly, as scatter plots have depicted, there is a lot of spread and outliers. Secondly, music is a subjective concept. It makes sense that there is no set pattern, no defining audio features, and no similar songs. All songs are different and all tastes are different. People may listen to a song because they like the lyrics. Or, someone may like the artist or the producer. Perhaps, someone likes the genre placement. After all, most people have a short attention span with music – they get bored of the same song repeatedly. These reasons mean that Spotify’s algorithm for determining audio features cannot tell us what we wanted to hear. There are other factors that make music popular, which cannot be studied through our data analysis. 

To list them, other factors influencing a song's popularity is lyrics, previous work/popularity, genre placement, the level of innovation/originality, and the abstract aspect of making music. 

<p align="center"><img width="393" alt="pie chart" src="https://user-images.githubusercontent.com/91847452/149546451-7538db67-2034-4ea1-b8be-1fa315ee1a41.PNG"></p>

<p align="center"><em>Image Source: Nielsen Music, 2015</em></p>

It is important to refer to the limitations we have faced that require further research. First of all, we analysed the top 25 most globally streamed songs for our research. If we were to evaluate a specific country’s top 25 most streamed songs, we might have gotten different results. Secondly, we analysed a small sample of songs from a short period of time. We only looked over the top 25 songs from 4 consecutive years: 2018, 2019, 2020 and 2021. Next, with the wide presence of social media, song popularity can be altered according to the social influence we receive. According to Pachet, “[k]nowing that a song is a hit…influences our liking” (2012). One social media platform that comes to mind is TikTok. We noticed that the majority of songs we analyzed are (or were at one point) widely used songs on TikTok. Lastly, a change of website where we acquired our data might cause different results. There are other websites such as Billboard that also provide the same type of data. With these limitations in place, our result is that it is not possible to fully predict song popularity. Moving forward, further research is needed to eliminate the limitations mentioned above. 


## Appendix 

[Spotipy Project Stata Code.pdf](https://github.com/sdito000/Spotipydataproject/files/7870044/Spotipy.Project.Stata.Code.pdf)

[R Analysis.pdf](https://github.com/sdito000/Spotipydataproject/files/7870171/R.Analysis.pdf)


## References 

[Ferreri et al. (2019)](https://www.pnas.org/content/116/9/3793)

[Pachet & Roy (2018)](https://www.researchgate.net/publication/220723429_Hit_Song_Science_Is_Not_Yet_a_Science)

[Pham et al. (2015)](https://www.semanticscholar.org/paper/Predicting-Song-Popularity-Pham/3a4d3e9dcb8ea421afb92903e1e4e5dd31861b7b)

[Spotify Web API: Get Audio Features](https://developer.spotify.com/documentation/web-api/reference/#/operations/get-audio-features)


## Thanks for listening!
