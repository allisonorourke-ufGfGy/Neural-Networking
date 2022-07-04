# Neural-Networking
## Overview of the analysis
Beks has come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively


## Results
### Data Preprocessing
* What variable(s) are considered the target(s) for your model? For this analysis and model, the target is held in IS_SUCCESSFUL field.
* What variable(s) are considered to be the features for your model?
ORGANIZATION,  
STATUS, 
INCOME_AMT, 
SPECIAL_CONSIDERATIONS, 
ASK_AMT, 
APPLICATION_TYPE, 
AFFILIATION, 
CLASSIFICATION, 
USE_CASE
* What variable(s) are neither targets nor features, and should be removed from the input data? NAME and EIN
### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why? This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively.
The input data has 43 features and 25,724 samples.
The output layer is made of a unique neuron as it is a binary classification.
To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
* Were you able to achieve the target model performance? No, the model accuracy was under 75% so it didn not satisfy the performance. It only reached about 51%.
* What steps did you take to try and increase model performance?
Increasing the number of hidden nodes in layer 1 (3 X number of input features). 
Increasing the number of hidden layers to include a 3rd. 
Changing the activation functions: tried linear, tanh, sigmoid for a combination of hidden layers and output layer.
## Summary
We were not able to build a model that reached the target of 75% accuracy so we would likely not be able to say this model is outperforming. I would not reccomend this model for other instiances and instead may reccomend one of the supervised machiene learning models. Since we are in a binary classification situation, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.
