# Fake-News-Prediction-Kaggle

This repository contains a project that aims to predict whether a news article is fake or real using various machine learning techniques.

## Table of Contents
- [Description](#description)
- [Evaluation](#evaluation)
- [Citation](#citation)
- [Dataset Description](#dataset-description)
- [Importing the Dependencies](#importing-the-dependencies)
- [Data Pre-Processing](#data-pre-processing)
- [Stemming](#stemming)
- [Applying Stemming to the DataFrame](#applying-stemming-to-the-dataframe)
- [TF-IDF (Term Frequency - Inverse Document Frequency)](#tf-idf-term-frequency---inverse-document-frequency)
- [Training the Model](#training-the-model)
- [Preparing the Submission File](#preparing-the-submission-file)

## Description
Develop a machine learning program to identify when an article might be fake news. Run by the UTK Machine Learning Club.

## Evaluation
The evaluation metric for this competition is accuracy, a very straightforward metric.

accuracy= correct predictions / (correct predictions + incorrect predictions)

Accuracy measures false positives and false negeatives equally, and really should only be used in simple cases and when classes are of (generally) equal class size

Submission Format
For every article in the test dataset, submission files should contain two columns: `id` and `label`. The `id` column should refer to a row in the `test.csv` file, and the `label` column should refer it's class of reliable (`0`), or potentially fake (`1`).

The file should contain a header and have the following format:

```
id,label
182041,1
182042,0
182043,1
182044,0
etc.
```

## Citation

[@fake-news]: William Lifferth. (2018). *Fake News*. Kaggle. Available at: https://kaggle.com/competitions/fake-news


## Dataset Description

1. train.csv: A full training dataset with the following attributes:

- id: unique id for a news article
- title: the title of a news article
- author: author of the news article
- text: the text of the article; could be incomplete
- label: a label that marks the article as potentially unreliable


- 1: unreliable
- 0: reliable


2. test.csv: A testing training dataset with all the same attributes at train.csv without the label.

3. submit.csv: A sample submission that you can use as a sample submission

## Importing the Dependencies
This section covers importing necessary libraries such as pandas, numpy, re, sklearn and nltk.

## Data Pre-Processing
Data preprocessing steps include:
- Handling missing values
- Text cleaning (removing punctuation, stopwords, etc.)

## Stemming
Stemming is applied to reduce words to their root form, which helps in reducing the dimensionality of the text data.

## Applying Stemming to the DataFrame
This section demonstrates how stemming is applied to the text data in the DataFrame using the PorterStemmer from the nltk library.

## TF-IDF (Term Frequency - Inverse Document Frequency)
TF-IDF is used to convert the text data into numerical features. This technique helps in understanding the importance of a word in a document relative to a collection of documents (corpus).

## Training the Model
A logistic regression model is trained and tested.

## Preparing the Submission File
The final model is used to predict the labels for the test dataset, and the results are saved in a CSV file for submission on Kaggle.
