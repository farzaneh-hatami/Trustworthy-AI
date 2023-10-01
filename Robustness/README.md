# Robustness
 In this project, we discuss about robustness and generalization.  

Generalization refers to model's ability to adapt properly to test data, drawn from the same distribution as the training 
data distribution. Robustness refers to the degree that a model's performance changes when using test data which are unseen versus training data.
We train the model with noisy data and without noisy data, and test the performance on them. 

## Dataset
We use CIFAR10 dataset for training and inference that has 10 classes.


## Architecture
The Resnet18 architecture is used for training the model. </br>


## Training
For the training part, we use corrupted and clean data, and different criteria like cross-entropy and angular loss are also tested.

We compare resualt with three different methods:
- Resnet18 training with CIFAR10 and cross-entropy criteria and testing on CIFAR10
- Resnet18 training with CIFAR10 and cross-entropy criteria and testing on corrupted CIFAR10
- Resnet18 training with corrupted CIFAR10 and cross-entropy criteria and testing on corrupted CIFAR10
- Resnet18 training with CIFAR10 and angular-loss and testing on CIFAR10
- Resnet18 training with CIFAR10 and angular-loss and testing on corrupted CIFAR10
- Resnet18 training with corrupted CIFAR10 and angular-loss and testing on corrupted CIFAR10


## Resualts

A sample of resualts:

 cross-entropy criteria:
 |                                                    |     test data     | validation data |
 |--------------------------------------------------  |-------------------|-----------------|
 |training with Clear data & testing on clear data    |      0.54         |       0.55      |
 |training with clear data & testing on coruptted data|      0.41         |       0.43      |
 |training and testing on corrupted data              |      0.54         |       0.55      |

 Angular criteria:
 |                                                    |     test data     | validation data |
 |--------------------------------------------------  |-------------------|-----------------|
 |training with Clear data & testing on clear data    |      0.59         |       0.59      |
 |training with clear data & testing on coruptted data|      0.45         |       0.47      |
 |training and testing on corrupted data              |      0.57         |       0.58      |

 ## Conclusion

 A trained model with a corrupted dataset helps the model be robust against those corruptions and also leads to better generalization.
Anglar loss is better than cross-entropy loss.

