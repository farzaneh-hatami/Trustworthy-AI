# Explainability 

In this project, we use the LIME and SHAP methods for a better understanding of our model.For complex models, such as deep neural networks,
we cannot use the original model as its own best explanation because it is not easy to understand, so we use a simpler explanation model.

## SHAP

We use SHAP to explain our model. We use two different models of SHAP:
- Kernel SHAP
- Deep SHAP

### Dataset
We use [(LifeExpectancy)](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who) dataset in our project, and use the following preprocessing steps:  

- Delete NANs from the dataset or replace them with a value
- Encode categorical features
- Replace the categorical features with new values.
- Normalize the features

### Model

The model is a neural network with 5 linear layers with 112 input neurons and 1 output nueron. After each linear layer, an activation function (Relu) is used. the network train with MSE loss and an Adam optimizer.

### Resualts

A sample of resualts:

Summery plot for SHAP:

<img src="imgs/deep_SHAP.PNG" data-canonical-src="imgs/deep_SHAP.PNG" width="400" />


  
