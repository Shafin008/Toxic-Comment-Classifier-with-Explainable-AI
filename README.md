# Toxic-Comment-Classifier-with-Explainable-AI

Played around with some classic ML algorithms like Logistic Regression, Support Vector Machines, and Naive Bayes algorithms to classify toxic comments and then implemented XAI (LIME) to understand the model's decision-making process.


## Dataset

The dataset from the ["Toxic Comment Classification Challenge"](https://www.kaggle.com/competitions/jigsaw-toxic-comment-classification-challenge/overview) was utilized to test those machine learning algorithms. The dataset contains a large number of Wikipedia comments that have been labeled by human raters for toxic behavior. The types of toxicity are, toxic, severe_toxic, obscene, threat, insult, and identity_hate```. 

Finally, Implemented Explainable AI LIME (Local Interpretable Model-Agnostic Explanations) to identify potential biases and improve the model's fairness and transparency.

The dataset is stored in a CSV format and I only utilized 2 columns:

- comment_text: The wikipedia comment text. (comment_text)
- toxic: If the comment is toxic or not.  (Target Column)
- Other columns are ignored, and hence are dropped.


## Preprocessing

Texts are cleaned to eliminate irrelevant information and reduce noise and nuances and. Such as,

- Text is lowercase.
- Contractions are expanded.
- URLs, mentions, and special characters are removed.

I also removed the stopwords since I am not using deep learning models or neural networks. I also utilized an unsupervised weighting scheme named TF-IDF (Term Frequency-Inverse Document Frequency) to create word embeddings consisting sparse matrix. This enables a model to identify how relevant a word is in a document by fitting and transforming the text data into vector representations.


## Classifiers

After splitting the dataset into 80:20 train-test splits, Utilized some classic ML algorithms like Logistic Regression, Support Vector Machines, and Naive Bayes algorithms to classify toxic comments. Trained those model on the data and then tested their performances.

The performances are shown in the table below.

| Serial        | ML Algorithm            | Accuracy       | Precision         | Recall           | F-1 Score |
| ------------- |:-----------------------:|:--------------:|:-----------------:|:----------------:|:---------:|	
| 1             |Logistic Regression	  |0.96            |0.96               |0.96              |0.96       |
| 2             |Linear SVM	              |0.96            |0.96               |0.96              |0.96       |
| 3             |Bernoulli's Naive Bayes  |0.95            |0.94               |0.95              |0.94       |

    
Finally, Explainable AI LIME (Local Interpretable Model-Agnostic Explanations) was implemented to identify potential biases and improve the model's fairness and transparency.

