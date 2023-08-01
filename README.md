# Stock-Sentiment-Analysis-using-News-Headlines

Prediction of fluctuation in stock price by using current day news headlines

## Stock-Sentiment-Analysis-Using-News-Headlines-by-Simple-NLP
In this Project we are predicting wheather the stock price goes up or down indicated by Label Colums of our data set.

Here, we are using diffrent types of model selection and apply text preprocessing and get the model accuracy from 54% to 85% which amazing for the accurate prediction.

We can use LSTM model also to get about 90% accuracy also. 


## Features of Dataset
* The kernel is all about creating a model to predict the stocks whether they go up or down based on the top 25 headlines
* The first column is "Date", the second is "Label", and the following ones are news headlines ranging from "Top1" to "Top25".
* Dataset Link from Kaggle  https://www.kaggle.com/datasets/aaron7sun/stocknews?select=upload_DJIA_table.csv)


## What is Sentimental Analysis? 
* Sentiment Analysis, as the name suggests, it means to identify the view or emotion behind a situation. It basically means to analyze and find the emotion or intent behind a piece of text or speech or any mode of communication.

* Python sentiment analysis is a methodology for analyzing a piece of text to discover the sentiment hidden within it. It accomplishes this by combining machine learning and natural language processing (NLP). Sentiment analysis allows you to examine the feelings expressed in a piece of text.


![senti](https://user-images.githubusercontent.com/90321099/175671498-5947c058-c10f-4b5c-bb7e-ae411359a0a2.png)


## Important Library
* Numpy
* Pandas
* nltk(Natural Language Toolkit)
* scikit-learn


## Data Cleaning and  Preprocessing
* Removing punctuations
  > --In this phase we are removing all the punctuations marks and unnecesssary character from the columns of the the dataset.

* Renaming of Columns name
  >--In this phase we just for simplicity and preprocessing purposes rename the columns like Top1,Top2,Top3..... to 1,2,3...etc.
* Lowering case of character
  >--In this we convert the case of all the data from upper case to lower so that during vectorization same word cannot have different vector. For example the word Go and go treating out model as same word. 


## Feature Extraction from Text
We use different types of models and vectorization method 
    
    1. CountVectorizer + RandomForestClassifer
        In this method,we uses CountVectorizer to convert the text into vector and RandomForestClassifer as a machine learning algorithm from model_selection
    2. TfidfVectorizer + RandomForestClassifer
        In this method,we uses TfidfVectorizer to convert the text into vector and RandomForestClassifer as a machine learning algorithm from model_selection
    3. TfidfVectorizer + MultinomialNB
        In this method,we uses TfidfVectorizer to convert the text into vector and MultinomialNB as a machine learning algorithm from model_selection
    
    
    
## Accuracy of models
* Accuracy of model should also depends on the the preprocesing of data,removal of particualar type of character and puctuation marks.
* Most of nlp project we can aplly Stopwords, Stemming and Lemmatization on documnet of words but In this project we did not apply any of them beacause these words are important for our training of model.
* Lowering the case of words play an important role dring training time and provide a Good Accuracy.


  >When we do not apply proper preprocessing and data cleaning then the Accuracy of our mmodel is around 50% only.
    1. CountVectorizer + RandomForestClassifer
      >This model gives around 85% accuracy
  ![1](https://user-images.githubusercontent.com/90321099/175764837-f047d638-0fda-4bd2-8376-a80a4e9219f9.png)

     2. TfidfVectorizer + RandomForestClassifer
      >This model gives around 84% accuracy
    ![2](https://user-images.githubusercontent.com/90321099/175764886-97690524-8b6d-486a-b330-aa063987842d.png)

    3. TfidfVectorizer + MultinomialNB
      >This model gives around 85% accuracy
    ![3](https://user-images.githubusercontent.com/90321099/175764893-6278dfca-50b8-4d70-a657-c2cbfbd305dd.png)


    
    
    
    