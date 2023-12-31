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

A sample of resualts for SHAPE:

Summery plot for deep SHAP:

<img src="imgs/deep_SHAP.png" data-canonical-src="imgs/deep_SHAP.png" width="400" />

Force plot for deep SHAP:
  
<img src="imgs/deep_sample1.PNG" data-canonical-src="imgs/deep_sample1.PNG" width="400" />
<img src="imgs/deep_sample2.PNG" data-canonical-src="imgs/deep_sample2.PNG" width="400" />

Summery plot for kernel-SHAP:

<img src="imgs/kernel.png" data-canonical-src="imgs/kernel.png" width="400" />

Force plot for kernel-SHAP:
  
<img src="imgs/kernel_sample1.PNG" data-canonical-src="imgs/kernel_sample1.PNG" width="400" />
<img src="imgs/kernel_sample2.PNG" data-canonical-src="imgs/kernel_sample2.PNG" width="400" />

## LIME

In this project, we want to explain our model with LIME.

### Model & Dataset

We use MobileNet-V2, which is trained on ImageNet. Fially For some selected classes, we show boundaries, pros and cons, and plot the heatmap for them.

### Resualt

A sampel of results on Goldfish class:
<br/>
<img src="imgs/goldfish_boundry.png" data-canonical-src="imgs/goldfish_boundry.png" width="400" />
<img src="imgs/pros_goldfish.png" data-canonical-src="imgs/pros_goldfish.png" width="400" />
<img src="imgs/headmap_goldfish.png" data-canonical-src="imgs/headmap_goldfish.png" width="400" />
