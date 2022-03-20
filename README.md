# Neural_Network_Charity_Analysis

## Overview
Utilize neural net machine learning model to predict which charity applications will be approved.

## Results

### Data Preprocessing
- The target of the model is the "IS_SUCCESSFUL" column of the application_df dataframe. 
- The features of the model are all remaining columns of the application_df dataframe, excluding the ones with dtype "object".

![data_frame](Images/data_frame.png)

### Compiling, Training, and Evaluating the Model
- In my optimization file, I used three hidden layers for my model. Layer one had 80 neurons, layer two had 40, and layer three had 20. Each layer used the "relu" activation function, with the exception being the output layer using sigmoid. I used 80 neurons in the first layer because it was approximately double the number of features inputted (44), with each following layer having half the neurons of the previous layer. I used the "relu" activation function because there were no negative values in the data that could have influenced the model, so everything was effectively scaled between 0 and 1. The sigmoid function also scaled the data appropriately in the output layer.
- I was unable to achieve the target model performance.
- To increase model performance, I tried adding a third hidden layer, changing the application type encoding to be < 100 rather than 500, and altering the number of epochs. Changing the epochs seemed to have minimal effect on the model, so I chose to stay at 50. I wanted to include more application data in the training so the model wouldn't disregard potentially useful applications in its assessment. 

## Summary
The model was 72.47% accurate from the initial parameters, and my optimization attempt was marginally better at 72.55%. I would recommend a supervised logistic regression model for better accuracy because it would run faster, not be prone to overfitting, and require much less tweaking.

![model_1](Images/model_1.png)

![model_2](Images/model_2.png)