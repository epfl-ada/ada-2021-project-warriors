# The American Political Landscape : Polarization between the Left and Right-wing

## Abstract
Political polarization, as defined in Wikipedia, is the extent to which opinions on an issue are opposed. It is assumed that polarization in the world in general, and in the US in particular, has been increasing over the past years. But, is it really the case? Has the polarization been always increasing over past years? In this project, we suggest a data-driven approach to quantify the polarization, and observe how it evolves over time. We explore the possibility of defining a similarity measure between politicians based on their quotes. Once we do this, we would like to study the difference between different political ideologies (mainly left and right) in order to see if there is a significant difference in their quotes.

## Research Questions
1. What are the main topics discussed by politicians ?
2. Does this quote dataset show the differences and contrasts between right-wing and left-wing politicians ?
3. How to define a similarity between politicians ? Can we derive such a measure of similarity ?
4. Clustering the speakers based on this measure, do these clusters match with the ideological left/right separation ? 
5. Through time, how the distance between these clusters evolve ? Can we relate this evolution to some major historic events ?

## Additional Datasets

[Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page). This database provides additional features about the politicians.

## Methods


First, as we were dealing with a huge file from Quotebank, our first objective was to filter it in order to keep only the useful data, and to have a data in a manageable size. For this purpose, we decided to remove the following features : Proba, phase, URLs, etc.(non-exhaustive list). As our interest was only about politicians, we filtered out all the quotes which were not written by politicians. To do so, we used the additional dataframe Wikidata for which more details are given below. 


In order to enrich our dataset, we decided to fetch the data from the additional dataset Wikidata. The objective was to get the country, the occupation, the political party, and the academic degree of each quotation’s speaker. This was maybe the most challenging part of the preprocessing, as we had to find a solution which does not lead to a huge runtime. The first option considered was to use the API of Wikidata, using the QwikiData library. Unfortunately, even though it was a feasible solution in theory, this was leading to an unfeasible runtime (many hours). The second option (also not feasible) was based on a merge of the data frames ( from Wikidata and QuoteBank).  The third (and last) one was based on the observation that qIDs were unique values, and could then be considered as an index. This solution produced the correct solution within only a few minutes. In order to show that it was working properly, the code printed a periodic feedback (every 10^5 quotes read). We then kept only the politicians, as it was the only need of our topic. That way, this enabled to filter out the quotes which were not related to a politician, as mentioned above. Other difficulties were met, namely when finding many ids for one speaker. In order to fix that, we considered only the first id. 
  

Finally, in order to get a better understanding of the data, we decided to do some visualisation. We started to plot the distribution of the political parties over the speakers, along with some ratios. For example, we found the percentage of American and non-American politicians in our data, which reinforced our choice of studying politicians in the USA. 

**Milestone 3**
We first tried to define a measure of closeness between the quotes, we tried to work with the Glove Model and use PCA to get a 2D visualisation but this tured out not to work so well.
We  finally used LDA model to analyse the quotes after preprocessing them(removing punctuation, lower casing, removing stopwords, Lemmatization), this gave us the 20 most important topics, after assigning a topic to each quote, we analysed the sentiments of the quotes for specific topics that we found pertinent.
We compared these sentiments between Democrats and republicans, and checked if their distributions and statistically different.
We also analysed the importance accorded to the topics by republicans and democrats throught the percentage of the quotes regarding those topics.
Link to generated Datasets: https://drive.google.com/drive/folders/1YEFlg6c92JPaKHY6pdl7OYabeDIW5cpf?usp=sharing

## Timeline 
* 19 Novembre : Explore the different NLP techniques and choose a similarity metric based on that.
* 26 Novembre : Apply the NLP and the clustering.
* 3 Decembre : Distance evolution through time between these clusters.
* 10 Decembre  : Educational degree analysis.
* 15 Decembre : Internal deadline, feedback and last updates.

## Team Organization 

We do most of the work as a team but we still defined some task manager: 
* Aya Rahmoun :  NLP techniques explorations, and NLP Analysis.
* Abdeslam Guessous : Clustering after having defined the appropriate similarity measure. 
* Louay Najar : Analysis of evolution through time and comparison to events.
* Mortadha Abderrahim : NLP Implementation and general review.
