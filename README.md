# Project Milestone 2 : ada-2021-project-warriors

## Abstract
This paper reports the differences between left and right wing ideologies. They have distinct, and to an extent, contradictory opinions and even have different priorities. However, do their quotes reflect these fundamental disagreements? 
We suggest clustering politicians based on the similarities in their quotes provided in the Quotebank to verify if we can conclude the ideology of a 
quote speaker based on a data-driven approach. Labels from speakers' political ideology on wiki data could be used as the ground truth to assess our classifier. 
Another aspect of this project is the study of the polarization throught the quotes.
Such analysis could provide readers with more insights and background on a quote/text to better understand it and its ideology.

## Research Questions
1. Does this quotes dataset show the differences and contrasts between right wing and left wing politicians ?
2. How to define a similarity between politicians ? Can we derive such a measure of similarity ?
3. According to this definition, do speakers with the same positionning show a higher level of similarity? 
4. Clustering the speakers based on this measure, do these clusters match with the ideologic left/right separation ? 
5. Through time, how the distance between these cluster evolve ? 
6. How does the politicians speech vary depending on the educational degree?

## Additional Datasets



## Methods


First, as we were dealing with a huge file (Quotebank), our first objective was to filter it in order to keep only the useful data, and to have a data in a manageable size. For this purpose, we decided to remove the following features : Proba, phase, urls, etc.(non-exhaustive list). As our interest was only about politicians, we filtered out all the quotes which were not written by politicians. To do so, we used the additional dataframe Wikidata for which more details are given below. 


In order to enrich our dataset, we decided to fetch the data from the additional dataset Wikidata. The objective was to get the country, the occupation, the political party, and the academic degree of each quotation’s speaker. This was maybe the most challenging part of the preprocessing, as we had to find a solution which does not lead to a huge runtime. The first option considered was to use the API of Wikidata, using the QwikiData library. Unfortunately, even tough it was a feasible solution in theory, this was leading to unfeasible runtime (many hours). The second option (also not feasible) was based on a merge of the data frames ( from Wikidata and QuoteBank).  The third (and last) one was based on the observation that qIDs were unique values, and could then be considered as an index. We then kept only the politicians, as it was the only need of our topic. That way, this enabled to filter out the quotes which were not related to a politician, as mentioned above.  

Finaly, in order to get closer to the data, we decided to do some visualisation , namely the distribution of the political parties over the quoters, and some statistical .


Having the preprocessing step, we will now use Natural Language Processing (NLP) to extract information from the quotes. After this, we will cluster the quotes in order to see if we get different clusters for left and right wings or, on the contrary, if we discover that there is no real difference between these ideologies.


##################################################### Brouillon des anciens readme qu'on garde au cas ou
we chose to filter the data by removing the unknown speaker, then we only get the quotes that have been said by a politician and we get from wikidata the political party, the educational degree and the nationality of the speaker.

We can remove all quotations that don't have a speaker identified. We can also split the dataset by year, so that our analysis can be run just on a single year.

The first step was to extract our data. We decided to split our data by year before loading it and to filter some information useless for our research. ######
################# We managed to load the data from both Quotebank and Wikidata. ############ A DVLPER For QuoteBank, we used the course
code in the notebook and for Wikidata we used parquets ##############XX.  After this, we created a join in term of the ID in order to group the informations in both database. 

We chose to start by filtering out the unknown in Quotebank and the non-politicians using wikidata.
We chose to quantify the distribution between Americans and Non Americans speakers in order to check if it was relevant to analyze the data only in the USA 
and we came to the conclusion that ?????? ############ Quelle ccl ?
We also decided to add an educational level feature for each speaker and we decided to study the distribution of this feature to see if it was reliable or not. 

### Data Visualization ???? Va-t-on en faire ? 
- distribution us non us : ratio 
- ratio political or not 
- what’s in the data (formats, distributions, missing values, correlations, etc.).

## Timeline & Team Organization
* Week 1 : Understand the distribution of the data depending on different parameters.
* Week 2 : Apply the NLP.
* Week 3 :
* Week 4 :
* Week 5 : Cluster the data and conclude.

## Contributions 
- Aya Rahmoun
- Abdeslam Guessous
- Louay Najar
- Mortadha Abderrahim

## Questions for TAs 

