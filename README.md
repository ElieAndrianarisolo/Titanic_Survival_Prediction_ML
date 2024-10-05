# Titanic Survival Prediction Using Machine Learning

## Overview
This project demonstrates the use of machine learning to predict the survival of passengers on the Titanic based on various features such as sex, age, and fare. The model is built using a neural network with TensorFlow and Keras, and the dataset is sourced from TensorFlow Datasets (TFDS). The goal is to create a binary classification model that predicts whether a passenger survived or not, using features such as sex, age, and fare.

## Project Structure
- **Dataset**: The Titanic dataset is loaded from TensorFlow Datasets (`tfds`). It contains features such as sex, age, fare, and the survival outcome of the passengers.
- **Preprocessing**: 
  - Categorical features (like 'sex') are one-hot encoded.
  - Missing values in the 'age' feature are filled with the median age.
  - Numerical features (like 'age' and 'fare') are scaled using standardization.
- **Model**: A neural network classifier with:
  - An input layer with 16 neurons using the ReLU activation function.
  - A dropout layer for regularization (with 20% dropout).
  - A hidden layer with 8 neurons using ReLU activation.
  - An output layer with a sigmoid activation function, used for binary classification.
- **Training**: 
  - The model is compiled using the Adam optimizer and binary cross-entropy loss.
  - Accuracy is used as the evaluation metric.
  - The model is trained for 20 epochs with an 80/20 validation split.
- **Evaluation**: 
  - The model is evaluated on a test dataset, and accuracy is printed to show the performance.
- **Prediction**: 
  - The trained model makes predictions on the test set, and the predicted outcomes are compared with the actual labels.
- **Analysis**:
  - Survival rates are analyzed based on gender (`Sex`) and age (`Age`) groups using the predictions and actual results.

## Output
1. **Model Accuracy**: After training, the model's accuracy on the test dataset is printed.
2. **Prediction Results**: The model's predictions for survival are compared with actual outcomes, and a summary is provided.
3. **Survival Analysis**: 
   - A summary of survival rates based on gender (`Sex`) is printed.
   - A summary of survival rates based on age (`Age`) is printed.

## Conclusion
This project successfully implements a machine learning pipeline to predict the survival of Titanic passengers. It demonstrates essential steps in data preprocessing, neural network design, model training, and post-model evaluation.
