# Emotion-Classification-using-CNN
A simple Emotion Classification model to predict the emotions of people using images

## Dependencies Required:

. Pytorch
. Torchvision
. Pillow
. Scikit-Learn
. numpy
. matplotlib
. collections


### THE EMOTION CLASSIFICATION DATASET CONSISTS OF 7 CLASSES OF DIFFERENT HUMAN EMOTIONS.

### Methodology:

1. Classes were heavily imbalanced, hence to address that I have used image augmentation of the minority classes to augment the images with randomized   
   transformation.
   
2. Randomized transformation promotes diversity and variablity.

3. Further we combine both the augmentation data with original data.

4. I applied Weighted Random Sampler to assign weight importances to each class , as this is essential to handle imbalanced classes

5. The Combined data of training and validation is then loaded to the DataLoader along with sampler
   
6. Defined our CNN model for the task

## Our Model architecture consists of:

### . 4 Convolutional Layers
### . 2 Dense Layers
### . 4 Batch Normalization Layers        
### . Mish Activation Function        
### . Dropout 



7. Mish outperformed ReLU for the emotion dataset. I have experimented along with Swish, ReLU, LeakyReLU

8. Further to prevent overfitting I have used L2 regularization which is then passed to the Optimizer
   
9. Integrated various method to stablilize learning and to prevent overfitting.

### . Used ADAMW as optimizer with L2 Regularization
### . Incorporated Learning Rate Scheduler On Plateau
### . Implemented Early Stopping


10. Finally Test conclusions were performed on validation as well as final_test set which was completely unseen data

### . Implemented Confusion Matrix for the Classes
### . Plotted Precision-Recall Curve for each class

Note:
### I Used precision recall curve as it helps understand how each class performs, this is especially helpful when the classes are imbalanced


## Lastly, Thank you for reading this.


 
       
