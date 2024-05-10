---
title: Data description
prev: "/"
next: network-analysis
---

To address the research question, "*What is the relationship between artist collaboration patterns, popularity, and lyrical expression of genre themes?*", acquiring comprehensive data on artists is essential.

<div style="text-align: center;">
    <div style="border-top: 3px solid #22c55e; margin-bottom: 10px;"></div>
    <a href="https://docs.genius.com" style="margin-right: 60px; display: inline-block;"><img src="/images/genius-logo.webp" alt="Genius Lyrics" width="110" height="110" style="border-radius: 10px;"></a>
    <a href="https://developer.spotify.com/documentation/web-api" style="margin-right: 60px; display: inline-block;"><img src="/images/spotify-logo.png" alt="Spotify" width="110" height="110" style="border-radius: 10px;"></a>
    <a href="https://www.kaggle.com/datasets/spoorthiuk/us-top-10k-artists-and-their-popular-songs" style="display: inline-block;"><img src="/images/kaggle-logo.webp" alt="Kaggle" width="150" height="150"></a>
    <div style="border-bottom: 3px solid #22c55e; margin-top: 10px;"></div>
</div>
<p style="text-align: center;">Figure 1: Main Data Sources.</p>

We utilize data from APIs such as Spotify and Genius, supplemented by a Kaggle dataset, as the cornerstone of our analyses. This data collection process resembles a "chain reaction", where Kaggle's "*US Top 10K Artists and Their Popular Songs*" dataset serves as the starting point. From there, we access the Spotify API to enrich the dataset with artist information, subsequently utilizing the Genius API, within the legal boundaries, to augment the dataset further by webscraping.

# Kaggle 
Kaggle serves as a data science community offering various tools and resources for researchers and scientists. This analysis utilizes a ["US Top 10K Artists and Their Popular Songs"](https://www.kaggle.com/datasets/spoorthiuk/us-top-10k-artists-and-their-popular-songs), a dataset created by Spoorthi Uday Karakaraddi. This dataset offers a comprehensive collection of the top 10 popular songs for each of the 10,000 most-listened-to artists in the United States as of 2023, but due to the Spotify API rate limit, we are only using the top 4250 artists from the dataset.

We focus solely on the file containing artist information and their associated attributes:

| Name          | ID                    | Genres                                            | Popularity | Followers |
|---------------|-----------------------|---------------------------------------------------|------------|-----------|
| Drake         | 3TVXtAsR1Inumwj472S9r4 | ['canadian hip hop', 'canadian pop', 'hip hop', 'pop rap', 'rap'] | 95         | 83,298,497|
| Post Malone   | 246dkjvS1zLTtiykXe5h60 | ['dfw rap', 'melodic rap', 'pop', 'rap']          | 86         | 43,130,108|
| ...           | ...                   | ...                                               | ...        | ...       |
| Pitbull       | 0TnOYISbd1XYRBk9myaseg | ['dance pop', 'miami hip hop', 'pop']             | 80         | 10,383,655|


# Spotify API
- Spotify API general info, incl. rate limit free version, owner, rights etc.

We iteratively query the Spotify API to construct our dataset for network and textual analyses. Beginning with the Kaggle dataset, we collect the top 10 most popular tracks for each artist on Spotify. We then utilize this information to identify collaborations and query the Spotify API for the top 10 tracks of featured artists. Due to the API rate limit and project scope, we cap our dataset at approximately 14,000 artists, comprising the initial 4250 artists and those featured on their top tracks. This is visualized in Figure 2.

{{< figure src="/images/FP-explainer.png" width="700" alt="explainer" class="center" >}}
<p style="text-align: center;">Figure 2: Visual representation of data collected from the Spotify API.</p>

Our dataset resulting from querying the Spotify API now consists of 14,888 rows. Each row represents an artist with the following important attributes: *Main Artist*, *Names of Top 10 Songs*, *Main Artist ID*, *Genres associated with Main Artist*, *Popularity*, *Followers*. 

### Artist Information

<table>
  <tr>
    <td style="padding-right: 10px;">Main Artist</td>
    <td style="padding-right: 10px;">Song Names (10)</td>
    <td style="padding-right: 10px;">Genres</td>
    <td style="padding-right: 10px;">Popularity</td>
    <td style="padding-right: 10px;">Followers</td>
    <td>ID</td>
  </tr>
  <tr>
    <td>A Tribe Called Quest</td>
    <td>['Can I Kick It?', <br>..., <br>'Check the Rhime']</td>
    <td>[conscious hip hop,<br>east coast hip hop,<br>golden age hip hop,<br>hip hop,<br>jazz rap,<br>queens hip hop]</td>
    <td>67</td>
    <td>2,081,598</td>
    <td>09hVIj6vWgoCDtT03h8ZCa</td>
  </tr>
  <tr>
    <td>Bruno Mars</td>
    <td>['Locked out of heaven', <br>..., <br>'Grenade']</td>
    <td>[dance pop, pop]</td>
    <td>89</td>
    <td>54,550,331</td>
    <td>0du5cEVh5yTK9QJze8zA0C</td>
  </tr>
  <tr>
    <td>...</td>
    <td>...</td>
    <td>...</td>
    <td>...</td>
    <td>...</td>
    <td>...</td>
  </tr>
  <tr>
    <td>DJ Khaled</td>
    <td>['GREECE (feat. Drake)', <br>..., <br>'POPSTAR (feat. Drake)']</td>
    <td>[hip hop, <br>miami hip hop, <br>pop rap, rap]</td>
    <td>75</td>
    <td>11,185,726</td>
    <td>0QHgL1lAIqAw0HtD7YldmP</td>
  </tr>
</table>


This dataframes constructed throughout our data collection from the Spotify API, are used for both the network analysis, and to furthermore collect data from the Genius API. Through the top 10 tracks of each artist, we find the names of their collaborators, and use this information for creating our network. How we use it for the textual analysis will be introduced in the next section! 

# Genius 
- Genius API general info, incl. rate limit free version, owner, rights etc.
- How and what are we webscraping using results from Spotify API? 
- Basic description of dataset (attributes, rows, MB).
- Include example table of above.

> Example of song 1

> Example of song 2

> Example of song 3

<img src="/images/dtu-logo.png" width="200" />

- Short intro to what we are using it for (motivation 1 sentence, mention text analysis)
