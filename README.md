# Loan-Approval-Status for banking system
# Objective
Here the loan approval machine learning algorithm should be trained. The main objectve is to minimize the false positives i.e; the approval of bad loans must be avoided at any cost with minimum loss of opportunity.
# Preprocessing
Data is taken and insights on the data were obtained using pandas library. Null values were dropped, Categorical variables are replaced by Dummy variable. Drop first is used to aviod Diummy variable trap. Normalization of numerical data is done using standard scaler. Dependent and independent variables are saperated. Data is split into train and test data.
# Model Building
Since it's a problem with binary output Logistic Regression model was trained. Predictions of the test data were obtained
# Model evaluation
Here is the crucial part of the model building i.e; to minimize the approval of the bad loans. Correct evaluation metrics to be chosen so that the minimum approval of bad loans and minimum loss of oppotunity. By default 0.5 is the threshold in the  Logistic model. So we build the custom model where we can adjust the threshold of the model manualy. So we proposed an conditional statement on the probabilities of the outcome of the Logistic Regression model. Even though the accuracy has come down significantly we are intrested in precision. Precision is very high in the model
# Threshold Selection
To select the best threshold we make use AUC of the ROC curve. The best threshold is selected with minimum loss of opportunity. The curve shows that to apprive 98% of the good loans the 40% of the bad loans woll also be approved. To minimize the approval of bad loans threshold is selected accordingly.
