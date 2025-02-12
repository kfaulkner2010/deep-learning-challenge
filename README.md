Neural Network Model for Charity Funding Prediction
Introduction
This report analyzes a neural network model designed to predict the likelihood of a charity organization receiving funding. We used TensorFlow’s Keras API to train and evaluate the model.

Data Preprocessing
Target Variables:

IS_SUCCESSFUL: This is the binary target variable, indicating whether a charity was successful in receiving funding (1 for success, 0 for failure).
Feature Variables:

All other columns except IS_SUCCESSFUL are considered features. These include:
APPLICATION_TYPE
AFFILIATION
CLASSIFICATION
INCOME_AMT
ASK_AMT
And other relevant columns.
Variables to Remove:

EIN and NAME were removed as they are unique identifiers for each charity and do not provide any meaningful predictive value for the model.
Compiling, Training, and Evaluating the Model
Neurons, Layers, and Activation Functions:

Neurons:
First hidden layer: 64 neurons.
Second hidden layer: 32 neurons.
Layers:
Two hidden layers were used to capture complex relationships in the data.
One output layer was used with a sigmoid activation function to predict binary outcomes (successful funding or not).
Activation Functions:
ReLU (Rectified Linear Unit) activation was used for both hidden layers to introduce non-linearity and prevent the vanishing gradient problem.
Sigmoid activation was used in the output layer to map the model's output between 0 and 1, making it suitable for binary classification.
Achieving Target Model Performance:

Training Accuracy: 74.04%
Validation Accuracy: 72.78%
The model performed reasonably well but didn’t quite reach an ideal performance. The validation accuracy is a little lower than the training accuracy, suggesting some overfitting.
Steps Taken to Improve Performance:

Regularization: No regularization methods, like dropout, were applied, but adding dropout layers could help prevent overfitting.
Hyperparameter Tuning: We experimented with the number of layers and neurons, but further tuning of the learning rate, batch size, or other hyperparameters could improve the model's performance.
Data Scaling: Feature scaling was performed using StandardScaler to ensure all input features were on the same scale, which aids in faster and more stable training.

Summary
The neural network model showed good results with a validation accuracy of 72.78%, which is a solid starting point. However, there is room for improvement, especially in reducing overfitting and fine-tuning the model further. By adding regularization techniques and experimenting with hyperparameters, we could potentially increase the model’s accuracy.
