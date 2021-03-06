# Kaggle's "Spooky Author Identification" solution

I built my solution on top of [this kernel](https://www.kaggle.com/sudalairajkumar/simple-feature-engg-notebook-spooky-author), however somehow managed to achieve a slightly better PL score.

### Ideas

Here's a quick list of what to try implementing next.

##### Simple models

1. ✔ calibrated predictors - achieved a slightly better score with `isotonic` method applied to the 2nd level XGBoost model;
1. add more models to the stack:
    - linear models (SGD),
    - tree-based models (RF, ETC, GBM, LGBM, CB),
    - Bayes models,
    - KNN,
    - SVM;
1. add more 2nd level models;
1. add 3rd level model;
1. ensembling - bagging, voting etc.

##### Features

1. CountVectorizer + TfidfTransformer;
1. ✔ SVDs on counts;
1. hashing vectorizer;
1. ✔ stemming and/or lemmatization in existing pipelines:
    - NLTK PorterStemmer,
    - NLTK WordNetLemmatizer;
1. word2vec-based features:
    - GloVe vectors → average per sentence,
    - train gensim on the dataset;
1. topic modeling - [look here](https://markroxor.github.io/gensim/tutorials/index.html).

##### More complicated models

1. LSTM:
    - word2vec,
    - character-wise,
    - [look here](https://github.com/brightmart/text_classification).
1. (Hidden) Markov chain model;
1. NLP in R.

##### Anything else?

1. tune parameters of models:
    - vectorizers - ngram ranges, mini\_df,
    - SVD - components, algorithm,
    - LR - maximum iterations, regularization,
    - XGBoost - number of trees, regularization, sampling.
