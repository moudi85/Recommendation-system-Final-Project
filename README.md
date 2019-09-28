# Play My Next Song
## Recommending Spotify songs 
### Project Aim: 

Today,  online music streaming has become the dominant platform for people to listen to their favorite songs, music streaming services are now able to collect large amounts of data on the listening habits of their customers. These streaming services, like Spotify, Apple Music or Pandora, are using this data to provide recommendations to their listeners. These music recommendation systems are the part of a broader class of recommender systems, which filter information to predict a user’s preferences when it comes to a certain item.

Current music recommender systems use user-generated meta-data, such as previous purchases and listening history, as the basis for the recommendations. However, such metadata-based systems cannot recommend artists or songs for which there is no data available (i.e., new songs or artists). This ”cold start” problem has made researchers focus on improving content-based recommender systems, which use audio features extracted automatically from the audio content as the basis for recommendations.

In this project, I will show how to use both Spotify API Metadata and audio features data to recommend songs using Content-Based Filtering recommendation. Content-based filtering algorithms are given user preferences for items and recommend similar items based on a domain-specific notion of item content. This approach also extends naturally to cases where item metadata is available (In our case music genres).
I closely examine the actual item to determine which features, in my opinion, are most important in making recommendations and how those features interact with the user’s preferences. Data collection can be much more complicated in content-based filtering as it is very difficult to select which features of an item will be important in creating some sort of predictive model.

## Repository Contents

#### [Data Collection](https://github.com/moudi85/Music-Recommender-/blob/master/README.md#data-collection-1)
#### [Exploratory Data Analysis](https://github.com/moudi85/Music-Recommender-/blob/master/README.md#exploratory-data-analysis-1) 
#### [Content-Based Filtering](https://github.com/moudi85/Music-Recommender-/blob/master/README.md#content-based-filtering-model-1) [[Model](https://github.com/moudi85/Music-Recommender-/blob/master/README.md#content-based-filtering-model-1)]
#### Songs Input

### Data Collection 
Using Spotify API, I acquired 10,000 data points from year 2018. I also obtained the audio features of that dataset, then I merged both data for the final dataframe. Of the total audio features, I decided to pick three features that have an impact on the mood of the user ( Danceability, Valence and Energy). They will be later used as my independent variables, in addition, to (Popularity). I must note that this choice was based on a personal taste and it might be different from person to perosn.

### Exploratory Data Analysis

![Optional Text](https://github.com/moudi85/Music-Recommender-/blob/master/Images/Genres%20distribution%20.png)
Of all genres I decided to group them into 12 genre categories [Pop, Rap, Hip Hop, Rock ,House ,R&B ,Indie ,Country ,Latin ,Metal ,Folk ,Blues]. Since my objective was to make recommendations based on artists genres.

![Optional Text](https://github.com/moudi85/Music-Recommender-/blob/master/Images/Genres%20Distributions%20.png)

I aslo converted "Popularity" variable into three classifications [Unpopular = 0 , Popular = 1 , Very Popular = 2]

![Optional Text](https://github.com/moudi85/Music-Recommender-/blob/master/Images/Artist%20Popularity%20.png)

Most pouplar singer based on my data was "Post Malone" 
![](https://github.com/moudi85/Music-Recommender-/blob/master/Images/Popular%20artist.png)

### Content-Based Filtering [Model]

Finding and determining what audio contents will be important in a music recommender system, is so difficult and it varies from user to user. Music information retrieval refers to the scientific field of extracting information about music and its audio content based on audio signal processing and using that information to make meaningful conclusions about a music item and how it relates to other music. Content-Based filtering closely examines the actual item to determine which features are most important in making recommendations and how those features interact with the user’s preferences. Based on the similarity between the music items and its contents(Genres, Popularity, Energy, Valence, Danceability), we will be able to recommend similar songs to the music inputs for the user.

The Content-Based filtering uses some specific similarity metric, which is Cosine Similarity. Cosine Similarity measures the similarity between two vectors by calculating the cosine of the angle between them. The cosine of a 0-degree angle is 1, therefore the closer to 1 the cosine similarity is; the more similar the items are. 

![](https://github.com/moudi85/Music-Recommender-/blob/master/Images/Cosine%20Similarity%20.png)


### Songs Input

Based on the cosine similarity, 'Boomerang' song closest to my recommendation was ‘Birds' by "Imagine Dragons".

![](https://github.com/moudi85/Music-Recommender-/blob/master/Images/Recommendation.png)







