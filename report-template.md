# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

The purpose of the analysis was to build a model that could predict the creditworthiness of borrowers based on certain fearures.

The data was retrieved from peer-to-peer lending services. It contained features and outcomes for the following categories: loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, total_debt,loan_status. Using a sample from the dataset to create a model that could predict the same outcomes as in the data accurately.

The model tries to predict the loan status of borrowers where 0 represents a healthy loand and 1 represents a high risk loan.

To create the model, the cleaned data was imported into a pandas dataframe. The known outcomes were then separated from their corresponding features by copying the outcomes into a new series and dropping the column from the original dataset. These were divided into training and testing sets. The model was trained(learned) on the training set and its accuracy was verified with the testing set. Lastly, a confusion matrix and a classification report were used to determine the accuracy of the model; how well the model was able to learn from the data.

The logisticregression was used to train the model with the maximum iterations set to 200. The trained model was then used to predict the results of the sample. The predicted results were compared with the actual outcomes to determine the performance of the model.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

Precision: All predictions made for Class 0, 100% were correct. The model is perfect in identifying instances of Class 0. Out of all the instances where the model predicted Class 1, 87% were correct. There are some false positives.
Recall: The model correctly identified all actual instances of Class 0. The recall of 1.00 means that the model found 100% of the true positives for Class 0. The model correctly identified 95% of the actual Class 1 instances. This means it missed 5% of the true positives.
Accuracy: 0.99
Meaning: 99% of all predictions made by the model were correct. This metric represents the overall correctness of the model.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

The average precision across both classes is 94%.
The model's average ability to find true positives across both classes is 97%.
In this model, the high precision and recall scores for Class 0 reflect strong performance on the majority class, while slightly lower scores for Class 1 indicate some difficulty in correctly identifying the minority class. However, the model's overall accuracy of 99% suggests it performs well across the dataset, mainly due to the large number of samples in Class 0.

If you do not recommend any of the models, please justify your reasoning.
I do not recommend the model because even though it could predict 85% accurately. I think issuing 15% high risk loans could cost financial institution a lot.
