# IELTS Task 2 Topic Modelling

This analysis applies topic modeling techniques to IELTS Task 2 writing samples. The goal is to identify recurring themes and topics in the essays, providing insights for language learners and educators.

## Algorithms

**Pipelines**
- **Regular:** traditional preprocessing steps: lowering, remove punctuation, estra space, stops, digits, and special characters.
  
**Model Selection**
- **Bag of Words + LDA:** LDA is the chosen model because of their assumptions: documents are mixtures of topics and that topics are mixtures of words.
- **BERT + K-Means++:** BERT was selected because of its bidirectional approach, which is suitable for language modelling. K-Means++ improved method is going to be implemented because of its refined cluster center selection based on the data.
  
**Number of topics evaluation**
- The first approach was the 10% of the number of unique questions tested in a range of puls-minus 5.
- The range wa splotted and evaluated by Elbow Plot

**Best model selection**
- **Bag of Words + LDA:** Weighted sum between perplexity and coherence (perplexity = 0.4,  coherence = 0.6). Perplexity has lower weight because its preference over certain topics.
- **BERT + K-Means++:** Weighted sum between Silhouette Score, Davies-Bouldin Index, and Calinski-Harabasz Index. (Silhouette Score =  0.4, Davies-Bouldin Index = 0.3, Calinski-Harabasz Index = 0.3).

## Project Structure

- **ielts_writing_dataset.csv**: Contains the dataset used for training and testing the model, containing IELTS writing samples and related metadata.
- **IELTS_T2_topic_modelling.ipynb**: Jupyter Notebook for performing topic modeling on IELTS Task 2 writing data. This includes preprocessing, model training, and analysis of the discovered topics.

## Versioning

- **Version 1**: Initial model, including data analysis, preprocessing, model training, and evaluation.
