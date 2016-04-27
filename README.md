NegaJoules Project - The Machine Learning part
-----------------------------
This document describes the methodology for importing data from a SQL database to Python environment, to conduct analysis, deliver Machine Learning predictive models and perform optimization on that model to improve the energy consumption of the systems under study.

Further documentation on the method can be found in this [blogpost](http://simaaron.github.io/Estimating-rainfall-from-weather-radar-readings-using-recurrent-neural-networks/).

## Get it started

### Download the code
To download the code run:
```
git clone git://github.com/diogoncalves/NJOULES.git
```

### Download the training and test data
The training and test data can be downloaded from the Kaggle competition webpage at this [link](https://www.kaggle.com/c/how-much-did-it-rain-ii/data). The two extracted files `train.csv` and `test.csv` should be placed in the `data` folder. 

Note: the benchmark sample solution and code provided by Kaggle are not required.

## Get things done

### Download and preprocess the data

Download relevant data from the MySQL database to your environment, from a specified time window. Divide the database in small datasets, deal with the `NaN` entries, remove the outliers (training data only) by running:

```
python data_preprocessing.py
```
This will also create three additional `train`, `valid`, and `test` folders. 

The size of the validation subset, the time window, the relevant variables, the outlier thresholds value can be changed in the above Python script.
