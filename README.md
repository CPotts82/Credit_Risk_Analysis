# Credit_Risk_Analysis
## Overview
In this analysis six different supervised machine learning models were explored and analyzed in order to evaluate their ability to detect credit risks.  Credit risk data is a highly imbalanced set of data due to the fact that low risk credit far outweighs high risk credit.  There are more opportunities for good loans than for bad ones but the high credit risks can be detrimental if they fall through.  The purpose of the machine learning models is to help predict which credit risks are high out of the mostly low risk dataset. Due to the fact that this is such an imbalanced dataset, various resampling techniques were explored. 
### Purpose/Background
The dataset for this analysis comes from LendingClub and was analyzed using multiple types of resampling techniques. Machine learning models were trained with the LendingClub dataset and then evaluated on their performance. Key metrics that were focused on were: accuracy score, precision, sensitivity, and F1 score. A confusion matrix was also generated for each model. This matrix identifies the number of ACTUAL high and low credit risks vs the PREDICTED number of high and low credit risks. 

Metric Definitions:
- Accuracy - the number of predictions the model predicted correct, both high and low credit risks.
- Precision - the measure of how Reliable a Positive classification/high credit risk identification is.
- Sensitivity - (also called recall) is the ability of classifiers to find ALL high credit risks. 
- F1 Score - combines precision and mean into one metric. 

## Resources:
Jupyter Notebook, SciKit-learn libraries, imbalanced-learn libraries, Pandas, Python

data: https://help.lendingclub.com/hc/en-us/articles/215488038-What-do-the-different-Note-statuses-mean-

## Results

The results of this analysis focus on the accuracy, precision, recall, and F1 scores (as defined above) for each model. There were 4 different resampling techniques applied: oversampling, undersampling, combination sampling and ensemble learning. The results for each model are shown below. 

### OverSampling Models:
### Naive Random Oversampling:
- Accuracy Score - 62.9%
- Precision - 99.0%
- Recall/Sensitivity - 68.0% 
- F1 Score - 81.0%
- Image:

![NR_Oversampling](https://user-images.githubusercontent.com/106348899/194399649-8fe8d10f-49af-43a3-aadb-18d36c39a7ba.png)

### SMOTE: 
- Accuracy Score - 62.2%
- Precision - 99.0%
- Recall/Sensitivity - 66.0%
- F1 Score - 79%
- Image:

![SMOTE Oversampling](https://user-images.githubusercontent.com/106348899/194399900-2506bbe7-3eee-4152-ac73-e9a87b0afe01.png)

### UnderSampling Model:
### Cluster Centroids Resampler:
- Accuracy Score - 50.6%
- Precision - 99.0%
- Recall/Sensitivity - 42.0%
- F1 Score - 59.0%
- Image:

![CC_Undersampling](https://user-images.githubusercontent.com/106348899/194400093-8ccee62e-1407-4ec9-8949-5d863f7eacf8.png)

### Combination Sampling Model:
### SMOTEENN:
- Accuracy Score - 62.7%
- Precision - 99.0%
- Recall/Sensitivity - 59.0%
- F1 Score - 74.0%
- Image:

![SMOTEENN_Combo](https://user-images.githubusercontent.com/106348899/194400264-334d4ab8-14ec-4594-8762-c180e9607f07.png)

### Ensemble Learner Models
### Balanced Random Forest Classifier:
- Accuracy Score - 78.8%
- Precision - 99.0%
- Recall/Sensitivity - 91.0%
- F1 Score - 95.0%
- Image:

![BRF](https://user-images.githubusercontent.com/106348899/194400408-d164a721-a78f-4259-8af6-7afc402d7c9a.png)

### Easy Ensemble AdaBoost Classifier:
- Accuracy Score - 92.5%
- Precision - 99.0%
- Recall/Sensitivity - 94.0%
- F1 Score - 97.0%
- Image:

![EE](https://user-images.githubusercontent.com/106348899/194400552-72753ba5-3118-4165-9746-8678d2616828.png)

## Summary
### Overview
Comparing the key metrics across all six machine learning models, the Ensemble Learning models performed the best out of the models analyzed. Specifically, the Easy Ensemble AdaBoost Classifier performed the best with accuracy, recall and F1 scores ranging from 92% to 97%. The Balanced Random Forest Classifier ranked second with very high F1 and recall scores and an accuracy score of 78.8%.  The Undersampling technique used here, Cluster Centroids Resampler performed the poorest out of all the models. The Cluster Centroids Resampler only predicted half of the test dataset correctly. Low accuracy score along with low recall and F1 scores make this a terrible model for credit risk analysis. Both of the Oversampling techniques, Naive Random Oversampler and SMOTE had mediocre results along with the Combination Resampling technique, SMOTEEN. Each of these three techniques had accuracy scores around 63% with relatively decent F1 Scores. Recall for SMOTEEN was low at 59% which means there are too many false negatives being predicted. Precision was not factored in to the ranking of the models because all six models scored 99% for precision. The precision is high in each model because of the skewed dataset. There are far more low credit risks than high and the model was excellent at identifying low risks.  
### Recommendations
My recommendation is to utilize the Easy Ensemble AdaBoost Classifier first and foremost to predict credit card risk. This model performed really well overall. The Ensemble Learner, Balanced Random Forest Classifier was a fairly good model but could be an even better model with a little more training in high credit risk data. This model needs a very little bit of fine tuning.  My only other recommendation would be to check the data and see if it may need a little more cleaning. As far as the resampling goes, The Ensemble Learners performed best with this dataset. I would not recommend working with any of the Oversampling or Combination sampling models for fear of overfitting. 
