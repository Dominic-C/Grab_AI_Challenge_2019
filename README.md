# Grab AI for SEA challenge - Safety
The following jupyter notebooks were written in google colab. For ease of running, open the notebooks in google colab and set hardware acceleration to "GPU".

I use google cloud storage to transfer files between the code notebooks. However, you may wish to use alternative methods to transfer files such as pickles and models from one notebook to another.

**Important note:** change all filepaths used in these notebooks to suit your environment.

## Prerequisites
* tensorflow and keras
* pandas
* numpy

## Jupyter notebooks
### preprocess_function.ipynb
This notebook is to be run first. It takes in csv files and outputs pickle objects for sequential data and pickles. The notebook consists of the functions I used to preprocess the given csv data into useable data. The `preprocess_data_for_training` function in this notebook is also used to preprocess the testing data.

This notebook also outputs two pickle files into the `/content/` in google colab and exports them to my google cloud storage account. Change the export location and method to suit your environment.

### model_train_from_pickle.ipynb
Imports the pickles saved from `preprocess_function.ipynb`, splits it into training and test data, and trains an LSTM model with training data.

### import_and_test_model.ipynb
Imports the model and tests it. User has to use the `preprocess_data_for_training` function in `preprocess_function.ipynb` to preprocess the test data before testing it.


