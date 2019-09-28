# Play My Next Song
## Recommending Spotify songs 
### Project Aim: 
Today online music streaming has becomes the dominant platform for people to listen to their favorite songs, music streaming services are now able to collect large amounts of data on the listening habits of their customers. These streaming services, like Spotify, Apple Music or Pandora, are using this data to provide recommendations to their listeners. These music recommendation systems are part of a broader class of recommender systems, which filter information to predict a user’s preferences when it comes to a certain item. 

Current music recommender systems use user-generated meta-data, such as previous purchases and listening history, as the basis for the recommendations. However, such metadata-based systems cannot recommend artists or songs for which there is no data available (i.e., new songs or artists). This ”cold start” problem has made researchers focus on improving content-based recommender systems, which use audio features extracted automatically from the audio content as the basis for recommendations.

In this project I will show how to use both spotify API Metadata and audio features data to recommend songs using Content-Based Filtering recommendation. I closely examines the actual item to determine which features, in my opinion, are most important in making recommendations and how those features interact with the user’s preferences. Data collection can be much more complicated in content-based filtering as it is very difficult to select which features of an item will be important in creating some sort of predictive model.

## Repository Contents

#### [Data Collection](https://github.com/moudi85/Music-Recommender-/blob/master/README.md#data-collection-1)
#### Exploratory Data Analysis
#### Content-Based Filtering
#### Songs Input

### Data Collection 
Using Spotify API, I acquired 10,000 data points from year 2018. I also obtained the audio features of that dataset, then I merged both data for the final dataframe. Of the total audio features, I decided to pick three features that have an impact on the mood of the user ( Danceability, Valence and Energy). I must note that this choice was based on a personal tatse and it might be different from person to perosn.


### Exploratory Data Analysis

![Optional Text](https://github.com/moudi85/Music-Recommender-/blob/master/Images/Spotifinal%20DF.png)
Of all genres I decided to group them into 12 genre categories [Pop,Rap,Hip Hop,Rock,House,R&B,Indie,Country,Latin,Metal,Folk,Blues]. Since my objective was to make recommendations based on artists genres.

![Optional Text](https://github.com/moudi85/Music-Recommender-/blob/master/Images/Genres%20Distributions%20.png)

I aslo converted "Popularity" variable into three classifications [Unpopular,Popular,Very Popular]

![Optional Text](https://github.com/moudi85/Music-Recommender-/blob/master/Images/Artist%20Popularity%20.png)







