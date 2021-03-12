# Credit_Risk_Analysis
_Applying machine learning to solve a real-world challenge: credit card risk._


## Overview
Credit risk presents an classification problem for supervised machine learning models, namely that good loans (one class) far outnumber the risky loans (another clas) making it difficult to train a model to detect the risky loans. Without particular attention, a supervised machine learning model will simply train itself to pick up the good loans which does a business no good. Enter stage left, our hypothetical institutional client LendingClub, a peer-to-peer lending services company.  

To assist LendingClub with its issue identifying bad loans, I used imbalanced-learn and scikit-learn, two python machine learning libraries, to train six supervised machine learning models based on different resampling techniques. The six different machine learning methods used were as follows: 
- ROS
- SMOTE
- Undersampling
- SMOTEENN
- Balanced Random Forest Classifier
- Easy Ensemble Classifer

Below in the results section, I evaluate the performance of each of these models. And, in the summary section I recommend whether the models should be used to predict credit risk.

## Results

### ROS
##### Balanced Accuracy Score
![](/images/ROS_balanced_accuracy_score.png)

##### Imbalanced Classification Report
![](/images/ROS_classification_report_imbalanced.png)

### SMOTE
##### Balanced Accuracy Score
![](/images/SMOTE_balanced_accuracy_score.png)

##### Imbalanced Classification Report**
![](/images/SMOTE_classification_report_imbalanced.png)

### Undersampling
##### Balanced Accuracy Score
![](/images/Undersampling_balanced_accuracy_score.png)

##### Imbalanced Classification Report
![](/images/Undersampling_classification_report_imbalanced.png)

### SMOTEENN
##### Balanced Accuracy Score
![](/images/SMOTEENN_balanced_accuracy_score.png)

##### Imbalanced Classification Report
![](/images/SMOTEENN_classification_report_imbalanced.png)

### Balanced Random Forest Classifier
##### Balanced Accuracy Score
![](/images/BalancedRandomForestClassifier_balanced_accuracy_score.png)

##### Imbalanced Classification Report
![](/images/BalancedRandomForestClassifier_classification_report_imbalanced.png)

### Easy Ensemble Classifier
##### Balanced Accuracy Score
![](/images/EasyEnsembleClassifier_balanced_accuracy_score.png)

##### Imbalanced Classification Report
![](/images/EasyEnsembleClassifier_classification_report_imbalanced.png)

## Summary
I would recommend the Easy Ensemble Classifier model because it has a balanced accuracy score of ~92%. However, that model is so high relative to the others that I would recommend the second strongest model, the Balanced Random Forest Classifier at 78%, be deployed for now and waiting to deploy the Easy Ensemble Classifier model until a colleague can peer over it to ensure its accuracy. The Balanced Random Forest Classifier seems like the highest balanced accuracy score still in the sphere of the other scores. When something is too good to be true, it should be further inspected.

The Balanced Random Forest Classifier model also has the highest average recall at 1.0. This makes me confident that we are not entirely osing quality in our fraud detection model for the short time we are double checking our potentially outstanding model, the Easy Ensemble Classifier.
