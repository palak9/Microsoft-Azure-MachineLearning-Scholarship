# Microsoft Azure Machine Learning - Udacity Lesson 3 : Model Training


👉Data Import and Transformation : 
1. Data Wrangling - 
It is the process of cleaning and transforming data to make it more appropriate for data analysis. The process generally follows these main steps :
1. Explore data and check the quality of data
2. Transform raw data by restructuring, normalizing, cleaning. 
3. Validate and publish data. 

Data wrangling is an iterative process where you do some data transformation then check the results and come back to the process to make improvements. 

--- 

👉Managing Data: 
1. Datastores: It provides an access mechanism that is independent of the computer resource that is used to drive a machine learning process. They offer a layer of abstraction over supported Azure storage services. They store all the information needed to connect to a particular storage service. 

2. Datasets: They are resources for exploring, transforming, and managing data in Azure ML. It is essentially a reference that points to the data in the storage. It is used to get specific data files in the data stores. 

$ They are used to interact with your data in the datastore and to package data into consumavle objects.
$They are not copies of the data but references that pojt the original data. 
$ Once dataset is registered in Azure ML workspace, you can share it and reuse it across various experiments without data infection complexities. 

Three steps of the data access workflow are:
1. Create a datastore. - access services
2. Create a dataset. - Training the model
3. Create a dataset monitor - data drift.

Data Drift: Input data that you are feeding into your model is likely to change, this is what data drift is. They are problematic for model accuracy. Eg: if you train a model to detect soam in email, it may become less accurate as new types of spam arise that are different from the spam on which the model was trained. 
Hence Data monitors are used to detect data drift and other issues in your data. When a data drift is detected, you can have the system automatically update the input dataset so that you can retrain the model and maintain its accuracy. 

---

👉Introduciñg Features : 
Columns of the table can be referred to as features. 

Feature Engineering: 
- Initial features in the data are not enough to produce high quality trained ML models. So you can use feature engineering to derive new features based on the values of existing features. 
- Once you have the features, another important task is selecting the features that are most important or most relevant. This is feature selection. 
- ML algorithms cannot accommodate a large number of features, so it is often necessary to do dimensionality reduction. 
 $ Deep learning can be used for the implementation of certain feature engineering process (like embedding)

Examples of Feature Engineering: 
1. Aggregation - count/sum/average/mean/median.
2. Part-of - eg: date, you can consider date/month/year
3. Binning - group your entities and apply aggregations over bins like eg: age of the customer and then calculate average purchase by that particular age group/bin
4. Flagging- deriving boolean values. Eg: yes/no
5. Frequency-based - 
6. Embedding - Feature learning 
7. Deriving by example - tend to learn new feature values based on existing examples. 

---

👉Feature Selection :
There are mainly two reasons for feature selection.
1. Some features might be highly irrelevant or redundant. So it's better to remove them in order to improve performance. 
2. Many ML suffer from the curse of dimensionality, hence do not perform well when given a large number of variables/features. 

We can improve the situation of having too many features through dimensionality reduction. 
Techniques used are : 
1. PCA - their statistical approach
2. t-SNE - a probabilistic approach. Is used a lot to visualize the 3-dimensional data into 2 dimensional. This is used abundantly since it is extremely tough to visualize data with a higher number of dimensions.
3. Feature embedding - encodes a larger no of features into a smaller number of "super-features"

Azure ML prebuilt modules: 
1. Filter-based feature selection: identify columns in the input dataset that have the greatest predictive power. 

2. Permutation feature importance: determine the best features to use by computing the feature importance scores. 

---

👉Data Drift
Data drift is a change in the input data for the model. Which degrades the performance of the model and is one of the reasons that model performance gets worse over time. 
The process of monitoring for data drift involves: 
1. Specifying baseline dataset - training data
2. Specifying Target dataset - input data 
3. Comparing these two datasets over time, to monitor for differences. 

Types of comparisons you might want to make the monitoring for data. 
1. Comparing input data vs. training data - this is proxy for model accuracy, I.e an increased difference betwé the input vs training data is likely to result in a decrease in model accuracy. 
2. Comparing different samples of time - eg: a model trained on data collected during one season may perform differently when given data from another time of year. Detecting this seasonal drift in the data will alert you to potential issues with your model's accuracy. 

---

👉Model training basics : 
To give the model a set of input features X, and have it predict the value of some output feature Y.

Parameters and Hyperparameters: 
The major goal of model training is to learn the values of the model parameters. In contrast, some model parameters are not learned from the data. These are called hyperparameters and their values are set before training. 
Eg: no of layers in DNN, no of clusters, learning are of the model. 

Splitting the data: 
1. Training data - learn the values for parameters.  
2. Validation data - check performance on the validation data and tune the hyoerparameters until the model performs well. 
3. Test data - since we believe we have our finished model (parameters and hyperparameters) we will want to do final check of it's performance - and we need to do this on some fresh test data that we did not use during the training process!!!

---

👉Training Classifiers : 
- A classification problem occurs when the expected outputs are categorical (discrete)
- There are 3 main categories of classification problems : 
1. Binary classification 
2. Multi-class Single label classification: output belongs to only one class out of all the available classes.
3. Multi-class multi-label classification: output for observation can belong to more than one class out of the total number of classes available.

---

👉Training Regressors : 
A regression problem occurs when the expected outputs are numerical. 
There are 2 main categories of regression problems:
1. Regression to arbitrary values 
2. Regression to values between 0 and 1

---

👉Evaluation metrics for classification 
1. Confusion matrix 
- Precision 
- Recall
- Accuracy 
- f1score
- auc 

---

👉Evaluation metrics for Regression
1. R-Squared: how close the regression line is to the true values. 
2. RMSE: Square root of the difference of the squares between the predicted and actual values. 
3. MAE: Average of the absolute difference between each prediction and the true value. 
4. Spearman Correlation: Strength and direction of the relationship between predicted and actual values. 

---

👉Strength in Numbers:
No matter how well-trained an individual model is, there is still a significant chance that it could perform poorly. Hence rather than training one single model, you can train multiple models, capturing collective results. 
Two approaches : 
1. Ensemble learning
2. Automated machine Learning.

$ Ensemble Learning:
- It combines multiple ML models to produce one predictive model. 
There are three types of ensemble models:
1. Bagging / bootstrap aggregation-
- reduce overfitting
- random sampling
- Trained models are homogeneous
- the final reduction is an average from predicted models.

2. Boosting -
- reduces bias for models.
- same input data to train multiple models using different hyperparameters. 
- boosting trains model in sequence by training weak learners one by one, with each new learner correcting errors from previous learners. 
- final predictions are weighted average from the individual models.

3. Stacking - 
- Trains a large number of completely different models.
- Combines the output of individual models into a meta model that yields more accurate predictions 
