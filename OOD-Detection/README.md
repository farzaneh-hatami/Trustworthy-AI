# Out of distribution detection
In this project we discuss about outliers, we set a threshold, if output of a softmax below that threshold, is considerd as outlier.

## Model
We use torchvision resnet18. For detect outliers, we train our model two times:
- Train a classifier without frog class
- Train a classifier without cat class

<br/>
We can see the training loss below:
  
## Result
A sample of result:

<br/>
<img src="imgs/frog.PNG" data-canonical-src="imgs/frog.PNG" width="500" />
<img src="imgs/cat.PNG" data-canonical-src="imgs/cat.PNG" width="500" />

