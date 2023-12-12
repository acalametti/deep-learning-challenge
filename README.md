# Deep Learning Challenge

## Contributors: Alex Calametti

# Overview: 

The purpose of this analysis was to better understand neural networks and deep learning using Google Colab. The goal was to run and optimize a model for Alphabet Soup in order to help with the selection of applicants in need of funding. The model creates a binary classification that predicts if the applicants will be sucessful if granted funds based on the results from previous organizations. 

## Programs and Files 

- Google Colab
- Charity Dataset: [charity_data.csv](https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv)
  
## Dependencies

- TensorFlow
- scikit-learn
- pandas


## Preprocessing

The preprocessing section focuses on preparing the dataset for machine learning. It includes:

- Importing necessary libraries such as TensorFlow, pandas, and scikit-learn.
- Reading the dataset
- Dropping non-beneficial ID columns ('EIN' and 'NAME').
- Binning low-frequency values in 'APPLICATION_TYPE'.
- Binning low-frequency values in 'CLASSIFICATION'.
- Converting categorical data to numeric using `pd.get_dummies`.
- Splitting the dataset into features (X) and target (y) arrays.
- Scaling the data using StandardScaler.
  
## Compile, Train, and Evaluate the Model

This section involves defining, compiling, training, and evaluating a deep neural network using TensorFlow:

- Defining a sequential model with input and hidden layers.
- Compiling the model with binary crossentropy loss and Adam optimizer.
- Training the model with preprocessed data.
- Evaluating the model's performance on the test dataset.
- Saving the trained model to an HDF5 file named 'model.h5'.

# Results 



## Acknowledgments

Thank you to my tutor Geronimo Perez for helping me create the code for my original model! 
