---
title: "Some Notes on scikit-learn"
date: 2016-05-12
---

# Some Notes on scikit-learn

There are many machine learning frameworks, but the one I like most is [scikt-learn](http://scikit-learn.org/stable/). If you use [Anaconda python](https://www.continuum.io/downloads), it is really easy to setup. So here are some quick notes: 

## How to setup a very basic training?

Here is a very simple example:

` from sklearn import svm #Import SVM`

` from sklearn import datasets #Import Dataset, we will use the iris dataset `

`clf = svm.SVC() #setup a classifier`

`iris = datasets.load_iris() #load in a database`

`X, y = iris.data, iris.target #Setting up the design matrix, i.e. the standard X input matrix and y output vector`

`clf.fit(X, y) #Do training`

`from sklearn.externals import joblib` `joblib.dump(clf, 'models/svm.pkl') #Dump the model as a pickle file.`

Now a common question is what if you have different type of input? So here is an example with csv file input. The original example come from [machinelearningmastery.com](http://machinelearningmastery.com/how-to-load-data-in-python-with-scikit-http://machinelearningmastery.com/how-to-load-data-in-python-with-scikit-learn/learn/):

`# the Pima Indians diabetes dataset from CSV URLPython` `# Load the Pima Indians diabetes dataset from CSV URL` `import numpy as np` `import urllib` `# URL for the Pima Indians Diabetes dataset (UCI Machine Learning Repository)` `url = "http://goo.gl/j0Rvxq"` `# download the file` `raw_data = urllib.urlopen(url)` `# load the CSV file as a numpy matrix` `dataset = np.loadtxt(raw_data, delimiter=",")` `print(dataset.shape)` `# separate the data from the target attributes` `X = dataset[:,0:7]` `y = dataset[:,8]`

from sklearn import svm `clf = svm.SVC()` `clf.fit(X, y)`

`from sklearn.externals import joblib` `joblib.dump(clf, 'models/PID_svm.pkl')`

That's pretty much it. If you are interested, also check out some cool text classification examples at [here](http://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html).

Arthur
