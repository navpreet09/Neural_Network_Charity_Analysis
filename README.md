# Neural_Network_Charity_Analysis
# Overview
The purpose of this project is to use deep-learning neural networks with the TensorFlow platform in Python, to analyze and classify the success of charitable donations.
We use the following methods for the analysis:
- preprocessing the data for the neural network model,
- compile, train and evaluate the model,
- optimize the model.
# Results
### Data preprocessing:
- The column IS_SUCCESSFUL is considered to be target variable. it contains binary information whether a charity is successful or failed.
- The column which have been considered as features variable are following: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.
- Binning is applied on APPLICATION_TYPE and CLASSIFICATION columns and categorical columns are encoded for train, test and split the features.
- The column names EIN and NAME have been removed from the data.
### Compiling, Training, and Evaluating the Model
- For this deep-learning model two hidden layers have been used first one with 80 neurons and second with 30 neurons.
- The activation function used in hidden layers is relu for higher acuracy of the model. whereas otput layer has a single neuron with sigmoid activation function. For the compilation the loss function is binary_crossentropy and optimizer is adam with metrics accuracy.
- After evaluating the model the accuracy is 72 % which is lower than expected acuracy of over 75 percent.
- To increase the model performance additonal columns STATUS and SPECIAL_CONSIDERATIONS dropped from the features and a third layer is added to the model with 20 neurons and the activation function also changed to tanh.Despite all these changes the model performance stayed under 75 percent.
# Summary
The deep learning neural network model did not reach the target of 75% accuracy. Considering that this target level is pretty average we could say that the model is not outperforming.
Since we are in a binary classification situation, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.
