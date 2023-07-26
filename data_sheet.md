# Datasheet Template

As far as you can, complete the model datasheet. If you have got the data from the internet, you may not have all the information you need, but make sure you include all the information you do have. 

## Motivation

- For what purpose was the dataset created? 

- Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?

No information to answer these questions, although what I can say is that they originate from Amazon and Stanford University is marked as a collaborator according to Kaggle.

## Composition

- What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)? 

The instances that comprise the dataset represent amazon user reviews.

- How many instances of each type are there? 

568 454

- Is there any missing data?

Not to the extent of my knowledge.

- Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by  doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?

Not to the extent of my knowledge. Someone may have leaked some degree of confidential information in a review they have written or in their username, but this would have to be verified by looking through the records manually, and is not specified from the source where which I downloaded the dataset (Kaggle).

## Collection process

- How was the data acquired? 

Unknown to me, but I'd assume it was given to the public by Amazon for research purposes.

- If the data is a sample of a larger subset, what was the sampling strategy? 

Whilst the dataset I downloaded was not, to my knowledge, a sample of a larger subset, in my individual project, I sampled the data to bring the number of reviews down to 30 000 for computational ease purposes, using stratified sampling.

- Over what time frame was the data collected? 

10 years.

## Preprocessing/cleaning/labelling

- Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section. 

Yes. I firstly sampled the data down to 30 000 records and then created a new data frame based only off reviews where the Score was 1 or 5. I then applied my clean_message() function to strip each review down only to words that be used in the sentiment analysis. These were then vectorised using a CountVectoriser.

- Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)?

Yes. 
 
## Uses

- What other tasks could the dataset be used for? 

Other tasks the dataset could be used for include conducting a k-means clustering analysis, going deeper from sentiment analysis and into emotional analyses. Fake review detection is another use case. These are just a few, the possibilities are endless.

- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms? 

Yes, if the dataset is used to produce information about a particular brand that is not true, but based off someones opinion, this could lead to legal trouble. Some reviews may also be fake or deliberately misleading.

To mitigate this, those who use this dataset must make sure to have solid transparency and explainability systems in place. For instance, if a model predicts that a particular brand of rice will make you sick, systems must be put in place to explain that this prediction arised from a customers review, and may not be true.

For fake and misleading reviews, one can implement systems to detect these, such as by assessing the review 'helpfulness' score and if done under ethical guidelines, assessing if that userID has a track record of consistently commenting fake and misleading reviews.


- Are there tasks for which the dataset should not be used? If so, please provide a description.

Yes, it shouldn't be used for product recommendations outside of food products. Any recommendations like this that occur come from a dataset specific to food reviews, and so the recommendation would be based off irrelevent information.

Adding to this point, quite obviously the data set shouldn't be used for non-food related sentiment analysis, since again the information would be irrelevent.

Since health and food are related in certain contexts, this dataset should not be used to produce health and medical analyses from this data, since inaccurate and damaging conclusions can easily occur.

## Distribution

- How has the dataset already been distributed? 

Through online repositories such as Kaggle and also on the Stanford website. There's probably more mediums of distributions where this dataset is available, but this escapes my knowledge.

- Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?  

No, it falls under public domain.

## Maintenance

- Who maintains the dataset?

No-one to the extent of my knowledge, I was unable to find this information. However, It was last updated 6 years ago. 

