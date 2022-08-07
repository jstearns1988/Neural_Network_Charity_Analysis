# Neural_Network_Charity_Analysis

## Overview of the analysis
Using machine learning and neural networks, I completed an anlysis on over 34,000 organizations that have received funding from Alphabet Soup. The data was preprocessed for a Neural Network Model. Then it the model was compiled, trained, and evaluated. I then made three attempts to optimize the model to achieve a target predicative accuracy higher than 75%.

## Results

### Preprocessing the Data

  - I removed the identification information columns EIN and NAME from the input data. 
  - I determined the number of unique values in each column to confirm IS_SUCCESSFUL contains binary data advising if the donation was used successfully. This colun is the target for the deep learning neural network.
  - Visualization was used via a density plot to create a cutoff point to bin "rare" categorical variables together in a new column, Other, and then I checked to make sure the binning was successful.
  - A list of categorical variables was generated, encoded using on-hot encoding, and placed in a new DataFrame.
  - The one-hot encoded DataFrame and the original DataFrame were merged and originals were dropped.
  
  ![Preprocess](https://github.com/jstearns1988/Neural_Network_Charity_Analysis/blob/main/Resources/Preprocess%20DF.png?raw=true)
  
### Compiling, Training, and Evaluating the Model
  - A deep-learaning neural network model was made of two hidden layers: one containing 80 neurons and one containing 30 neurons.
  - The next step was to check the structure of the model
  
  ![Structure Model](https://github.com/jstearns1988/Neural_Network_Charity_Analysis/blob/main/Resources/Structure%20Model.png?raw=true)
  
  - Next, a callback that saves the model's weights every 5 epochs was added.
  - The model was evaluated using the test data to determine the loss and accuracy.
  - The model accuracy is below 75%. This accuracy is not satisfactory in predicting the outcome of the charity donations.
  
  ![Model Eval](https://github.com/jstearns1988/Neural_Network_Charity_Analysis/blob/main/Resources/Model%20of%20Eval.png?raw=true)
  
### Optimizing the Model

  - Using TensorFlow, I attempted to optimize the model in order to achieve a target predictive accuracy higher than 75%.
  - I first attempted to increase the performance of the model by applying bucketing to the feature ASK_AMT and organized the differing values by intervals
  - The number of neurons was increased on one of the hidden layers
  - A model with three hidden layers was used
  - I also attempted to improve performance by using the tanh function
  - Unfortunately, all three attempts resulted in less than 75% performance
  
  #### Attempt 1 Results
  
  ![Attempt 1](https://github.com/jstearns1988/Neural_Network_Charity_Analysis/blob/main/Resources/Attempt%201.png?raw=true)
  
  #### Attempt 2 Results
  
  ![Attempt 2](https://github.com/jstearns1988/Neural_Network_Charity_Analysis/blob/main/Resources/Attempt%202.png?raw=true)
  
  #### Attempt 3 Results
  
  ![Attempt 3](https://github.com/jstearns1988/Neural_Network_Charity_Analysis/blob/main/Resources/Attempt%203.png?raw=true)
  
## Summary

The goal of a target 75% accuracy was not met. I would suggest trying this model with a Random Forest Classifier to combine decision trees to generate clssified output and evaluate its performance against the deep learning model performed in this analysis.
  
