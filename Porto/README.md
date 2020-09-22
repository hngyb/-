# Porto Seguro's Safe Driver Prediction 
Bert Carremans님의 "[Data Preparation & Exploration](https://www.kaggle.com/bertcarremans/data-preparation-exploration "")" Kernel 내용을 클론 코딩해보며, Binary Classification을 학습함.   
[Data link](https://www.kaggle.com/c/porto-seguro-safe-driver-prediction/data "")
## Description
Nothing ruins the thrill of buying a brand new car more quickly than seeing your new insurance bill. The sting’s even more painful when you know you’re a good driver. It doesn’t seem fair that you have to pay so much if you’ve been cautious on the road for years.   

Porto Seguro, one of Brazil’s largest auto and homeowner insurance companies, completely agrees. Inaccuracies in car insurance company’s claim predictions raise the cost of insurance for good drivers and reduce the price for bad ones.   

In this competition, you’re challenged to build a model that predicts the probability that a driver will initiate an auto insurance claim in the next year. While Porto Seguro has used machine learning for the past 20 years, they’re looking to Kaggle’s machine learning community to explore new, more powerful methods. A more accurate prediction will allow them to further tailor their prices, and hopefully make auto insurance coverage more accessible to more drivers.   
## Evaluation
### Scoring Metric
Submissions are evaluated using the __Normalized Gini Coefficient.__   

During scoring, observations are sorted from the largest to the smallest predictions. Predictions are only used for ordering observations; therefore, the relative magnitude of the predictions are not used during scoring. The scoring algorithm then compares the cumulative proportion of positive class observations to a theoretical uniform proportion.   

The Gini Coefficient ranges from approximately 0 for random guessing, to approximately 0.5 for a perfect score. The theoretical maximum for the discrete calculation is (1 - frac_pos) / 2.   

The Normalized Gini Coefficient adjusts the score by the theoretical maximum so that the maximum score is 1.   

The code to calculate Normalized Gini Coefficient in a number of different languages can be found in this forum thread.
## Data Description
In this competition, you will predict the probability that an auto insurance policy holder files a claim.   

In the train and test data, features that belong to similar groupings are tagged as such in the feature names (e.g., ind, reg, car, calc). In addition, feature names include the postfix bin to indicate binary features and cat to indicate categorical features. Features without these designations are either continuous or ordinal. Values of -1 indicate that the feature was missing from the observation. The target columns signifies whether or not a claim was filed for that policy holder.
