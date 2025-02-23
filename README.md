# Clustering-Wikipedia-Text-Data-A-Comparative-Analysis-of-K-Means-and-Hierarchical-Clustering

Photo by <a href="https://unsplash.com/@lukechesser?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Luke Chesser</a> on <a href="https://unsplash.com/photos/wikipedia-page-screenshot-D8QbsYyiFmw?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a>
      
Project Overview

This project explores text clustering techniques using web-based content retrieved from Wikipedia. The dataset consists of 40 Wikipedia pages categorized into four general topics: artificial intelligence, sports, college majors/courses, and animals. The goal is to apply unsupervised machine learning methods to analyze the underlying structure of the textual data and evaluate how well clustering techniques can organize documents into their expected topical groups.

Methodology:

a.) Data Preparation

> Retrieve Wikipedia page content for the selected topics.

> Preprocess the text and construct a TF-IDF-weighted Document Term Matrix to represent the textual data numerically.

b.) K-Means Clustering

> Perform elbow analysis to determine the optimal number of clusters (k) by evaluating the sum of squared distances for k values ranging from 2 to 15.

> Analyze whether the optimal k aligns with the expected number of topic groups.

> Implement K-Means clustering and examine the cluster assignments.

C.) Hierarchical Clustering

> Apply Agglomerative Clustering with k set to the expected number of topic groups.

> Evaluate the clustering output and assess its alignment with the expected classification of topics.

Findings & Observations

> Elbow analysis did not reveal a distinct k value, suggesting that the text data contains overlapping features across categories. This lack of a clear elbow point indicates that simple clustering based on TF-IDF features may not effectively separate the topics.

> K-Means clustering did not fully align with the expected topic groupings. Some documents, such as "leopard" (animal) and "hockey" (sports), were incorrectly clustered together, indicating semantic similarities between topics that K-Means struggled to separate.

> Hierarchical clustering also failed to produce distinct topic-based clusters. Examples include "Biology" (academic course) being grouped with "swimming" (sports), and "Economics" (academic discipline) being clustered with "monkey" (animal). These misclassifications suggest that additional feature engineering or domain-specific embeddings might be needed for improved clustering performance.

Conclusion

This analysis highlights the challenges of clustering high-dimensional text data using traditional TF-IDF representations. The overlap in document features suggests that alternative approaches such as topic modeling (LDA) or word embeddings (Word2Vec, BERT) could be explored to improve clustering accuracy. Future work could involve refining preprocessing techniques, experimenting with different similarity metrics, or incorporating supervised learning methods to guide clustering performance.
