---
title: Data description
prev: "/"
next: network-analysis
---

Finding data on artists is crucial to answering the research question: *"What is the relationship between artist collaboration patterns, popularity, and lyrical expression of genre themes?"*. 

<div style="text-align: center;">
    <div style="border-top: 3px solid #22c55e; margin-bottom: 10px;"></div>
    <a href="https://docs.genius.com" style="margin-right: 60px; display: inline-block;"><img src="/images/genius-logo.webp" alt="Genius Lyrics" width="110" height="110" style="border-radius: 10px;"></a>
    <a href="https://developer.spotify.com/documentation/web-api" style="margin-right: 60px; display: inline-block;"><img src="/images/spotify-logo.png" alt="Spotify" width="110" height="110" style="border-radius: 10px;"></a>
    <a href="https://www.kaggle.com/datasets/spoorthiuk/us-top-10k-artists-and-their-popular-songs" style="display: inline-block;"><img src="/images/kaggle-logo.webp" alt="Kaggle" width="150" height="150"></a>
    <div style="border-bottom: 3px solid #22c55e; margin-top: 10px;"></div>
</div>

Data from API's such as the Spotify API and the Genius Lyrics API alongside addtional data from Kaggle will act as the foundation for the analyses. Collecting all data used for this project bears sign of a "chain-reaction". The dataset "US Top 10K Artists and Their Popular Songs" from Kaggle created a foundation for fetching data from the Spotify API, that then allowed for fetching data from the Genius Lyrics API which was then used for webscraping within the legal limits of Genius Lyrics.  

# Kaggle 
Kaggle serves as a data science community offering various tools and resources for researchers and scientists. This analysis utilizes a ["US Top 10K Artists and Their Popular Songs"](https://www.kaggle.com/datasets/spoorthiuk/us-top-10k-artists-and-their-popular-songs), a dataset created by Spoorthi Uday Karakaraddi, providing "*a comprehensive collection of the top 10 popular songs for each of the 10,000 most-listened-to artists in the United States*" from 2023.

This project only utilize the file containing the artists and their associated attribute:

| Name          | ID                    | Genres                                            | Popularity | Followers |
|---------------|-----------------------|---------------------------------------------------|------------|-----------|
| Drake         | 3TVXtAsR1Inumwj472S9r4 | ['canadian hip hop', 'canadian pop', 'hip hop', 'pop rap', 'rap'] | 95         | 83,298,497|
| Post Malone   | 246dkjvS1zLTtiykXe5h60 | ['dfw rap', 'melodic rap', 'pop', 'rap']          | 86         | 43,130,108|
| ...           | ...                   | ...                                               | ...        | ...       |
| Pitbull       | 0TnOYISbd1XYRBk9myaseg | ['dance pop', 'miami hip hop', 'pop']             | 80         | 10,383,655|

We are only using the top 4250 artists from the dataset due to the rate limit of the Spotify API, which will be introduced in the next section.

# Spotify API
- Spotify API general info, incl. rate limit free version, owner, rights etc.

Taking our starting point in the "US Top 10K Artists and Their Popular Songs"-dataset, we query the Spotify API a multitude of times to construct the dataset for our network analysis and textual analysis. Using the Artists from the Kaggle dataset to collect their top 10 most popular tracks on Spotify, we find their collaborations. We then query the Spotify API for the top 10 tracks of the featured artists to find their possible collaborations. While its possible to expand our dataset to include more artists, we will cap the dataset at the 4250 artists collected from the Kaggle dataset (iteration 1) and the artists featured on their top 10 tracks (iteration 2) totalling around 14000 artists in total. This is largely due to the rate limit of the Spotify API and the scope of this project. This means that artists featured on songs by artists found in the second iteration who are not already a part of either iteration 1 or 2 will not be included in the dataset. This is visualized in Figure 2.

{{< figure src="/images/FP-explainer.png" width="700" alt="explainer" class="center" >}}
<p style="text-align: center;">Figure 2: Visual representation of data collected from the Spotify API.</p>

Our dataset resulting from querying the Spotify API now consists of 14888 rows. Each row represents an artist, and has the following important attributes: *Main Artist*, *Names of Top 10 Songs*, *Main Artist ID*, *Genres associated with Main Artist*, *Popularity*, *Followers*. 

| Main Artist           | Song Names                                       | Genres                                                                         | Popularity | Followers | ID                 |
|-----------------------|--------------------------------------------------|--------------------------------------------------------------------------------|------------|-----------|--------------------|
| A Tribe Called Quest | ['Can I Kick It?', ..., 'Check the Rhime']       | [conscious hip hop, <br>east coast hip hop, <br>golden age hip hop, <br>hip hop, <br>jazz rap, <br>queens hip hop] | 67         | 2,081,598 | 09hVIj6vWgoCDtT03h8ZCa |

- Basic description of dataset (attributes, rows, MB).
- Include example table of above.
- Short intro to what we are using it for (motivation 1 sentence, mention network analysis) 

<table>
  <tr>
    <td style="padding-right: 10px;">Main Artist</td>
    <td style="padding-right: 10px;">Song Names</td>
    <td style="padding-right: 10px;">Genres</td>
    <td style="padding-right: 10px;">Popularity</td>
    <td style="padding-right: 10px;">Followers</td>
    <td>ID</td>
  </tr>
  <tr>
    <td>A Tribe Called Quest</td>
    <td>['Can I Kick It?', ..., 'Check the Rhime']</td>
    <td>[conscious hip hop,<br>east coast hip hop,<br>golden age hip hop,<br>hip hop,<br>jazz rap,<br>queens hip hop]</td>
    <td>67</td>
    <td>2,081,598</td>
    <td>09hVIj6vWgoCDtT03h8ZCa</td>
  </tr>
</table>




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
