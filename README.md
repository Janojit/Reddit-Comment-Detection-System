# Reddit-Comment-Detection-System

## Description About The Dataset:
Dataset was collected from Reddit using "praw" library. The Dataset consists of different kinds of Reddit Comments where labels are Normal, Racist or Provoking. The Dataset giving us the details about a comment being Provoking or Racist or not

## VARIABLE DESCRIPTIONS:
comment: Reddit Comments(text)
label: Categorical Variable Consits of normal, provoking, racist
## Objective:
- Analyse Reddit comments
- Develope a ML model which can determine wheather a comment is Provoking or Racist or Normal
- Understand Reddit Users behaviour
## Title: Reddit Comment Detection System
## Problem Statement:
Reddit is a social media where usually people share their opinions on certain events or issues, which portrays a mirror of our Society. The task is to develop a machine learning model that can accurately detect the type of comments on Reddit as either provoking or racist. The model should be able to analyze the textual content of the comment and classify it as either one of the three categories Normal, Provoking, Racist. The success of the model will be measured by its accuracy and AUC on a test dataset.

## Approach/Methods:
- Scraping Comments from Reddit using praw
- Removing The Null Values
- Converting the Imbalanced Classification data to Balanced one using SMOTE technique
- Appling Count Vectorizer
- Comparing Different models and Deploy the Best model
## Observation:
- Comments are collected from different Subreddits over a year using "praw" library.
- The Comments are labeled based on some basic Racist and Provoking words.
- There are 5 Null values in the Dataset which we need to drop or fill.
- It is better to drop those values as they are not having any significance effect on the model.
- As per the data we scraped, we found there are more than 2.8 lakh normal comments whereas provoking comments are about 6.3K and Racist comments are about 0.5K. From which we can infer that most of the Reddit users are not Racist and Provoking or Reddit's Policy for This kind of Comments are very strict.
- As the Data is imbalanced for classification, so we need to apply some kind of balancing techniques.
- I have label encoded the labels as string values can't be given to a model. "normal" has been mapped to 0, "provoking" has been mapped to 1 and "racist" has been mapped to 2.
- As the Scraped data was so huge so it's hard to fit models into it as our local system isn't that much efficient so. I have taken a sample of 20K out of it and going to fit those into models.
- If we take all 2.9 Lakh data points then obiviously the accuracy will be much higher.
- Using "nltk" library we are ignoring the common words which are not significant for this problem.
- To convert the text dataset into a proper dataframe I have used Count Vectorizer.
- As the Sampled data was also imbalanced so I have applied SMOTE technique to balanced the dataset.
- SMOTE is a statistical technique for increasing the number of cases in your dataset in a balanced way. The component works by generating new instances from existing minority cases that you supply as input.
- Random Forest is the best model for this case with Test Size 0.2 and Random State 40.
## Learnings & Reflection:
- Helped me to know about Data Scraping from Reddit
- Get Knowledge about NLP techniques
- Learn about SMOTE
