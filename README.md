# credit-risk-classification


<h2>Supervised Machine Learning Challenge</h2>

<h3>Overview</h3>
<hr/>

<p> 
The main objective of this assignment was to use a logistic regression machine learning model to predict whether a loan event is classified as a healthy loan or a high-risk loan. The dataset, "lending_data," includes key loan characteristics such as "loan_size," "interest_rate," "borrower_income," "total_debt," and others.

To build the model, I followed the four main steps of machine learning: preprocessing, training the model, validation, and prediction. In the final step, I evaluated the model’s performance by generating a confusion matrix and a classification report.

During the preprocessing stage, I loaded the data and separated it into features (X) and the target variable (y), where loan_status was the binary outcome to be predicted. The value counts for loan_status were: 0 (healthy loans) – 75,036 instances, and 1 (high-risk loans) – 2,500 instances. I then split the data into training and testing sets using an 75%-25% ratio with train_test_split.

In the training stage, I fit the training data (X_train and y_train) into the logistic regression model, which is designed to predict binary outcomes. The two possible outcomes in this case were a healthy loan (0) or a high-risk loan (1). Afterward, I validated the model by reviewing its accuracy score.

Finally, I used the model and the test feature set (X_test) to make predictions. To assess the performance of the model, I generated a confusion matrix and a classification report, which provided metrics like precision, recall, and overall accuracy.
</p>

<hr/>

<h3>Evaluation</h3>

<h4>Accuracy Score</h4>
Accuracy is the ratio of correctly predicted observations to the total overvations. In the evaluation, I got the score 0.99 (99.2%), which means the model correclty classifies both healthy and high-risk loans.

<h4>Precision</h4>
Precision is the ratio of correctly predicted positive observations to the total predicted positive overvations. The precision score for high-risk laons (label 1) is 0.84 (84.1%), this answers the question "Of all the loans predicted as high-risk how many are actually high-risk?." In other words, the model predicts a loan as high-risk, it's correct about 84% and 1.00 (99.8%) for healthy loans (label 0), which means the model correclty classifies healthy loan 99.8%.

<h4>Recall</h4>
Recall is the ratio of correctly predicted positive observations to all predicted overvations for that class. The recall score for high-risk laons (label 1) is 0.94 (94.2%), this means that the model correctly identifies 94.2% of all actual high-risk loans. Recall for healthy loans (label 0) is 99.4%, which means that the model correctly identifies 99.4% of all actual healthy loans.

<hr/>

<h3>Summary</h3>

<h4>Justification for Recommendation:</h4>
The model performs exceptionally well in predicting healthy loans, with 99.8% precision and 99.4% recall, ensuring that the vast majority of loan applications are correctly classified as healthy. Its 94.2% recall for high-risk loans is strong, meaning most high-risk loans are accurately identified, which is crucial for minimizing financial risk. Additionally, the model’s 99.2% overall accuracy provides reliable predictions across both healthy and high-risk loans. While the precision for high-risk loans is lower at 84.1%, resulting in some healthy loans being misclassified as high-risk, this can be mitigated based on the company’s tolerance for false positives.

<h4>Recommendation:</h4>
I recommend this model for use by the company, as its strong overall performance ensures reliable predictions, especially for healthy loans. However, attention should be given to reducing false positives by fine-tuning the model or adjusting decision thresholds for high-risk loans to improve precision. This approach will help ensure that the model balances the detection of high-risk loans with the minimization of unnecessary rejections.