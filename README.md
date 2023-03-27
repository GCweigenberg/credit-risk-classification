# credit-risk-classification
Credit-Risk Analysis

Credit Analysis Report

The purpose of this credit-risk analysis was o use various techniques to train and evaluate a model based on loan risk. We used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers. In the module, the dependen variable (y-value) was the "loan status" which indicated whether a loan was healthy or high risk. The independent variables (x-values) were "loan size", "borrower income", "interest rate", "debt to income" ratio, "number of accounts", and "derogatory marks". 

Here is the process we took: 
  - Split the Data into Training and Testing Sets
  - Create a Logistic Regression Model with the Original Data
  - Predict a Logistic Regression Model with Resampled Training Data
  
 Results:
 
 Original data Logistic Regression:
 
 balanced_accuracy_score: 0.9520479254722232
                   precision    recall  f1-score   support

  healthy loan 0       1.00      0.99      1.00     18765
high-risk loan 1       0.85      0.91      0.88       619

        accuracy                           0.99     19384
       macro avg       0.92      0.95      0.94     19384
    weighted avg       0.99      0.99      0.99     19384
    
 Re-Sampled data Logistic Regression:
  
Balanced Accuracy Score: 0.9936781215845847
                   precision    recall  f1-score   support

  healthy loan 0       1.00      0.99      1.00     18765
high-risk loan 1       0.84      0.99      0.91       619

        accuracy                           0.99     19384
       macro avg       0.92      0.99      0.95     19384
    weighted avg       0.99      0.99      0.99     19384
    
    
Final Report:
Logistic regression models work on a scale from 0.0 to 1.0. All data returned must fall between those two values. The original data model returned near perfect precision and recall scores for healthy loans. Whereas the scores returned for the high-risk loans were not as high. The balanced accuracy score was 0.952, which is poor considering the imbalanced dataset we are working with. Accuracy is not a reliable output for imbalanced datasets.
Regarding the re-sampled data, The precision and recall stayed the same for our healthy-loan predictions. And the recall for the high-risk loan prediction improved to near perfect prediction. This means that our test was great at predicting positives. The precision for the re-sampled data stayed the same for healthy loans, while, unfortunately, decreasing for the high-risk loans. This is not good to see because it means that our model was maybe too good at predicting positives. Lastly, the balanced accuracy score was .993, a good improvement 
To conclude, I believe the re-sampled data came through with good results. However, I cannot in good faith recommend the model on the basis of the greatly outweighed dataset. I beleive the model was too good at predicting positives outcomes due to the high number of healhy-loan (low risk). This returned heavily biased results that favored positive predictions.
    
   
