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

This section focuses on preparing the data for machine learning:

- Import necessary libraries listed in the dependencies section
- ReaD the dataset in 
- Drop uneccessary columns ('EIN' and 'NAME').
- Binning values in 'APPLICATION_TYPE' and 'CLASSIFICATION' that occur a small number of times.
- Convert categorical data to numeric data using the `pd.get_dummies` function.
- Spli the dataset into features (X) and target variable (y) arrays.
- Scale using StandardScaler to standardize dataset.
  
## Compile, Train, and Evaluate the Model

This section focuses on defining, compiling, training, and evaluating a deep neural network:

- Defines a sequential model with input and hidden layers that included neurons and activation functions.
- Compiles the model with binary crossentropy loss and a Adam optimizer.
- Trains the model with data that preprocessed in previous section.
- Evaluatesthe model's performance on the test dataset.
- Saves the trained model to an HDF5 file named 'model.h5'.

## Optimization

The original model (AlphabetSoupCharity.ipynb) was optimized to help improve performance. For the first attempt (AlphabetSoupCharityOptimization.ipynb), the number of nuerons in the second hidden layer was increased from 30 to 300 while the epochs were changed from 100 to 200. This did not change the performance at all. So, for the second attempt (AlphabetSoupCharityOptimization2.ipynb) the binning value for class count was lowered from <1000 to <700 and the number of neurons in the second hidden layer to was increased to 600. This had the highest performance with an accuracy of 0.731. The third and final attempt (AlphabetSoupCharityOptimization3.ipynb) added to the second optimization by creating a third hidden layer with 1000 neurons. This models' accuracy performed better than the original but was sligtly lower than my second optimization attempt. 


# Results 

- AlphabetSoupCharity: accuracy = 0.7279
- AlphabetSoupCharityOptimization: accuracy = 0.7248
- AlphabetSoupCharityOptimization2: accuracy = 0.7308
- AlphabetSoupCharityOptimization3: accuracy = 0.7306

The results of this model show that a deep learning model may not be the best approach for the purpose of Alphabet Soups desired goal. Deep learning is a reasonable approach to binary classification problems but can risk over or underfitting. An alternative that could be explored is a random forest model since it can capture complex relationships in data that is non-linear. 


## Acknowledgments

Thank you to my tutor Geronimo Perez for helping me create the code for my original model! 
