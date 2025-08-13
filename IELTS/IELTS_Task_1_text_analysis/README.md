# Text analysis of IELTS Task 1 essays

This analysis is part of a broader effort to apply Natural Language Processing (NLP) techniques to educational datasets, with a specific focus on IELTS writing tasks. The goal is to identify patterns, evaluate writing quality, and generate insights to assist learners and educators.

## Algorithms

**Data Analysis**
- Overall score per band
- Percentage of grades by band
- Wordclouds of example essays

**Pipelines**
- **Fine-grained:** traditional fine-grained, in which details relevant to grammar are included
- **Deep fine-grained:** punctuation, stop words, and numbers were added to the previous pipeline.
  
**Word Embedding Methods**
- **BERT:** helps to deeply understand the sentence structure, meaning, and grammar use.
- **TF-IDF:** helps to verify if the words are related and consistent with the topic of the task.
- **SpaCy:** regular numerical embeddings of the entire document
  
**Evaluation Metrics**
- Cosine similarity
- Cosine dissimilarity

## Project Structure

- **ielts_writing_dataset.csv**: Contains the dataset used for training and testing the model, containing IELTS writing samples and related metadata.
- **IELTS_T1_text_analysis.ipynb**: Jupyter Notebook for analyzing IELTS Task 1 writing tasks. It includes data cleaning, preprocessing, and exploratory data analysis specific to the IELTS dataset.

## Versioning

- **Version 1**: Initial model, including data analysis, preprocessing, model training, and evaluation.
