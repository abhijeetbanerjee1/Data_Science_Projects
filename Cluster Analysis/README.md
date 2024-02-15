# Cluster Analysis

## Overview
Cluster Analysis is a text analysis tool designed to perform cluster analysis on text data, particularly focusing on identifying common themes or topics within the data. This tool processes text data by cleaning it, performing lemmatization, and removing stopwords to enhance the accuracy of clustering. It then converts the cleaned text data into TF-IDF vectors and applies K-means clustering to group similar documents together. Additionally, it generates a word cloud as an output visualization to gain a deeper understanding of the prevalent themes or issues discussed in the text data.

## Features
- Text cleaning: Removes numbers, converts text to lowercase, and removes filler words like "umm".
- Lemmatization: Performs lemmatization using WordNet POS tags to reduce words to their base form.
- Stopwords removal: Eliminates common stopwords to improve clustering accuracy.
- TF-IDF vectorization: Converts the cleaned text data into TF-IDF vectors for clustering.
- K-means clustering: Applies K-means clustering algorithm to group similar documents.
- Word cloud generation: Produces a word cloud visualization to highlight prevalent terms within each cluster.

## Requirements
- Python 3.8
- scikit-learn
- NLTK (Natural Language Toolkit)
- WordCloud

## Note
Please note that the datasets used for testing and the corresponding outputs are not included in this repository. These datasets may contain sensitive information related to a research study and are not suitable for public distribution. However, you can use your own text data for cluster analysis using the provided tool.
