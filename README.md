# Mod-3-Project-Books

# Predicting Authors of Books

## Motivation
We wanted to see if we could predict an author of a book by it’s text using NLP and Machine Learning. Our goal was to create a model that we could input a book (or smaller passages) to predict the author.  We are hopeful that given enough data a more expansive version of this model could be used in plagarism detection and aid in the identification of unidentified texts.
## Sources
We took .txt files of books from http://textfiles.com/etext/AUTHORS/ and Project Gutenberg. We wanted to make sure that all of the books that we used were part of the public domain, so no modern authors were included. We looked at 239 books from 16 different authors. We anticipated that translations of books would not be a reliable input as there could potentially be significant differences in vocabulary between different translators, so we excluded foreign authors from our data collection.
## Exploratory Data Analysis of our DataFrame
DataFrame Head: This shows the top five rows of our dataframe. Author is our Target (y) variable while text is our independent variable: 

![image of dataframe head](/Screen%20Shot%202019-03-29%20at%2011.23.03%20AM.png)

This graph shows the number of works per author our dataset had:

![image of graph of work counts per author](/Screen%20Shot%202019-03-29%20at%201.11.14%20PM.png)

This graph shows the word count (in millions) per author our dataset had: 

![image of graph of word counts per author](/Screen%20Shot%202019-03-29%20at%201.10.31%20PM.png)

## Cleaning Up the Data
After EDA, we cleaned up our data. We created a class that read, pre-processed, and cleaned our data automatically. Our pre-processing included removing capitalization and punctuation prior to tokenization, as well as the removal of stop words. The class then tokenized and lemmatized the text and returned it as a dataframe along with the target author lifted from the file path.

## Data Analysis
Our best performing model had a testing F-1 score of 1.0 and a cross validation score of .93 across 5 folds.

![image of best model outcomes](/Screen%20Shot%202019-03-29%20at%201.12.01%20PM.png)

![image of AOC of best model](/Screen%20Shot%202019-03-29%20at%201.12.24%20PM.png)

## Model Results
We made multiple models with multiple parameters to get the best model possible. After multiple models and hyper parameter tuning we found that atuned SGDC-Regression model worked best. Our model predicts with approximately 93% accuracy. Given that this is a multiclass classification model based on text data, this is beyond excellent. Here is a basic picture of all our models and their accuracy scores. 

## Frameworks / Libraries Used:
- Sklearn
- Matplotlib
- Pandas
- Numpy
- Itertools
- Seaborn
- Scipy 
- Wordcloud
- Wget - for harvesting the data, not a requirement if you want to use something else or if you just start from our csv file

## How to use?
If you would like to run this yourself with your own data, download all of your data as txt files. Have a folder for each author (named as said author) and all their works named as the title of the work in the appropriate folder. Make a list of all the file paths and start with the notebook “pre_process_clean_data.ipynb”. This will read in and pre process the data.
Then use the notebook “SVM_SGDR.ipynb“ for our best model. It is labled "Tuned SGD Classifier".

## Credits
By Lois Rosenbloom and Luke Borsare
