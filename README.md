# Credit_Risk_Analysis
## Overview
### Purpose/Background
### Overview of Data and what we are looking for. Define - accuracy, precision, recall, F1 score and Confusion Matrix. Define types of resampling.

## Resources:
Jupyter Notebook, SciKit-learn libraries, imbalanced-learn libraries, Python

data: https://help.lendingclub.com/hc/en-us/articles/215488038-What-do-the-different-Note-statuses-mean-

## Results

The results of this analysis focus on the accuracy, precision, recall, and F1 scores (as defined above) for each model. There were 4 different resampling techniques applied: oversampling, undersampling, combination sampling and ensemble learning. The results for each model are shown below;

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
### Recommendations
