# Scotiabank Data Science DIscovery Days hackathon 


This hackathon project aimed to tackle the issue of credit card fraud, which had become a significant problem in Canada due to the widespread use of credit cards and the increase in online transactions during the Covid-19 pandemic. The challenge for this project was to build a new fraud detection model that could accurately identify fraudulent transactions and provide insights and recommendations on how to prevent fraud in the future. The team was required to analyze historical and publicly available data to develop the model and conducted statistical/business analysis to answer questions related to fraud prevention.


We used XGBoost–an implementation of gradient-boosted-decision trees. The data
was imbalanced - (2.4% of transactions are fraudulent), causing baseline XGBoost F1 to suffer
due to low recall.
We tried two approaches to improve recall. First, SMOTE applied data augmentation to
the minority class, balancing the number of examples in each class. Next, we used
Thresholding to search for the optimal prediction threshold to maximize F1 score on a
validation set.
We found that thresholding works better and combining them does not help.
