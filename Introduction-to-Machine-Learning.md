# Microsoft Azure Machine Learning - Udacity Lesson - 2

---
👉Data Science Process -
1. Collect Data
2. Prepare Data
3. Train model
4. Evaluate model
5. Deploy model (retrain model)

---

👉Common types of data
$ It's all numerical in the end 
1. Numerical
2. Time-series eg: stocks
3. Categorical(discrete)
4. Text eg: news article 
5. Image

---

👉Tabular Data:
  Data that is arranged in a data table. Similar to the spreadsheet.
  
    1. Row - an item/entity
    2. Column - a property 
    3. Single value - cell

In ML we ultimately work with vectors 
Vector - an array of numbers or a nested array that contains other arrays of numbers.

- Khan Academy - Linear Algebra 

---

👉Scaling Data : 
Scaling data means transforming it So that the values fit within some range or scale, such as 0-100 or 0-1. 
Why scale the data? - to speed up the training process. 
Two approaches : 
1. Standardization - rescales the data to have mean = 0 and variance = 1. 

Variance - average of sqaured differences from the mean.

Standard deviation - sqaured root of variance = (x-mean)/standard-deviation 

2. Normalization - rescales the data into the range [0,1] = (x-xmin)/(y-ymin)

---

👉Encoding Categorical Data: 
Two approaches 

1. Ordinal encoding - convert the categorical data into integers ranging from 0 to (no of categories -1)
Drawback : implicitly assumes order across the categories which is meaningless. 

2. One hot encoding - convert each categorical value into a column. 

---

👉Image Data: 
**How to convert image into vectors?** 

**Each pixel can be represented by a vector of three numbers (RGB)**

- Encoding an Image: 
1. Horizontal position of each pixel.
2. Vertical position of each pixel.
3. Color of each pixel. 

Size of the vector = height*width*depth of that image. 
Each cell in the matrix represents the pixel value. 

---

👉Text Data:
- Normalization -
1. Lemmatization 
2. Tokenization 

- Vectorization - 
1. TFIDF
2. Word2Vec or GloVe

---

👉Two Perspectives on ML

1. Computer Science-
Input features -> Program -> Output = program(input features)

2. Statistical 
Mathematical function ->  Independent variables -> Dependent variables = f(independent var)

---

👉 Tools for ML:
Libraries- 
1. Scikit-Learn 
2. Keras 
3. Tensor flow
4. PyTorch 

Development Environments - 
1. Jupyter Notebooks
2. Azure Notebooks 
3. Azure Databricks 
4. Visual Studio Code
5. Visual Studio

---

👉Libraries for ML

I. Core frameworks and Tools:
1. Python
2. Pandas
3. Numpy
4. Jupyter notebook

II. ML and DL
1. Scikit learn
2. Apache spark
3. Tensorflow
4. Keras 
5. PyTorch

III. Visualization
1. Plotly
2. Seaborn
3. Matplotlib
4. Bokeh
