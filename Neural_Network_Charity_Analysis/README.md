# Neural_Network_Charity_Analysis
Preprocessing Data for a Neural Network model and optimizing it

## Overview of the analysis:
Using my knowledge from machine learning and neural networks for this project I use the features in this dataset I create a binary classifier that will tell the customer whether or not the applicants will be successful using alphabet soup. The dataset contains over 34,000 organizations that have been funded by alphabet soup. There are a number of columns that capture the metadata of each organization such as organization type, the use of funding amongst others. This project is comprised of 3 steps: Preprocessing the data for the neural network, Compile,train and evaluate the model & finally optimizing the model.

## Results:
* Data Preprocessing
    * Variable(s) that are considered as target(s) for the model
        * The variable we are targeting in this module is the IS_SUCCESSFUL column since we are checking if the applicants will be successful if funded by Alphabet Soup.

    * Variable(s) that are considered as the features for the model
        * The features that we are using are every column of the DataFrame application_df droping the column IS_SUCCESSFUL.

    * What variable(s) are neither targets nor features, and should be removed from the input data?
        * The EIN and NAME columns will not be having any role in increasing accuracy of the model and hence can be removed.

* Compiling, Training, and Evaluating the Model
    * How many neurons, layers, and activation functions did you select for your neural network model, and why?
        * I selected layer 1 - 100 neurons, layer 2 - 60 neurons, layer 3 - 30 neurons, layer 4 - 10 neurons.
        * First and second layer have relu as the activation while third, fourth and output layers have sigmoid as activation layer.
        * Selecting all the above increased the accuracy to 72.85 %
    
    ![Image3](https://github.com/Vaishali715/Neural_Network_Charity_Analysis/blob/main/Images/nn_3.png)

    * Were you able to achieve the target model performance?
        Although the target for the model to achieve was 75% or above, I was not able to reach the target.

    * What steps did you take to try and increase model performance?
        * Some of the steps I took to try and make the model more accurate were adding hidden layers, changing the activation type, changing the number of epochs and changing the number of neurons in each layer.
    Below are the screenshots for the accuracy from initial model from deliverable 1 & 2 and accuracy for the optimized model.

![Image1](https://github.com/Vaishali715/Neural_Network_Charity_Analysis/blob/main/Images/nn_1.png)

![Image2](https://github.com/Vaishali715/Neural_Network_Charity_Analysis/blob/main/Images/nn_2.png)


## Summary:
* The model's accuracy ended up being 72.75% - we started with a data set and tried to predict whether or not the project would be successful on all of the features that we used after dropping two features that we figured to be irrelevant. Although I did not get to the accuracy of 75% that I wanted, but it is possible that the reason for this is we may have had to drop more features which may have affected the results. The best way to increase the accuracy of this model is to have more data. If we have solid data added to this model, the accuracy of this model will be much more concrete.

* The random forest classifier can also be used for the same data as it has achieved a similar accuracy with less time than the neural network model. If we compare both model's predictive accuracy, their output is very similar. Both the random forest and deep learning models were able to predict correctly if applicants will be successful if funded by Alphabet Soup. Although their predictive performance was comparable, their implementation and training times were not. The random forest classifier was able to train on the large dataset and predict values in seconds, while the deep learning model required a couple minutes to train on the tens of thousands of data points. In other words, the random forest model is able to achieve comparable predictive accuracy on large tabular data with less code and faster performance.

![Image4](https://github.com/Vaishali715/Neural_Network_Charity_Analysis/blob/main/Images/nn_rf.png)
