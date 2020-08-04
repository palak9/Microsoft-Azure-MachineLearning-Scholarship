# Microsoft Azure Machine Learning by Udacity Lesson 5: Managed Servies for Machine Learning

The machine learning process can be labor intensive. Machine learning requires a number of tools to prepare the data, train the models, and deploy the models. Most of the work usually takes place within web-based, interactive notebooks, such as Jupyter notebooks. Although notebooks are lightweight and easily run in a web browser, you still need a server to to host them. Typically, this involves installing several applications and libraries on a machine, configuring the environment settings, and then loading any additional resources required to begin working within notebooks or integrated development environments (IDEs).

All this setup takes time, and there is sometimes a fair amount of troubleshooting involved to make sure you have the right combination of software versions that are compatible with one another. This is the advantage of managed services for machine learning, which provide a ready-made environment that is pre-optimized for your machine learning development.

---

👉  Intro to the Managed Services Approach :

1. Conventional ML
- Lengthy installations and set up 
- Expertise to configure hardware 
- A fair amount of troubleshooting 

2. Managed Services Approach : 
- Very little set up 
- Easy configuration for any needed hardware. 

---

👉 Examples of compute resources :
1. Training clusters
2. Inferencing clusters
3. Compute instances 
4. Attached compute
5. Local compute 

---

👉 Compute Resources 
- A compute target is a designed compute resource or environment where you run training scripts or host your service deployment. There are two different variations on compute target :
1. Training compute targets
2. Inferencing Compute targets 

Inference refers to the process of using a trained Machine Learning algorithm to make a prediction. 

- Training clusters: use for training and batch inferencing. 
1. Single or multi-node cluster 
2. Can auto-scale each time you submit or run. 
3. Automatic cluster management and job scheduling.
4. Support for both CPU and GPU resources

- Inferencing Compute : 
1. After you have trained your model and you are ready to put it to work, deploy it to a web hosting environment or IoT device. 
2. When you use your model, it infers about the new draw it is given, based on it's training.

---

👉 Basic Modeling : 
- Training,  evaluating, and selecting the right ML models are at the core of each modern data science process. 
1. Experiment: Before you create a new run, you must first create an experiment. An experiment is a generic contact for handling runs. Think about it as a logical entity you can use to organize your model training process. 

2. Runs: Once you have an experiment, you can create runs within that experiment. Model training runs are what you use to build the trained model. A run contains all artifacts associated with the training process like output files, metrics, logs, and a snapshot of the directory that contains your scripts. 

3. Models: A run is used to produce a model. Essentially, a model is a piece of code that takes input and produces output. To get a model, we start with a more general algorithm. By combining this algorithm with the training data - as well as by tuning the hyperparameters - we produce a more specific function that is optimized for the particular task we need to do. 
Model = algorithm + data + hyperparameters 

4. Model Registry: Once we have a trained model, we can turn to the model registry, which keeps track of all models in an Azure ML workspace. Note that models are either produced by a Run or originate from outside of Azure ML.

---
