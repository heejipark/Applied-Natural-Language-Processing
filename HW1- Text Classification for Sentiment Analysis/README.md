# CSCI544: Homework Assignment 1 
## SCORE: 100/100

- This assignment gives you hands-on experience with text represen-tations and the use of text classiﬁcation for sentiment analysis. Sen-timent analysis is extensively used to study customer behaviors using reviews and survey responses, online and social media, and healthcare materials for marketing and costumer service applications. The assign-ment is accompanied with a Jupyter Notebook to structure your code. Please submit a PDF report which contains answers to the questions in the assignment and also print the completed Jupyter Notebook in PDF format (just submit one PDF ﬁle by merging your written answer and the completed Jupyter notebook). On your completed Jupyter notebook, please print the requested values, too. Additionally, you also need to submit an executable .py ﬁle which when run, generates the requested numerical outputs in the assignment. We need the .py ﬁle to check overlap between codes to detect plagiarism.


### 1. Dataset Prepration (10 points)
We will use the Amazon reviews dataset which contains real reviews for kitchen products sold on Amazon. The dataset is downloadable at:
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_ us_Kitchen_v1_00.tsv.gz
(a) Read the data as a Pandas frame using Pandas package and only keep the Reviews and Ratings ﬁelds in the input data frame to generate data. Our goal is to train sentiment analysis classiﬁers that can predict the sentiment (positive/negative) for a given review. Include three sample reviews in your report along with corresponding ratings. Also, report the statistics of the ratings, i.e., how many reviews received 1 ratings, etc.
We create binary labels using the ratings. We assume that ratings more than 3 demonstrate positive sentiment (mapped to 1) and rating less than 2 demonstrate negative sentiment (mapped to 0). Discard reviews with the rating 3. Include the number of reviews for each of these three classes in your report (to be printed by .py ﬁle in separate lines).
The original dataset is large. To avoid computational burden, select 100,000 reviews with positive sentiment along with 100,000 reviews with negative sentiment to preform the required tasks on the downsized dataset. Split your dataset into 80% training dataset and 20% testing dataset.


### 2. Preprocessing (20 points)
Implement the following steps to preprocess the dataset you created:
-	convert the all reviews into the lower case.
-	remove the HTML and URLs from the reviews
-	remove non-alphabetical characters remove extra spaces
-	perform contractions on the reviews, e.g., won’t → will not. 
Include as many contractions in English that you can think of.
You can either use Pandas package functions or any other built-in func-tions. Do not try to implement the above processes manually. Most of the above processes can be performed with one line of code. In your report, print the average length of the reviews in terms of char-acter length in your dataset before and after cleaning (to be printed by .py ﬁle).


### 3. Preprocessing (20 points)
Use NLTK package to process your dataset:
-	remove the stop words
-	perform lemmatization
Print three sample reviews before and after data cleaning + preprocessing.
In the .py ﬁle, print the average length of the reviews in terms of character length in before and after preprocessing.


### 4. Feature Extraction (10 points)
Use sklearn to extract TF-IDF features. At this point, you should have created a dataset which consists of features and binary labels for the reviews you selected.


### 5. Perceptron (10 points)
Train a Perceptron model on your training dataset using the sklearn built-in implementation. Report Accuracy, Precision, Recall, and f1-score on both the training and testing split of your dataset. These 8 values should be printed in separate lines by the .py ﬁle.


### 6. SVM (10 points)
Train an SVM model on your training dataset using the sklearn built-in implementation. Report Accuracy, Precision, Recall, and f1-score on both the training and testing split of your dataset. These 8 values should be printed in separate lines by the .py ﬁle. 


### 7. Logistic Regression (10 points)
Train a Logistic Regression model on your training dataset using the sklearn built-in implementation. Report Accuracy, Precision, Recall, and f1-score on both the training and testing split of your dataset. These 8 values should be printed in separate lines by the .py ﬁle.


### 8. Multinomial Naive Bayes (10 points)
Train a Multinomial Naive Bayes model on your training dataset using the sklearn built-in implementation. Report Accuracy, Precision, Recall, and f1-score on both the training and testing split of your dataset. These 8 values should be printed in separate lines by the .py ﬁle.
