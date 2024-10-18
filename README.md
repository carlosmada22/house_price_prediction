# house_price_prediction
Neural Network for predicting house prices (training, testing and prediction)

## Predicting House Prices
### Problem:
- **Objective**: Predict house prices. 
- **How**: Building a Feedforward Neural Network.
- **Dataset**: Various features about houses (e.g., square footage, number of bedrooms, furnished status).
- **Target variable**: House price

### Steps:
**Load the Dataset**: Housing dataset coming from Kaggle ([Link Here](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset))

**Preprocess the Data**:
  1) Convert categorical columns into numerical representations
  2) Separate features and target (price)
  3) Split data into training and testing sets
  4) Scale input features
  5) Scale target (price)
  6) Convert features and labels to tensors

**Build the Neural Network**: Feedforward Neural Network with the following layers:

*Input Layer*: Match the number of input features.

*Hidden Layers*: Two hidden layers with ReLU activation (512 and 256 units).

*Dropout Layers*: After each of the first two layers, dropout is applied with a probability of 0.3 to prevent overfitting.

*Output Layer*: One neuron for the continuous output (price).

**Train the Model**: 
 1) Use the MSE loss function and Adam optimizer. 
 2) Train for 400 epochs.
 3) Calculate and print the validation loss during training.

**Evaluate the Model**:  
 1) Calculate test loss after training.
 2) Plot training VS validation loss curves
 3) Calculate R-squared
