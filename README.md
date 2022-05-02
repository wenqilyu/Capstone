# COVID-19 Rumor Detection 

## Repository Structure

**data**: This folder contains the data used by the project. 

**notebook**: This folder is divided into three parts, the first part is data cleaning, the second part is EDA part, and the third part is model part.


## Problem Statement
The spreading rate of coronavirus disease 2019 (COVID-19) has been very high around the world. The world was in a war to fight not only a pandemic, but also an infodemic. In this project, I design a rumor detection and truth response system to combating the infodemic.

## Approach
1.Data collection: I found some COVID-19 related rumor tweets from papers and GitHub[1], and scraped the information using Twitter Hydration Tool[2]. 

2.Data processing: After successfully extracting the data, we finally generate a new COVID-19 rumor dataset with labels. Where tag=1 means that the tweets are correct information, where tag=0 means that the tweets are incorrect information. Then, we clean tweets content, removing stop words, punctuation, lemmatization, etc.

3.Exploratory Data Analysis:In the EDA section, first, we analyze the distribution of the age of rumored users and the number of followers. Second, we analyzed the content of the rumor, comparing the number of proper nouns, the number of stop words, and the number of capital letters between the rumor and correct information. Third, we did a sentiment analysis to see if sentiment differed between rumors and non-rumors using nltk package[3]. Finally, we plotted word clouds from 2020 to 2022, showing which topics people paid attention to when COVID-19 was extracted in different years.

4.Model: We mainly used logistic regression[4], support vector machines[5] and BiLSTM[6] as classification models. We use sklearn[7], karas[8] and tensorflow[9] packages.

5.Truth match: 

## Thanks

