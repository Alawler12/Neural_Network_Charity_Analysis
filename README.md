# Neural Network Charity Analysis

### Analysis Overview
The purpose of this analysis was to create a machine learning model that could help predict whether applicants to charity funding would be successful in receiving funding based on a dataset of 34,000 past applications.  The data was preprocessed to work with a neural network model, trained, fit, and evaluated for accuracy.  I then attempted to optimize the model for better performance based on that evaluation.

### Results
* Data Processing
  - The target for this model was the variable “Is Successful,” which is indicates if an application was approved or not.
  - The features for this model were “Status”, “Ask Amt”, “Application Type”, “Income Amt”, “Affiliation”, “Classification”, “Use Case”, “Organization”, and “Special Considerations”
  - The variables that were neither features nor the target were “Name” and “EIN”.  These variables were removed from the input values.

The data was then encoded and scaled as necessary.

* Compiling, Training, and Evaluating the Model
  - My final model had three layers, with 110, 46, and 10 neurons respectively.  I chose 110 because that number is 2 to 3 time the number of input variables.  Honestly, the other two numbers were random and based on the numbers used in the challenge instructions.  I used a Relu activation function in the first hidden layer and Sigmoid functions in the other hidden layers and the output layer.  I chose these because based on my limited experience, they seemed to have been used the most often in other examples.  The Relu function can handle classification and regression, while the Sigmoid is better for binary classification.
  - I was not able to achieve a model performance over 75%
  - I took the following steps to optimize the model with the results listed below:
![attempts.PNG]( https://github.com/Alawler12/Neural_Network_Charity_Analysis/blob/main/images/attempts.PNG)

The model consistently showed a different accuracy during training and during testing.  It often came very close to the goal or exceeded it in training, and then dropped with evaluated with the different values in the testing data.  Frustrating. 
![training_accuacy.PNG)]( https://github.com/Alawler12/Neural_Network_Charity_Analysis/blob/main/images/training_accuacy.PNG)
![test_accuracy.PNG]( https://github.com/Alawler12/Neural_Network_Charity_Analysis/blob/main/images/test_accuracy.PNG)

### Summary
After 12 attempts to optimize the model, I was not able to gain a greater accuracy than about 73%.  Some different attempts I might have made could be to train the model with a greater number of epochs or to make more significant changes to the number of neurons between attempts.  I also think this dataset is kind of small for a deep learning neural network, and could be better served by a different machine learning algorithm like a random forest model.
