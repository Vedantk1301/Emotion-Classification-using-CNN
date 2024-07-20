# Emotion-Classification-using-CNN
A simple Emotion Classification model to predict the emotions of people using images

## Dependencies Required:

* PyTorch
* Torchvision
* Pillow
* Scikit-Learn
* NumPy
* Matplotlib
* Collections
  

### THE EMOTION CLASSIFICATION DATASET CONSISTS OF 7 CLASSES OF DIFFERENT HUMAN EMOTIONS.

__Methodology__:

1. Classes were heavily imbalanced, hence to address that I have used image augmentation of the minority classes to augment the images with randomized   
   transformation.
   
2. Randomized transformation promotes diversity and variablity.

3. Further we combine both the augmentation data with original data.

4. I applied Weighted Random Sampler to assign weight importances to each class , as this is essential to handle imbalanced classes

5. The Combined data of training and validation is then loaded to the DataLoader along with sampler
   
6. Defined our CNN model for the task


   __Our Model architecture consists of:__
      
     
     ___* 4 Convolutional Layers___
     ___* 2 Dense Layers___
     ___* 4 Batch Normalization Layers___
     ___* Mish Activation Function___
     ___* Dropout___



8. Mish outperformed ReLU for the emotion dataset. I have experimented along with Swish, ReLU, LeakyReLU

9. Further to prevent overfitting I have used L2 regularization which is then passed to the Optimizer
   
10. Integrated various method to stablilize learning and to prevent overfitting.
    

    ___* Used ADAMW as optimizer with L2 Regularization___
    ___* Incorporated Learning Rate Scheduler On Plateau___
    ___* Implemented Early Stopping___


11. Finally Test conclusions were performed on validation as well as final_test set which was completely unseen data
    

    ____* Implemented Confusion Matrix for the Classes___
    ____* Plotted Precision-Recall Curve for each class___


___Note:___

___I Used precision recall curve as it helps understand how each class performs, this is especially helpful when the classes are imbalanced___


___Lastly, Thank you for reading this.___


 
       
