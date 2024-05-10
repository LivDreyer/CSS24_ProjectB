---
title: Text analysis
prev: network-analysis
---

{{< figure src="/images/spotifycode.png" width="350" alt="explainer" class="center" >}}
<p style="text-align: center;">If you would like to listen to a playlist of the 1000 songs used, scan this code with your Spotify app!</p>

## Motivation for analysis 

Textual analysis of song lyrics is used in our project to investigate distinctive themes and language patterns across different genres. This approach is interesting for several reasons:

**Genre-Specific Themes:** We would like to see if it is possible to identify genre-specific characteristics/themes. Analyzing these differences should help to define what sets the genres apart.

**Comparative Analysis:** By looking into the frequency and context of words within genres, we can identify which themes and words are predominant for each genre. This analysis helps shed light on what characterizes the different genres.

## Analysis 
We begin our analysis by cleaning the dataset, using regular expressions to ensure the text data is ready for analysis. Language detection algorithms identify the primary language of each song's lyrics, which is useful for accurate genre-specific analysis.
We use TF-IDF analysis to highlight distinctive words in each genre’s lyrics, helping to pinpoint unique themes. Additionally, wordclouds visually represent these themes, offering an immediate understanding of the most prevalent words across genres. This approach allows us to understand the unique identifiers of the genres and what characterises each genre, some more than others.

### Word Clouds:
If we choose to look at a few specific word clouds for a subset of the genres as it becomes easier to see the distinctiveness of each genre and why we consider the wordclouds a success.

![](/images/wordclouds.png)
<p style="text-align: center;">Figure 5: The result of our textual analysis formatted in wordclouds.</p>

*Country genre:* This word cloud emphasizes emotions and rural life with words like “love”, “heart” and “gon ride”.

*Electronic genre:* This word cloud highlights words such as “dance”, “night”, “beat” showcasing a focus on the “club life” and dancing which is especially characteristic of the electronic genre.

*Hip Hop genre:* The hip hop genre is perhaps the most easily identifiable word cloud with words such as “bitch”, “money”, “fuck”, and another racially motivated word. This highlights the confrontational and wealth-focused nature of the Hip Hop genre.

### TF-IDF 
This part of the textual analysis shows generally the same as the word clouds which just builds on our insights from the word clouds and confirms our findings of the characteristics of each genre being more or less easily identifiable. 

Through our text analysis using tools such as TF-IDF analysis and word clouds, we have gained insights into the distinctive themes and characteristics of different music genres. Our approach allowed us to clean and analyze the dataset efficiently, identifying unique characteristics for each genre. The word clouds provided visual representations of prevalent words, offering immediate insights into genre-specific themes. Similarly, TF-IDF analysis further confirmed our findings, reinforcing the uniqueness of each genre. Overall, our analysis highlights the importance of textual analysis in understanding the nature of music genres and their thematic variations.

## Discussion 
To properly perform an in-depth analysis of the lyrical expression within the previously mentioned non-english genres, it would require knowledge of the languages beyond literal translations, as removing adverbs and filler words is a crucial part of the TF-IDF analysis and when creating wordclouds. Furthermore, to expand our understanding of lyrical expressions within different genres, we could improve our textual analysis by comparing lyrics of songs where the artist has mixed genres to lyrics of songs where the artist is only associated with a single genre, potentially enlightening how artists work to incorporate their own brand into collaborative works while adjusting some aspects to align with their collaborators. 
