# Predictions for Alphabet Soup funding data | A binary classifier
### Goal
To create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.
### Data
A CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.
### Tools
Google Colab, TensorFlow and Keras, sklearn, pandas
### Steps

a. **Preprocessing the data**
   - Determined the targets and features:
      The following variable is the target for the model: was the money used successfully.
      The following variables are the features for the model: application type, affiliation, classification, use case, organization, status, income classification, special considerations for application, funding amount requested.
      The following variables should be removed from the input data because they are neither targets nor features: identification columns (EIN and NAME). 
   - Determined the number of data points for each unique value and picked a cutoff point to bin "rare" categorical variables together in a new value *Other*
   - Used pd.get_dummies() to encode categorical variables
   - Split the data into training and testing and scaled it

b. **Compiling, training, and evaluating the model**
   - Used TensorFlow and Keras to create a neural network model
   - Compiled and trained the model: 2 hidden layers, 80 neurons in the first one and 30 neurons in the second one, relu activation function for the hidden layers and sigmoid function for the output layer
   - Evaluated the loss and accuracy
     
c. **Optimizing the model to try and increase its accuracy** 
  - Optimization 1: added another hidden layer
  - Optimization 2: added neurons to the second hidden layer and replaced *relu* with *tahn* for the hidden layers
  - Optimization 3: reduced the number of neurons for the first hidden layer and switched back to *relu*

I wasn't able to achieve the target model performance of 75%.
