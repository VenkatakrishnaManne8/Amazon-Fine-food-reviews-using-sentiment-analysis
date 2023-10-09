# Amazon-Fine-food-reviews-using-sentiment-analysis

The data set consists of 14 features along with the target value which is used to predict whether the person has heart disease or not, It is a multivariate data set that consists of or includes a number of distinct mathematical or statistical variables, as well as multivariate numerical data analysis.

The Amazon Fine Food Reviews dataset consists of reviews of fine foods from Amazon.

Number of reviews: 568,454 Number of users: 256,059 Number of products: 74,258 Timespan: Oct 1999 - Oct 2012 Number of Attributes/Columns in data: 10 Attribute Information: Columns in the dataset

Id: The ID for each row of data ProductId - unique identifier for the products in Amazon fine food category UserId - A primary identifier for each user ProfileName - Profile name of the associated user HelpfulnessNumerator - number of users who found the review helpful HelpfulnessDenominator - number of users who indicated whether they found the review helpful or not Score - rating which varies between 1 and 5 Time - timestamp for the review Summary - brief summary of the review Text - text of the review

a) Objective: Predicting the sentiment of the given review

I've applied LSTM, Random Forest,KNN, and Naive Bayes to this data set

Steps Performed on the Dataset:

I've acquired this dataset from Kaggle through this link https://www.kaggle.com/snap/amazon-fine-food-reviews

2. DataCleaning:

I've applied a few techniques in order to remove any missing, duplicate values within the dataset.

As well as per the dataset The helpfulness numerator which means the number of users who found it helpful should be always less than the denominator which includes both kinds of users who found it helpful or not we identified those and removed them
If we observe the data we have reviews whose rating ranges from 1 to 5 however we see there are reviews with a rating of 3 which are considered neutral reviews as we need to predict either positive or negative reviews so I removed these rows with neutral review
we also encoded the reviews greater than 3 as 1 and the ones less than 3 as 0.

3.  Data Pre-processing:

In this, we performed activities like Removing Punctuations and HTML tags from the texts of the review.
Stopwords: we have removed the stop words like (and, is, are, etc,..) from the text as it doesn't help the model understand the sentiment of the user and will also help the model to learn the more weighted words within the reviews
Stemming: We have applied a technique called stemming which stems the words to their roots so that all the words that are common but change in their tense will be treated as one word and will help in reducing the vector dimension and also converted the text into lower case for encoding purpose.
Encoding the data: I've applied the Bag of words technique in order to encode the text data into a vector form

4. Observations

Accuracies of the classifiers used :
LSTM: 87.88
Naive Bayes: 86.81
Random forest: 85.51
I have run this pre-processed data on LSTM, Naive Bayes, Random forest
After running all the models it's observed that LSTM outperformed w.r.t to its accuracy on the test/validation set.
