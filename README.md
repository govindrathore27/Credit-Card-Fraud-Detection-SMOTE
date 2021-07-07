# Credit-Card-Fraud-Detection-SMOTE
- In this dataset , the data is highly imbalanced towards the "Not Fraud" class. As it is more frequent event than the event of "Fraud" occuring. 
- As in this case we can not use accuracy in this case as getting a high accuracy will be a piece of cake because a model which just classifies every test case as "Not Fraud" will get very good accuracy.
- So  accuracy is disqualified as **evaluation metric**. Rather we will use **Recall** as it will focus on decreasing **False Negatives** .
- TP -> transactions which are actually fraudulent and the model also able correctly identify them as fraudulent transactions
- FP -> transactions which are actually non fraudulent transactions but the model is predicting them as fraudulent transactions
- TN -> transactions which are actually non fraudulent transactions and model is also predicting them as non fraudulent transactions
- FN -> transactions which are actually fraudulent but the model is predicting them as non fraudulent transactions
![](https://miro.medium.com/max/1400/1*pOtBHai4jFd-ujaNXPilRg.png)

## For handling this type of data , we uwse **Resampling** to create more data for miniority class , so as to create a balanced dataset.
The imbalanced datasets are generally biased towards the majority class of the target variable. In this case the majority class is non fraudulent transactions and the minority class is fraudulent transactions. Hence if we don't balance these two classes the machine learning algorithms will be biased towards the majority class. Therefore it becomes important to balance the classes present in target variables. There are two ways in which we can balance these two categories - 

- **Undersampling**: In undersampling we randomly select as many observations of majority class as we have for minority class to make both of these classes balanced
- **Oversampling**: In oversampling, we create multiple copies of minority class to have same number of observations as we have for majority class. Here also we can oversampling in two ways - 
    - **Minotiy Oversampling**: here we create duplicates of same data from minority class
    - **SMOTE (Synthetic Minority Oversampling Technique)**: here we create observations for the minority class, based on those that already exist. It randomly picks a point from the minority class and computes the k-nearest neighbors for this point. The synthetic points are added between the chosen point and its neighbors.
