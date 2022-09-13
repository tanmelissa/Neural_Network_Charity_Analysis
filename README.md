# Neural_Network_Charity_Analysis

## Overview of Analysis

This analysis seeks to create a neural network to predict which organizations are going to use donations from Alphabet Soup, a charity organization, in an impactful way.

## Results

### Data Preprocessing

- This neural network is seeking to predict if the donation is successful. I this dataset, this (the target) is the column "IS_SUCCESSFUL".

- The features for this model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.

- The variables that needed to be removed from the input data are "EIN" and "NAME" as they are not targets nor features.

### Compiling, Training, and Evaluating the Model

- The final model had two hidden layers, both with 128 nodes. 

![image](https://user-images.githubusercontent.com/102273449/189786846-60f1aaea-d6a3-4f0a-a2df-bc59dfcb7052.png)

- The number of epochs was 17. The number of nodes was selected by using Keras Tuner to search for the best hyperparameter. The number of epochs was found by looking for the epoch with the best tested accuracy out of 100 epochs. The final moodel was then trained for that amount of epochs (17).

![image](https://user-images.githubusercontent.com/102273449/189787347-9b301fb2-b984-4874-92d9-2dad93d67e31.png)

- I was unable to achieve the target model performance of 75%, but was close at 72.3%

## Summary

- The final model had two hidden layers using relu, and an output layer using sigmoid. The two hidden layers had 128 nodes each.

- With a test accuracy of 72.3% and a test loss of 0.55, this model is a fair model for predicting which organizations are low risk to donate to.

- This model could be improved by looking into the most beneficial number of hidden layers (perhaps more would be better) or by looking at the dataset and removing any extreme outliers.
