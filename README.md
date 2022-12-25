The dataset is from the url https://www.dropbox.com/sh/hkcde3z2l1h9mq1/AAB2U1dYf6pR7qij1tQ5y11Fa/csv?dl=0&subfolder_nav_tracking=1
This data is of Indian district courts from the Development Data Lab.

The 3 metadata links are:
1. https://docs.google.com/spreadsheets/d/e/2PACX-1vTNxZtceqgzYlUogz-gJfMfqm-RygJZcqfZiFCQAsJYFG7BU1_ZT5aKTPrNODeDgRnoyZFBnjt2sghd/pubhtml#

2. https://docs.google.com/spreadsheets/d/e/2PACX-1vSqcp7VlnFB4ujCCHV5uGHjBlwYf7Mo4B3N3aqdiAukS7VMY8lLGU9ejhHH4c8qCse8l1kc8yIkCnq9/pubhtml#

3. https://docs.google.com/spreadsheets/u/1/d/e/2PACX-1vSkFghNxGjLxIAsjvUPkW8IV2AF1vf2KOQV93vMhB0TD3CBT13gah1LczI8W0d3Eom1zPcroBuPQ-uy/pubhtml#

The files we need from the dataset are: cases_2010.csv, cases_2011.csv, judges_clean.csv, and acts_section.csv

The directory structure is, jupyter notebook in the root directory along with cases_2010.csv and cases_2011.csv.
The files judges_clean.csv and acts_section.csv are in the csv folder of the root directory.

The jupyter notebook is named as "main.ipynb".

To run the code, just run the jupyter notebook.

The dependencies are:
1. pandas
2. matplotlib
3. sklearn

The approach I have taken is first gone through the data format and then try to come up with some basic analyses.
Then I combined the data from 2010 and 2011 into one python variable and did the necessary pre-processing.

Since the data set is very large, I have taken the data of the first 20000000 lines from the acts data and found whichever ones belong to the years 2010 and 2011 by mapping the ddl_case_id between the files.

This generated around 1.5 million rows of data which I have used for my analysis.

The classification problem I came up with is: run an ML model and check if the cases have been misclassified as criminal when based on the other parameters it should not have been the case.

The ML models I have used are Bayesian Classifier, and KNN Classifier.

Based on this, I found that there indeed were many cases which were misclassified as criminal when they should not have been and then generate insights on the same.
The insights were related to:
1. Time it takes for these misclassified cases to be closed as compared to the average time.
2. State wise distribution of these misclassified cases to check if there is any pattern.
3. Which position of the judge is most likely to misclassify the cases.

I also plotted my results in the form of bar graphs and pie graphs for all the above mentioned insights and analyses.

The code has also been commented wherever necessary for the readers' convenience.

Finally, I have also reported the performance measure of the model I have used.
