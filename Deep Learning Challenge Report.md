Deep Learning Challenge Report 

1. Overview 
    The purpose of this analysis was to better understand neural networks and deep learning using Google Colab. The goal was to run and optimize a model for Alphabet Soup in order to help with the selection of applicants in need of funding. The model creates a binary classification that predicts if the applicants will be sucessful if granted funds. 

2. Results 
    - Data Processing

        - What variable(s) are the target(s) for the model?
            - The target variable for this model is the column 'IS SUCCESSFUL' which represents if a charity was successful (1) or not (0). So the model is trained to predict this based on the features. 

        - What variables(s) are the features for the model?
            - The features in this model are all of the columns except for the target variable and unecessary columns that were droped. All of the features are assigned to X. 

        - What variable(s) shoudld be removed from the input data because they are neight targets nor features?
            - The 'EIN' and 'NAME' columns were removed as they are not relevant in predicting the target variable. 

    - Compiling, Training, and Evaluating the model
        - How many neurons, layers, and activation functions did you select for your neural network model, and why?
            - In the original model I did two hidden layers and an output layer. The first hidden layers had 80 neurons and a 'relu' activation function since it is a standard setup. The second hidden layer contained 30 neurons and also had a 'relu' acitivation function. The output layer was a single neuron with a 'sigmoid' activation function. 

        - Were you able to achieve the target model performance?
            - During the optimization process I was unable to achieve target model performance. I was able to slightly raise the performance to 0.731 from 0728.

        - What steps did you take in your attempts to increase model performance?
            - In my first attempt, I increased the number of nuerons in the second hidden layer from 30 to 300 and increased the epochs from 100 to 200. This did not change the performance at all. So, for the second attempt I changed my binning value for class count from <1000 to <700 and increased the neurons in the second hidden layer to 600. This gave me the highest performance stated in the answer above. For my final attempt I added onto my second optimization by creating a third hidden layer with 1000 neurons. This model performed better than the original but was sligtly lower than my second optimization attempt. 

3. Summary 
    - The results of this model show that a deep learning model may not be the best approach for the purpose of Alphabet Soups desired goal. Deep learning is a reasonable approach to binary classification problems but can risk over or underfitting. An alternative that could be explored is a random forest model since it can capture complex relationships in data that are non-linear. 