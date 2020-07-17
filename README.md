# POS-Tagging-and-News-Classification in Python (Internship Task)
Name: Sreyam Dasgupta
Dataset: BBC News Dataset from Kaggle 
Test Set Accuracy: 98.32

Libraries Used:
For NLP tasks: Spacy, CountVectorizer, TfIdfVectorizer
For handling data: csv, numpy, pandas
For ML models: sklearn (Logistic Regression, SVC, Multinomial NB)
For metrics: sklearn (accuracy score, classification report)

News Classification:

Pipeline:
1. Training Data is used to form a bag of words/one-hot encoding. (Both are used to check which one gives better performance)
2. Training, validation and test features are obtained from these embeddings.
3. The different models are trained on training features.
4. The trained models are used to predict on validation fatures.
5. The model with best accuracy on valiadtion set is selected.
6. It s then applied on test data.

Conclusion and Discussion:
   All the six models performed well on validation set but Multinomial Naïve Bayes with One-hot encoding vectorization performed best.  
I used Naïve Bayesbecause it assumes that the features are independent of each other, which is true to some extent in this case. I
used its multinomial version because it assumes a (multinomial) distribution of each feature given a class. This works particularly 
well for features like word counts, etc. I used fit_prior as True because, there is an imbalance in classes, and I wanted the model 
to use that knowledge while prediction. I used alpha = 0.01 as a regularization parameter to stop the model from overfitting.




POS Tagging:

Pipeline:
1. The article is tokenized.
2. The POS tag of each of token is extracted, and each token is added to corresponding POS TAGlist.

Conclusion:
    This task is quite straightforward thanks to python's library 'spacy'.
