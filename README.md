Comparing Naive Bayes and Support Vector Machines For Sentiment Analysis Accuracy.

## NON-TECHNICAL EXPLANATION OF YOUR PROJECT

The purpose of this project was to create a sentiment classifier based off Amazon food review data, using both a Naive Bayes classifier and SVM classifier and compare the f_1 score for both models. For both, I experimented on the data set both without tuning my model and with tuning the model. The reason for this , is because I work in sales and often need to upsell clients on new products. As a result, it’s extremely helpful to have a program classify reviews as either positive or negative for me as they come in so I can focus only on contacting the positive ones and ignore the negative ones, otherwise I could end up easily wasting a bunch of time. The Amazon food review data was chosen because it’s a very large dataset, and so it the training process was smoother. However, the dataset , and the model following it simply acts as serves as a prototype to be put to use in a wide variety of use cases, such as in my email campaigns to classify positive responses and my company review data too.

## DATA

500 000 Amazon Fine Food reviews that were sampled to 30 000. Got it from Kaggle - https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews

Papers that have used this dataset - J. McAuley and J. Leskovec. From amateurs to connoisseurs: modeling the evolution of user expertise through online reviews. WWW, 2013.


## MODEL 

NaiveBayes classifier and SVM classifier.

## HYPERPARAMETER OPTIMSATION

The first hyperparameter I optimised was the 'alpha' hyperparameter, which is a smoothing parameter used to avoid zero probabilities and used the grid search for this, all in the attempt to find the best 'alpha' that results in the highest f1 score for the test set.

The second hyperparamter I optimised was the C value for SVM, which denotes the trade off between classification error and the margin of seperation of the hyperplane. 

The 3rd hyperparameter was the type of kernel used, ie) 'linear' or 'radial'.


## RESULTS

The SVM F1 score was significantly better than that of the Naive Bayes classifier before tuning. However, after some tuning, the Naive Bayes classifier also demonstrated satisfactory performance, bringing it's f1 score up to 0.69. However, the f1 score of the SVM dropped for some reason due to tuning, which I attribute to bias and inaccuracy in my sampling methods.

However, I must stress the potential bias/inaccuracy that may be present, since I had to resample the original dataframe and make it smaller in order to be able to perform hyperparameter tuning for the SVM model. 
