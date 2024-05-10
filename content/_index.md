---
title: The Symphony of Data 
layout: single
next: data-description
---

## Motivation 
Since the 1990’s, the number of songs with featuring artists have increased around 30%. A *featuring artist* is someone who appear as a secondary artist on a song. In 2023, 33 songs out of *Billboards* “Year-End Hot 100 singles” were created by more than one artist. Why is this? When an artist creates a song with one or more featuring artist(s), the featuring artist(s) is (are) essentially “guesting”, contributing their skill and brand to the song and its marketing. When speaking of features, or collaborations, it is often referring to vocals, while it is rarely used in reference to producers, samples, or others contributing to the process of creation in that sense. 

The increase in such music collaborations have inspired researchers to study the success of songs with featuring artists opposed to those without , finding that releasing collaborative songs can increase an artist’s future plays. Furthermore, studies addressing the significance of genres in collaborative music find that greater difference between the genres of collaborating artists increase the likelihood of a song becoming popular. 

This project aims to answer the research question: "*What is the relationship between artist collaboration patterns, popularity, and lyrical expression of genre themes?*" using modern data science methods. 
To answer this question, we center our network analysis around the world’s largest music streaming service: Spotify. Given our project's focus on artist popularity, we employ Spotify for the following reason: With streaming services contributing to 84% of the music industry's revenue, and Spotify holding a dominant market share of 30.5%, the platform offers a comprehensive insight to artist popularity. For those reasons, our project utilizes the [Spotify API](https://developer.spotify.com/documentation/web-api) to gain insights into several aspects of top US artists including artist collaborations, popularity, and top songs. To examine lyrical differences between genres, and in this context artists who may collaborate, we utilize the [Genius API](https://docs.genius.com/#/getting-started-h1) which serve as an "online music encyclopedia" .
This project begins from the Kaggle dataset ["US Top 10K Artists and Their Popular Songs"](https://www.kaggle.com/datasets/spoorthiuk/us-top-10k-artists-and-their-popular-songs). The dataset, created by Spoorthi Uday Karakaraddi, was collected using the Spotify API and features several attributes of the top 10k artists in the US in 2023. It serves as the foundation for constructing the datasets used for network analysis, and the textual analysis.

## [Explainer Notebook](ProjectB.html)

This website will provide an overview of our findings. If you are interested in exploring our data or analyses further, please check out our Explainer Notebook! 
