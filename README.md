# Mod-3-Project-Books

# Predicting Authors of Books

## Motivation
We wanted to see if we could predict an author of a book by it’s text using NLP and Machine Learning. Our goal was to create a model that we could input a book (or a chapter, sentence or even word) to predict the author.  If a model like this has enugh data, it could be used to guess ghost writters of a book, or guess pen names of well known authors who write other books on the side.
## Sources
We took txt files of books from http://textfiles.com/etext/AUTHORS/ and Project Gutenberg. We wanted to make sure that all of the books that we used were part of the public domain, so no modern authors were included. We looked at 239 books from 16 different authors. We also didn't want to try to deal with differences in translations, so we only chose authors who wrote in English.
## Exploratory Data Analysis of our DataFrame
DataFrame Head: This shows the top five rows of our dataframe. Author is our Target (y) variable while text is our independent variable: 

![image of dataframe head](/Screen%20Shot%202019-03-29%20at%2011.23.03%20AM.png)

This graph shows the number of works per author our dataset had:

![image of graph of work counts per author](/Screen%20Shot%202019-03-29%20at%201.11.14%20PM.png)

This graph shows the word count (in millions) per author our dataset had: 

![image of graph of word counts per author](/Screen%20Shot%202019-03-29%20at%201.10.31%20PM.png)

## Cleaning Up the Data
After EDA, we cleaned up our data. We created a class that read in our data and did pre processing and cleaning automatically. It got rid of all punctuation and made everything lowercase. Then it tokenized all of the text and removed all common English stop words. It then lemmatized the text and added it to a single dataframe that was exported to a csv for easy sharing and importing into other notebooks.

## Data Analysis
Our best model had a testing F-1 score of 1.0 and a cross validation score of .93 across 5 folds.

![image of best model outcomes](/Screen%20Shot%202019-03-29%20at%201.12.01%20PM.png)

![image of AOC of best model](/Screen%20Shot%202019-03-29%20at%201.12.24%20PM.png)

## Model Results
We made multiple models with multiple parameters to get the best model possible. After multiple models and hyper parameter tuning we found that SGD-R tuned TF and ______ worked best. Our model predicts with nearly ~93% accuracy. Given that this is a multiclass classification model based on text data, this is beyond excellent. Here is a basic picture of all our models and their accuracy scores. 

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
