# Mod-3-Project-Books

# Predicting Authors of Books
We took txt files of books from http://textfiles.com/etext/AUTHORS/ and Project Gutenberg. We wanted to make sure that all of the books that we used were part of the public domain, so no modern authors were included. We looked at 239 books from 16 different authors.
## Motivation
We wanted to see if we could predict an author of a book by it’s text using NLP and Machine Learning.
## Tech/framework used
- Sklearn
- Matplotlib
- Pandas
- Numpy
- Itertools
- Seaborn
- Scipy 
- Wordcloud
- Wget - for harvesting the data, not a requirement if you want to use something else or if you just start from our csv file
## Features
Our best model had a testing F-1 score of 1.0 and a cross validation score of .93 across 5 folds.
## How to use?
If you would like to run this yourself with your own data, download all of your data as txt files. Have a folder for each author (named as said author) and all their works named as the title of the work in the appropriate folder. Make a list of all the file paths and start with the notebook “pre_process_clean_data.ipynb”. This will read in and pre process the data.
Then use the notebook “SVM_SGDR.ipynb“ for our best model.
## Credits
By Lois Rosenbloom and Luke Borsare
