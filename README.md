# ANN_Churn_Modelling
Using Artificial Neural Network to classify Churning Customers 


Artificial Neural Network: Customer Churning Model

Introduction
The aim of the project to classify the Churning Customers based on various features related to the bank. In this model, I applied Artificial Neural Network using “Keras” package (working on “Tensorflow” backend) to classify the “Exited” customer. Later, I also applied XGBoost Classifier to speed up the process and compare their accuracies.

Dataset:
Dataset consist of 12 features and one target variable.

Features are as follows:
1. CustomerId: Customer Id, int
2. Surname: string
3. CreditScore: Credit Score of customer, int
4. Geography: France, Spain or Germany, qualitative
5. Gender: Male or Female, qualitative
6. Age: Integer
7. Tenure: For how long customer is associated with the bank, int
8. Balance: float
9. NumOfProducts: Number of products customer has such as debit card, number of policies, etc, int
10. HasCrCard: Has credit card or not, 0 or 1
11. IsActiveMember: Is an active member in the past 6 months, 0 or 1
12. EstimatedSalary: Salary of the customer, float

Target Variable:
Exited:  0 or 1

Model Building Steps;
1. Importing the dataset and partitioning it into Features and Target variable.
2. Converting categorial variable: Geography and Gender into dummies.
3. Dropping unnecessary features such as CustomerID and Surname
4. Using train test split to split the data
5. Feature scaling was done using StandardScaler function.
6. Build Artificial Neural Network input layer using Sequential function in Keras.
7. First layer consist of 11 number of nodes same as the number of features in our model.
8. Two Hidden layers were built that consist of 6 nodes each (average of input layer nodes and output layer node). Hidden layer is activated by using ‘Rectifier function’.
9. Output layer consist of one node and is activated using ‘Sigmoid Function’.
10. 'adam' is used as an Optimizer and Binary Crossentropy is used as loss function.
11. Model was trained on taking batch of 10 observation and running it for 100 epochs.
12. Finally Classification Reports and Confusion matrix was generating resulting in f1 score of 82% and accuracy of 84.6%.
13. Also, I applied XGBoost Classifier on the same dataset that resulted in slightly better accuracy of 86.29%.

