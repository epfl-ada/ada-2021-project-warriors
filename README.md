# Project Milestone 2 : ada-2021-project-warriors

## Abstract
This paper reports the differences between left and right wing ideologies. They have distinct, and to an extent, contradictory opinions and even have different priorities. However, do their quotes reflect these fundamental disagreements? 
We suggest clustering politicians based on the similarities in their quotes provided in the Quotebank to verify if we can conclude the ideology of a 
quote speaker based on a data-driven approach. Labels from speakers' political ideology on wiki data could be used as the ground truth to assess our classifier. 
Another aspect of this project is the study of the polarization throught the quotes.
Such analysis could provide readers with more insights and background on a quote/text to better understand it and its ideology.

## Research Questions
1. Are right wing and left wing politicians that different?
2. How to define a similarity between politicians ? Do quotes whose speakers are similar in ideological background or political positioning
show similarities in terms of that definition? 
3. Can we design a data driven approach to cluster quotes matching with the ideologic left/right separation ? 
4. Does the increase in polarisation result in an increase in political violence ?
5. How does the politicians speech vary depending on the educational degree?

## Proposed Datasets
1. [Quotebank](https://quotebank.dlab.tools). This is the dataset from the course that will provide us speaker-attributed quotations. 

2. [Wikidata](https://www.wikidata.org). This dataset will give us all the informations related to political speakers (political party, education, nationality...).

## Methods
First,in order to have a managable dataset we chose to filter the quote bank data set in the following way:
We deleted the quotes that have 'None' speakers, then we deleted the 'quoteID','numOccurrences','probas','urls'and'phase' columns since we do not need them for our analysis.
In order to enrich our dataset we used the provided speaker_attributes.parquet dataset, for each quote speaker we extracted from this dataset his political party, educational level and nationality. We were also interested in the proportion of American politicians in the dataset so we calculated this variable for each year.

Having Preprocessed our data, our plan is to now use Natural Language processing in order to extract information from the quotes and then cluster the quotes and see if we get different clusters for left and right or if we discover that there is no real difference in the "expressed sentiments"



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

