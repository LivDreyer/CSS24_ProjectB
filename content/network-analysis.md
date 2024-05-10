---
title: Network analysis
prev: data-description
next: text-analysis
---

The purpose of the network analysis is to highlight the underlying mechanism of the Spotify Network and tendencies between artists when they collaborate with each other.

*Degree Distribution:* This analysis of the degree distribution, comparing our artists collaboration network to a random mirroring network, shows that the real network of artist collaborations exhibits non-random patterns, meaning artists are not connected purely by chance.

*Assortativity:* There was found no major indications that popularity was correlated with a higher number of features. However, it seemed that the network was assortative, as the network had a clear tendency to have high-degree nodes connect with high-degree nodes i.e. artists with many features would be more likely to collaborate with other artists that had a lot of features. Conversely, artists with few features would also be more likely to collaborate with other artists that also did not have many features.so

*Centrality:* It was found, based on closeness centrality, that artists of the type DJ/Producers were very central, as they inherently collaborate with a lot of different artists. Moreover, artists that were bilingual, i.e. produced music to a wider audience, were also central to the network, as they could connect different communities.

*Community:* The analysis discovered a correlation between genres and the communities, but that a perfect partition could not solely be made based on genres, and a more thorough partition would involve nationalities of the artists. Moreover, it was found with the use of the Louvain method that there is no perfect partition of the network without any overlaps.

Overall, the graph analysis gave many valuable insights into the Spotify Network, some of them being expected but also others being unexpected.

![](/images/network.png)
<p style="text-align: center;">Figure 2: Artist Collaboration Network genre-coded by color.</p>

The analysis resulted in unexpected discoveries; artists would be more central to the network if they produced music in more languages than one, because then they would connect different communities. This makes a lot of sense, but something that was not thought about before the analysis was carried out.  A point to raise in relation to the aforementioned, maybe the communities are a bit misleading, as some of the genres may refer more to nationalities than actual music genres. This was without a doubt a shortcoming of the analysis, as it maybe would have been more insightful to also compare the partition of countries/nationalities with that of genres. The current community analysis could be a bit speculative, because such a partition is missing. 

Contrarily, one of the project's weakest points is that it very rudimentarily categorizes less popular genres into more popular genres. Here the project could have used k-means or other clustering methods that would create more robust results. In relation to this, the “other” genre has not been addressed much in the analysis, but this was a genre that contained all other genres which was not easily classified with the rename genres function. Therefore, many improvements could have been made to the classifications of genres. But as scientific papers are being made solely on the use of Machine Learning to classify music genres of songs, it was accepted that the classification of genres to be rather rudimentary - considering the scope of the project. 

> If you want to dive deeper into how we performed our analyses, visit our [Explainer Notebook](ProjectB_final1.html)!
