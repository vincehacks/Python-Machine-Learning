# ML Training

Created by Vince Chang </br>

Instructor: Tim Fox </br>
Email: tfox@elephantscale.com

- Using Anaconda to toggle and manage different environments for Python


#### How to Install Packages
- Two Package Management Repositories:
	- 1. PyPi: Python Package Index
		- Works on any distribution of Python
	- 2. Anaconda: Anaconda packages
		- Only works in Anaconda

- Two Package Management Tools (From the command line):
	- 1. `pip`: Install packages from PyPI
		- ex. `pip install MYPACKAGENAME`
	- 2. `conda`: Install packages from anaconda
		- ex. `conda install -c conda-forge MYPACKAGENAME`


# Python
- General purpose, object-oriented, dynamic programming language
- Python is also **language & environment** for data science computing and
graphics
- Open source
- Rich ecosystem (lots of libraries)
- Great for modeling, machine learning ,ad-hoc analytics
- Used by developers, scientist, and data scientist


#### Why Python
- **Comprehensive**: can do a lot of analysis
- **State-of-the-art graphics capabilities**
- **Designed for interactive analysis**: no time consuming, supports scripting
- **Open Source**: commercial packages costs $$$
- Python can import from variety of formats (csv, excel, db)
- Python is extensible: thousands of libraries in PyPi (open source)
- Free IDEsL Spyder, Pycharm


#### Python History
- Created by Guido Von Rossom in 1991
- Dynamically Typed Language: automatic type conversion
- JIT (just in time): code compiles and runs in real time


#### Python Use Cases
- Web programming
- Microservices
- System Automation Tasks
- Scientific Programming
- Data Analysis / Data Science
- ML / AI


# Machine Learning Primer


#### Advantages
- Accurate: ML can learn from data, the more data it learns from the better it
gets
- Automated: Bulk of the decisions can be automated
- Fast: ML can process data within milliseconds
- Customizable: ML algorithms can be adopted for various scenarios
- Scalable: ML algorithms can scale for large amount of data


#### Challenges
- Data Prep: Data may not be ready-to-use form
- Accuracy: Measuring accuracy can get complicated
- Algorithm Choice: Different algorithms perform differently, choosing the
best algorithm us very important


#### Deep Learning
- Uses Neural networks techniques
- ex. Google Translate
- ex. Face Recognition
- requires a lot of data


#### ML vs. Deep Learning
- **ML**
	- Good for small data
	- Doesn't scale with large amount of data
	- Doesn't need a lot of compute power
	- Mostly CPU bound
	- Features needs to specified manually (by experts)
	- Training usually takes seconds, minutes, hours
	- Easy to interpret
- **Deep Learning**
	- Need large amount of data for reasonable performance
	- Scales well with large amount of data
	- Needs a lot of compute power(usually runs on clusters)
	- Can utilize GPU for certain computes(massive matrix operations)
	- DL can learn high level features from data automatically
	- Training takes longer (days
	- Hard to understand the final result


#### How to do ML
- Collect Data: More data, the better the algorithms become. This data can
come from internal logs or external sources
- Prepare Data: Raw data is hardly in a form to be used. It needs to be
cleansed, tagged and curated before ready to use
- Train a model: Feed the training data to model so it can learn
- Evaluate the model: Test the model accuracy
- Improve the model: Either by adding more training data, choosing a different
algorithm, etc.


#### Types of ML
- **Supervised ML**: ***all about training***
	- Mode is "trained" with human labeled training data
	- Model is testing on test data to see performance
	- Model can be applied to unknown data
	- Ex. Classification (Spam or not), regression(stock market), decision trees(
	fraud detection)
	- Ex. Predicting the stock market = we have the data already, predict trends
	- ***Model learns from (Training data)***
	- ***Then Predicts on 'unseen' data***
- **Unsupervised ML**: ***all about inference***
	- Model tries to find natural patterns in the data
	- No human input expect parameters of the model
	- Ex. Clustering news stories = cluster similar data to make predictions
	based of the patterns we see
	- Ex. Group Uber trips, Cluster DNA data
	- ***No training needed***
	- ***Algorithms tries to find patterns in data***
- **Semi-Supervised Learning**:
	- Model is trained with a training set which contains unlabeled and labeled
	data
	- Ex. Large images archive only a few of them are labeled and a majority are
	unlabeled


# Scikit-Learn Intro
- Provides a lot of algorithms


#### Clustering
- There are many different clustering algorithms for vectors
- Simplist is k-means
- K-means requires a known value of k (number of clusters) to start with


#### K-Means Clustering
- K-Means: Simplest Clustering Algorithm
- **Step 1**: k numbers of points (centroids) are pre-seeded in the data
- **Step 2**: Each point in the dataset is associated with its nearest centroid
as determined by a distance measurement 
- **Step 3**: The centroid (geometric center) of the clustered points
becomes the new centroid of that cluster. Each centroid is updated
- **Step 4**: Repeat steps 2 and 3 until convergence is reached (the points
move less than the threshold amount)


#### K-Means Clustering Summary
- Easy to parallelize
- **Disadvantages**:
	- Values of k must be known in advance, which may mean running the exercise
	many times to get good results
	- Initial centroid positions are important; may cause long convergence
	- Dense grouping of points are not especially considered (outliers = bad)
	- Clusters not broadly (hyper)spherical don't work well for k-means