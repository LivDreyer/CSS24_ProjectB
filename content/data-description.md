---
title: Data description
prev: "/"
next: network-analysis
---

## Short introduction to datasets and motivation for using them

Finding data on artists is crucial to answering the research question: *"What is the relationship between artist collaboration patterns, popularity, and lyrical expression of genre themes?"*. 

<div style="text-align: center;">
    <div style="border-top: 3px solid #22c55e; margin-bottom: 10px;"></div>
    <a href="https://docs.genius.com" style="margin-right: 60px; display: inline-block;"><img src="/images/genius-logo.webp" alt="Genius Lyrics" width="110" height="110" style="border-radius: 10px;"></a>
    <a href="https://developer.spotify.com/documentation/web-api" style="margin-right: 60px; display: inline-block;"><img src="/images/spotify-logo.png" alt="Spotify" width="110" height="110" style="border-radius: 10px;"></a>
    <a href="https://www.kaggle.com/datasets/spoorthiuk/us-top-10k-artists-and-their-popular-songs" style="display: inline-block;"><img src="/images/kaggle-logo.webp" alt="Kaggle" width="150" height="150"></a>
    <div style="border-bottom: 3px solid #22c55e; margin-top: 10px;"></div>
</div>

Data from API's such as the Spotify API and the Genius Lyrics API alongside addtional data from Kaggle will act as the foundation for the analysis that will hopefully lead to our enlightenment on the above research question. Collecting all data used for this project bears sign of a "chain-reaction". The dataset "US Top 10K Artists and Their Popular Songs" from Kaggle created a foundation for fetching data from the Spotify API, that then allowed for fetching data from the Genius Lyrics API which was then used for webscraping within the legal limits of Genius Lyrics.  

## Kaggle 
Kaggle serves as a data science community offering various tools and resources for researchers and scientists. This analysis utilizes a [dataset](https://www.kaggle.com/datasets/spoorthiuk/us-top-10k-artists-and-their-popular-songs) created by Spoorthi Uday Karakaraddi and it provides "*a comprehensive collection of the top 10 popular songs for each of the 10,000 most-listened-to artists in the United States*" from 2023.

This project only utilize...

- Basic description of dataset (attributes, rows, MB).
- Include example table of above.

## Spotify API
- Spotify API general info, incl. rate limit free version, owner, rights etc.
- How are we pulling from the API using Kaggle? Explain how many features we are including (refer to figure 1).
- Basic description of dataset (attributes, rows, MB).
- Include example table of above.
- Short intro to what we are using it for (motivation 1 sentence, mention network analysis) 

## Genius 
- Genius API general info, incl. rate limit free version, owner, rights etc.
- How and what are we webscraping using results from Spotify API? 
- Basic description of dataset (attributes, rows, MB).
- Include example table of above.

> Example of song 1

> Example of song 2

> Example of song 3

<img src="/images/dtu-logo.png" width="200" />

- Short intro to what we are using it for (motivation 1 sentence, mention text analysis)
