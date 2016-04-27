NegaJoules Project - The Machine Learning part
-----------------------------
This document describes the methodology for importing data from a SQL database to Python environment, to conduct analysis, deliver Machine Learning predictive models and perform optimization on that model to improve the energy consumption of the systems under study.

%Further documentation on the method can be found in this [blog %post](http://simaaron.github.io/Estimating-rainfall-from-weather-radar-readings-using-recurrent-neural-networks/).

## Generating the solution  

### Install the dependencies
The models are written in Python 2.7 and makes use of the NumPy, scikit-learn, and pandas packages. These can be installed individually via `pip` or all together in a free Python distribution such as [Anaconda](https://www.continuum.io/downloads).

Theano can be installed and configured to use any available NVIDIA GPUs by following the instructions [here](http://deeplearning.net/software/theano/install.html) and [here](http://deeplearning.net/software/theano/tutorial/using_gpu.html). The Lasagne package often requires the latest version of Theano; a simple `pip install Theano` may give a version that is out-of-date (see Lasagne documentation for details).  

Lasagne can be installed by following the instructions [here](http://lasagne.readthedocs.org/en/latest/user/installation.html).


### Download the code
To download the code run:

```
git clone git://github.com/simaaron/kaggle-Rain.git
```
Create an empty data folder

```
cd kaggle-Rain
mkdir data
```


### Download the training and test data
The training and test data can be downloaded from the Kaggle competition webpage at this [link](https://www.kaggle.com/c/how-much-did-it-rain-ii/data). The two extracted files `train.csv` and `test.csv` should be placed in the `data` folder. 

Note: the benchmark sample solution and code provided by Kaggle are not required.

### Preprocess the data
