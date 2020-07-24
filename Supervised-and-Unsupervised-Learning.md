# Microsoft Azure Machine Learning by Udacity - Lesson 3 : Supervised and Unsupervised Learning

👉Supervised Learning : Classification 
There are several main approaches, which differ based on how many classes or categories are used, and whether each output can belong to only one class or multiple classes. 
Types of classification problems:
1. Classification on tabular data- The data is available in the form of rows and cloumns.
2. Classification on image or sound data- The training data consists of images or sounds whose categories are already known. 
3. Classification on Text data- The training data consists of texts whose categories are already known. 

👉Categories of Algorithms: 
1. Two-class classification : predict between two categories.
Eg: 1. Two-class SVM
       2. Two-class Averaged Perceptron
       3. Two-class Decision Forest
       4. Two-class Logistic Regression 
       5. Two-class Boosted Decision Tree
       6. Two-class Neural Network
2. Multi-class single-label classification : multiple categories, output belongs to single category. 

3. Multi-class Multi-label classification : multiple categories, output belongs to multiple categories. 

👉Supervised Learning: Regression
Types of Regression problems:
1. Regression on tabular data 
2. Regression on image data
3. Regression on text data

Categories of Regression :
1. Linear Regression - Fast training, linear model
2. Decision Forest Regression - Accuarte, fast training times. 
3. Neural Net Regression - Accurate, long training times. 

$ Linear Regression - linear relation between independent variables and numeric outcome.
Approaches: 
I. Ordinary least squares method.
II. Gradient descent.

$ Decision Forest Regression - 
- Ensemble learning method using multiple decision trees.
- Each tree outputs a distribution as a prediction. 
- Aggregate to find a distribution closest to the combined distribution. 

$ Neural Network Regression - 
- supervised learning method 
- label column must be numerical data type
- input layer + one hidden layer + output layer

👉Automate the Training of Regressors

- Conventional Machine Learning process:
1. Features available in the dataset.
2. Suitable Algorithms.
3. Hyperparameters tuning.
4. Evaluation metrics. 

👉What is automated ML? 
$ Intelligently test multiple algorithms and hyperparameters in parallel and return the best one
- Ready models can be either deployed into production or 
- Can be further customized or refined. 

👉The Automated ML Process : 

- User input > automated ML > Leader board
    
1. User input can be Dataset, Target metric Or constraints. 
2. Automate ML will have iterations having features + algorithm + hyper parameters along with training score of every iteration.  
3. Leader board will display the best suited algorithms.  

👉Unsupervised Learning :
- Algorithms learn from unlabeled data by looking for hidden structures in the data.  
- Obtaining unlabeled data is comparatively inexpensive and unsupervised learning can be used to uncover very useful information in such data.  
- Eg : we can use clustering algorithms to discover implicit grouping within the data,  or use association algorithms to discover hidden rules that are governing the data.  

Types of Unsupervised Learning Approaches : 

1. Clustering : Organizes entities from the input into a finite number of subsets or clusters. 

2. Feature Learning : Transforms input into other inputs that are potentially more useful in solving a given problem. 

3. Anomaly detection : Identifies two major types of categories i.e normal and abnormal (anomalies). 

👉Semi - supervised Learning : 
- Semi supervised learning combines the supervised and unsupervised approaches,  typically it involves having small amounts of labeled data and large amounts of unlabeled data. 
- Sometimes fully labeled data cannot be obtained,  or is too expensive -but at same time it may be possible to get partially labeled data.  This is where semi-supervised learning is useful. 

👉Clustering : 
- Clustering is the problem of organizing entities from the input data into a finite number of subsets or clusters,  the goal is to maximize both intra-cluster similarity and inter-cluster differences. 

Clustering algorithms :
1. Centroid based clustering
2. Density based clustering
3. Distribution based clustering
4. Hierarchical clustering
