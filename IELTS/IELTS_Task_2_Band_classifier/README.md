# Band classification of IELTS writing task 2

## Summary of Project

This project presents a prototype classifier for predicting IELTS Writing Task 2 band scores using neural networks. The goal is to assist students in evaluating their writing performance by predicting their band level based on their essay and the task prompt. The classifier was built using Feedforward Neural Networks (FFNN), Long Short-Term Memory (LSTM) networks, and Transformer-based BERT models, with various optimizers and hyperparameter tuning strategies.

## Preprocessing Steps

- **Dataset Source**: ['IELTS Writing Scored Essays Dataset'](https://www.kaggle.com/datasets/mazlumi/ielts-writing-scored-essays-dataset/data)
- **Filtering**: Focused on Task_Type 2 (essay writing tasks)
- **Band Conversion**: Overall scores were mapped to band labels (A, B1, B2, C1, C2), then simplified to binary classification (B vs. C)
- **Tokenization**: Used Keras Tokenizer and padding for FFNN/LSTM; BERT tokenizer for Transformer model
- **No Cleaning**: Preserved punctuation, casing, and special characters due to their relevance in writing assessment

## Model Architecture

### FFNN
- Embedding → Flatten → Dense (ReLU) → Dropout → Dense → Dropout → Output (Sigmoid)

### LSTM
- Embedding → LSTM (stacked) → Dense layers → Output (Sigmoid)

### BERT
- Pretrained BERT (frozen) → Dense layers → Output (Sigmoid)

## Training Process

### Framework
- TensorFlow & Keras

### Loss Function
- Binary Crossentropy

### Optimizers
- Adam
- AdamW
- SGD with Momentum

### Metrics
- Accuracy
- Precision
- Recall
- F1 Score

## Results

### FFNN with Adam
- **Accuracy**: 0.6352
- **Precision**: 0.6528
- **Recall**: 0.5875
- **F1 Score**: 0.6184

### FFNN with AdamW
- **Accuracy**: 0.5786
- **Precision**: 0.8421
- **Recall**: 0.2000
- **F1 Score**: 0.3232

### FFNN with SGD
- **Accuracy**: 0.6289
- **Precision**: 0.6842
- **Recall**: 0.4875
- **F1 Score**: 0.5693

### LSTM with Adam
- **Accuracy**: 0.4969
- **Precision**: 0.0000
- **Recall**: 0.0000
- **F1 Score**: 0.0000

### LSTM with AdamW
- **Accuracy**: 0.5660
- **Precision**: 0.5591
- **Recall**: 0.6500
- **F1 Score**: 0.6012

### LSTM with SGD
- **Accuracy**: 0.4969
- **Precision**: 0.0000
- **Recall**: 0.0000
- **F1 Score**: 0.0000

### BERT (Transformer)
- **Performance**: Poor across all metrics; deemed unsuitable for this task

## Conclusion

- FFNN with Adam optimizer yielded the best overall performance.
- Hyperparameter tuning improved LSTM performance but not BERT.
- BERT-based models were downgraded due to poor results.
- The project demonstrates the feasibility of using neural networks for automated writing band classification.