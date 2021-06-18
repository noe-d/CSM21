# How does Twitter map French departments ?

## Abstract

The availability of geographical information from social media data such as Twitter allows the identification of diversity in the spreading of information across one country. This document reports the analysis of hashtags from the collected geo-enabled tweets in a period of two weeks from the country of France to identify geographical characteristics of the collected hashtags. By using topic modelling methods to cluster the hashtags into meaningful topics, the geo-topical distribution of hashtags can be calculated for each France department, then the local and global characteristic of the topics can be identified. The analysis shows that hashtags clusters that contain geographically self-referential information and punctual events are largely local, and clusters that are related to entertainment and pets are mostly global. Interestingly, some clusters that are related to TV show and entertainment are found to have local preferences.

## Git contents

### Jupyter notebooks

This repository hosts the code used to collect, clean, explore and analyze the data.

#### Data collection

- `twitter_stream.ipynb` collect tweets thanks to Twitter Standard Streaming API

#### Preprocessing and preliminary exploration

- `preprocessing.ipynb` after an anonymization process: NLP cleaning of the textual contents including tokenization, stopwords removal, POS tagging, ... (not further used due to technical difficulties), and geo-enrichment based on geo-tags provided by the API
- `Hashtags_analysis.ipynb` coarse exploration of the hashtags contained in the tweets and first analyses

#### Topic Modelling

- `LDA.ipynb` LDA topic modelling on hashtags, including results and visualizations
- `LGLDA_tune.ipynb` tuning procedure for the hyper-parameters of the LGLDA model
- `LGLDA.ipynb` LGLDA topic modelling on hashtags, including results and visualizations
- `Network.ipynb` topic modelling through a graph theory approach
- `Louvain_viz.ipynb` Louvain communities topic modelling on hashtags, including results and visualizations

### Results

The main results and visualizations are also provided in two folders.

#### `html_figures`

- `data_filtered.html` map of the number of tweets for selected departments
- `hashtags_count.html` map of the count of hashtags for selected depatments
- `finalMap.html` final visualization associating word-cloud to each of the studied departments
- `Louvain.html` hashtags network with nodes colored according to their Louvain community (topic)

#### `topics_results`

- `df_lda_short.csv` topics found with the LDA, with the 10-topwords 
- `df_lglda_short.csv` topics found with the LGLDA, with the 10-topwords
- `df_louvain.csv` topics found with the network approach (communities with at least 5 hashtags)

