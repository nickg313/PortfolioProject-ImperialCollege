# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

**Input:** The input data into my model would be an Amazon Fine Food Review in text form, that was subsequently by me in the notebook and converted into a numerical representation using CountVectoriser to be inserted into the classification function.

**Output:** The output of my data is a sentiment classification for review. 1 represents negative sentiment and 5 represents positive sentiment. 

**Model Architecture:** In this project I used 2. The first was a Naive Bayes classifier, and the second was a Support Vector Machine model.

## Performance

For this project, I assessed performance by evaluating the F1 score of the model in question. I made sure to divide the data into both a training set and test set, and calculated the F1 score with hyper-parameter tuning and without it.

What I noticed was that the tuning of the SVM was flawed, and the bias in the data must have muddled the readings, because after tuning the SVM performance had dropped to a f1 score of 0.6 from 0.69.

Meanwhile, for NB, after tuning the model performance increased from f1 score of 0.59 to 0.69.

## Limitations

The first limitation is definitely that both models rely on the frequency of words and pattern in which they occur (note how the processing was done after the clean_message() function). As a result, there is a possibility that context and nuance could be lost in an analysis of a review, leading to misclassification potentially. 

The data is also very imbalanced, as demonstrated by the histogram in the notebook. There is roughly a 87/12 split in favour of 5 star reviews, meaning that biased predictions could potentially be made.

Another limitation is that the model was trained on Amazon Food reviews. As you can imagine, this is quite specific, and so the model may not adapt easily to other reviews/pieces of text.

Note - Lastly, one key limitation of the dataset here is that the way in which I sampled data for the hypertuning process of the SVM. Because GridSearch optimisation can be quite an extensive process, I sampled the original dataset down to 6k records before preprocessing. This is potentially bad practice, and may have led to inaccurate readings.

## Trade-offs

I definitely noticed the trade off between computation time and performance. The original dataset was 500 000+ records and I simplified it down to 30 000, which is still a big number, but at least I could process the data without waiting 2 hours! The trade off here is actually quite small since 30k is still enough for my processes, but represents an example of a small tradeoff I had to make, since 500k could have potentially produced better performance, even if it would have been marginal.

This was seen particularly with when I was trying to train my SVM model on even the 30k dataset, which was taking too long with GridSearch. As a result, I cut it down to 6k, and the program was able to flow again.

Another trade off was with generalisation and overfitting, which I saw very clearly in the SVM section. After hyperparameter tuning, my training data recieved an F1 score of 1 which indicated no false fittings whilst my test data got an F1 score of 0.60, which is mediocre. Perhaps by allowing the F1 score of the training data to fall, the test data's F1 score would rise, producing a better model ultimately. 



