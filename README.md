# Machine-Learning-Predicting-Phishing-
Develop a model that classifies whether a website is a Phishing website.

## About dataset
Dataset consists of information about the website features.
Number of variables : 31
Number of records : 2456

## Data Pre-processing
1. Extracted the data into datafram 'df'
2. df.isna().sum - gives number of null values in each attribute.
   This dataset does not have any null values.
3. Since the records are one among [-1,0,1], there are no outliers.
4. Hence the dataset does not have noise and is clean.
5. Website features are stored in 'features' and target variable is stored in 'result'

6. Split the data into training set and test set.
 Firstly 99% of data is considered for training and 1% for testing.
 This resulted in considerable difference between accuracies of training and testing sets.
        accuracy on training data is 0.9226
        accuracy on testing data is 0.84
 
 Since maximum data is being taken for traning, the model is getting overfit.
 Hence change in split of data.
 
7. Now, 77% od data is considered for training and 33% for testing.
 This resulted in better accuracy scores.
 Hence continued with this split for further modeling.
 
##Training the model
Since it is a classification problem: Support Vector Machine, Gaussian Naive Bayes Classifier,
Random Forest Classifier, Decision Tree Classifier can be used.

 Results obtained on testing data sets are :
 Accuracies : Support Vector Classifier = 0.9531
              Gaussian Naive Bayes Classifier = 0.9395
              Random Forest Classifier = 0.9691
              Decision Tree Classifier = 0.9593
             
8. Let us apply PCA(PRINCIPLE COMPONENT ANALYSIS) on data and train the models
 Results obtained on testing data sets are :
 Accuracies : Support Vector Classifier after applying PCA = 0.9642
              Gaussian Naive Bayes Classifier after applying PCA = 0.9346
              Random Forest Classifier after applying PCA = 0.9667
              Decision Tree Classifier after applying PCA = 0.9593
              
##Conclusion
Since Random Forest Classifier gives best accuracy and even high precision rate.
Random Forest Classifier is selected to train our model.

Working of Random Forest Classifier
Random subsets are created from the original dataset.
At each node in the decision tree, only a random set of features are considered to decide the best split.
A decision tree model is fitted on each of the subsets.
The final prediction is calculated by averaging the predictions from all decision trees.


 
