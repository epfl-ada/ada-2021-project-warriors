# Project Milestone 2 : ada-2021-project-warriors

## Abstract
This paper reports the differences between left and right wing ideologies. They have distinct, and to an extent, contradictory opinions and even have different priorities. However, do their quotes reflect these fundamental disagreements? 
We suggest clustering politicians based on the similarities in their quotes provided in the Quotebank to verify if we can conclude the ideology of a 
quote speaker based on a data-driven approach. Labels from speakers' political ideology on wiki data could be used as the ground truth to assess our classifier.   
Such analysis could provide readers with more insights and background on a quote/text to better understand it and its ideology.

## Research Questions
1. Are right wing and left wing politicians that different?
2. How to define a similarity between politicans ? Do quotes whose speakers are similar in ideological background or political positioning
show similarities in terms of that definition? 
3. Can we design a data driven approach to cluster quotes matching with the ideologic left/right separation ? 
4. Does the increase in polarisation result in an increase in political violence ?
5. Is there a difference in the language used by politicians who have a university degree and those who don’t ?

## Proposed Datasets
1. Quotebank. This is the dataset from the course that will provide us speaker-attributed quotations. 

2. Wikidata. This dataset will give us all the informations related to political speakers (political party, education, nationality...).

## Methods
We can remove all quotations that don't have a speaker identified. We can also split the dataset by year, so that our analysis can be run just on a single year.
The first step was to extract our data. We decided to split our data by year before loading it and to filter some information useless for our research. ######
################# We managed to load the data from both Quotebank and Wikidata. ############ A DVLPER For QuoteBank, we used the course
code in the notebook and for Wikidata we used parquets ##############XX.  After this, we created a join in term of the ID in order to group the informations in both database. 

### Preprocessing : 
We chose to start by filtering out the unknown in Quotebank and the non-politicians using wikidata.
We chose to quantify the distribution between Americans and Non Americans speakers in order to check if it was relevant to analyze the data only in the USA 
and we came to the conclusion that ?????? ############ Quelle ccl ?
We also decided to add an educational level feature for each speaker and we decided to study the distribution of this feature to see if it was reliable or not. 

### Data Visualization ???? Va-t-on en faire ? 
- distribution us non us : ratio 
- ratio political or not 
- what’s in the data (formats, distributions, missing values, correlations, etc.).

## Timeline & Team Organization
Week 1

Week 2

Week 3

Week 4

## Contributions 
Aya Rahmoun

Abdeslam Guessous

Mortadha Abderrahim

Louay Najar

## Questions for TAs 

