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

4.Model: We mainly used logistic regression, support vector machines and BiLSTM as classification models. We use sklearn[4], karas[5] and tensorflow[6] packages.

5.Truth match: We use jaccard similarity[7] to match the question with the tweets content and find the one with the largest similarity score as our return value.

## Thanks
[1]Cheng M, Wang S, Yan X, et al. A COVID-19 Rumor Dataset. Front Psychol. 2021;12:644801. Published 2021 May 31. doi:10.3389/fpsyg.2021.644801

[2]Documenting the Now. (2020). Hydrator [Computer Software]. Retrieved from https://github.com/docnow/hydrator

[3]Bird, Steven, Edward Loper and Ewan Klein (2009). Natural Language Processing with Python.  O'Reilly Media Inc.

[4]Scikit-learn: Machine Learning in Python, Pedregosa et al., JMLR 12, pp. 2825-2830, 2011.

[5]Chollet, F., & others. (2015). Keras. GitHub. Retrieved from https://github.com/fchollet/keras

[6]Martín Abadi, Ashish Agarwal, Paul Barham, Eugene Brevdo,Zhifeng Chen, Craig Citro, Greg S. Corrado, Andy Davis,Jeffrey Dean, Matthieu Devin, Sanjay Ghemawat, Ian Goodfellow,Andrew Harp, Geoffrey Irving, Michael Isard, Rafal Jozefowicz, Yangqing Jia,Lukasz Kaiser, Manjunath Kudlur, Josh Levenberg, Dan Mané, Mike Schuster,Rajat Monga, Sherry Moore, Derek Murray, Chris Olah, Jonathon Shlens,Benoit Steiner, Ilya Sutskever, Kunal Talwar, Paul Tucker,Vincent Vanhoucke, Vijay Vasudevan, Fernanda Viégas,Oriol Vinyals, Pete Warden, Martin Wattenberg, Martin Wicke,Yuan Yu, and Xiaoqiang Zheng.TensorFlow: Large-scale machine learning on heterogeneous systems,2015. Software available from tensorflow.org.

[7]Jaccard, Paul (February 1912). "THE DISTRIBUTION OF THE FLORA IN THE ALPINE ZONE.1". New Phytologist. 11 (2): 37–50. doi:10.1111/j.1469-8137.1912.tb05611.x. ISSN 0028-646X.
