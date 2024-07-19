# Emotion-Classification-using-CNN
A simple Emotion Classification model to predict the emotions of people using images

Dependency Required:
Pytorch
Torchvision
Pillow
Scikit-Learn
numpy
matplotlib
collections


THE EMOTION CLASSIFICATION DATASET CONSISTS OF 7 CLASSES OF DIFFERENT HUMAN EMOTIONS.

Classes were heavily imbalanced, hence to address that I have used image augmentation of the minority classes to augment the images with randomized transformation.
Randomized transformation promotes diversity and variablity.

Further we combine both the augmentation data with original data.

I applied Weighted Random Sampler to assign weight importances to each class , as this is essential to handle imbalanced classes

The Combined data of training and validation is then loaded to the DataLoader along with sampler

## Our Model architecture consists of:

### 4 Convolutional Layers
### 2 Dense Layers
### 4 Batch Normalization Layers        
### Mish Activation Function        
### Dropout 



Mish outperformed ReLU in the dataset. I have experimented along with Swish, ReLU, LeakyReLU

Further to prevent overfitting I have used L2 regularization which are then passed to the Optimizer

### Used ADAMW as optimizer with L2 Regularization
### Incorporated Learning Rate Scheduler On Plateau
### Implemented Early Stopping


Finally Test conclusions were performed on validation as well as final_test set which was completely unseen data

### Implemented Confusion Matrix for the Classes
### Plotted Precision-Recall Curve for each class


### Used precision recall curve as it helps understand how each class performs

## Thank you for reading this.


 
       
