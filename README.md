# Analysis of Transgender and Non-Binary (TGNB) Reddit Posts and Comments 

## Table of Contents

1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Data](#data)
4. [Methodology](#methodology)
5. [Results](#results)
6. [Future Directions](#future-directions)
7. [Contact](#contact)

## Introduction

As a gender-affirmation surgeon I am interested in what potential patients and members of this community are discussing in online forums, particularly in regards to surgical procedures. 
Patients may feel more comfortable discussing their true opinions and thoughts in online spaces rather than at the surgeon's office.
I downloaded Reddit posts from TGNB subreddits that specifically included the word "surgery" and performed an exploratory data analysis (EDA), topic modeling, TF-IDF, and sentiment analysis on the texts. 
This is strictly an EDA and investigation of these posts, to better understand this community. Future directions would require manual labeling of the post and creating models that accurately predict the sentiment of the posts. 

## Project Overview

The data will be examined in the following ways: 
1. Examine post titles and comments to posts.
2. Perform NLP preprocessing steps.
3. Perform a brief network analysis of Redditors that are active in these spaces.
4. Perform TF-IDF on the comments.
5. Perform sentiment analysis on the comments.
6. Perform topic modeling on the comments. 

## Data

The data was scraped from reddit using the praw package on September 1, 2024. The following datasets were created during EDA.
1. TGNB metadata with the name of the original posts, the Redditor that posted them, the score
2. Comments csv with the parent comment replies to the original posts
3. Sentiment analysis csv with the sentiment analysis results
4. Cohsim csv with the topic modeling results
5. Topic scores csv with the topic modeling scores and results

## Methodology

EDA: Plots were created to examine posts by subreddit. Authors who posted more than once were analyzed in more detail. 
Network analysis was performed to examine the subreddits where authors post and how they are connected to one another. 
Comments to posts were extracted and also analyzed. 

NLP preprocessing was performed with the following steps:
1. Removing newline and special characters
2. Tokenization
3. Lemmatization
4. Removing stop words
   
Visualizations of word counts and character counts were created. Top words in the dataset were plotted. A word cloud visualization was created.

Topic Modeling: Topic modeling was performed on the Reddit comments to investigate trends and latent topics within the data.
A range of topic numbers were tested and analyzed. 

TF-IDF: Term frequency-inverse document frequency was performed for unigrams and bigrams to evaluate top words in the dataset.
Two tokenizers were used to evaluate the data.

Sentiment Analysis: Sentiment Analysis was performed using several models, both lexicon and machine learning based. 
The following sentiment analysis models were used:
1. TextBlob
2. VADER
3. FLAIR

## Results

EDA demonstrated that many Redditors only post or comment once. There is a select group of Redditors that are active on TGNB subreddits. This can result in less varied online conversation.

TF-IDF with the simple tokenizer (string splitting) had the best results over the spacy tokenizer and nltk casual tokenizer.

Topic modeling revealed an ideal number of 10 topics. These varied but were mostly negative. 

Sentiment analysis with varying models did not agree. There was little correlation between the two models. This indicates the necessity for ground truth labeling.

## Future Directions

Future directions of this project would require manual review of each post and with manual labeling of sentiment or polarity. This can be used as the ground truth for models. 
Models could be built with TF-IDF inputs or topic model vector inputs. 

## Contact 

If interested in replicating or assisting me in publishing this work, you can contact me via Github at any time.
