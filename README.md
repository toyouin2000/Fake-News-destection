# Fake_News_Detection

The aim of this project is to classify user supplied news as real or fake. For this task we will be using NLP techniques such as CountVectorizer, Tf-idf vectorizer, Tf-idf transformer.

The complete roadmap is : 
    
    1. Import Dataset
    2. Creating wordcloud visuals
    3. Cleaning & Preprocessing
    4. Applying NLP techniques
    5. Using classification models
    6. Creating pipeline
    7. Predictions
    
## Importing Dataset
The dataset contains Id, Title of news, Author, Complete text (news) and the labels (0 means fake news and 1 means real news), some preprocessing steps were taken : replacing NaN values by " "; merging title, author, text and creating a new column "total" 

## Creating wordcloud visuals
all the words from "total" column were used to create wordclouds for both the real words (real news) and fake words (fake news).

## Cleaning and Preprocessing          
used regex on every row of "total" column in order to remove punctuations (eg. @,!,#,% etc.), then used word_tokenize() from nltk library in order to tokenize the sentences in words, further removed stopwords (English) and used WordNetLemmetizer to converting the word into their dictionary format.

## Applying NLP techniques 
Countvectorizer and Tfidftransformer were used to get the frequency of words in data and represented as matrix.

## Using classification models
Used logistic regression and multidimentional naive bayes model to classify the news as real or fake. Both model takes tfidf matrix as input.
The test set accuracy of logistic regression was around 98% whereas for multidimentional naive bayes it was around 84%.

## Creating pipeline
Pipeline was imported from sklearn.pipeline, then pipeline object was created with countvectorizer, tfidf-transformer and logistic regression as steps.
Then it was trained over the untransformed data and saved as pipeline.sav

## Prediction
Prediction on the user supplied news was done.
