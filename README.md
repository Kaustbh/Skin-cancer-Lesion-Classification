# Skin-cancer-Lesion-Classification

The primary goal of this work is to build up a Model of Skin Cancer Detection System utilizing Machine Learning Algorithms.

We can increase the validation accuracy by adding the BatchNormalization layer after each Dense, and MaxPooling2D layer .

## Skin Cancer MNIST:HAM10000 Dataset

Download the dataset from here : 

https://www.kaggle.com/kmader/skin-cancer-mnist-ham10000

This is  the HAM10000 ("Human Against Machine with 10000 training images") dataset.It consists of 10015 dermatoscopicimages which are released as a training set for academic machine learning purposes and are publiclyavailable through the ISIC archive. This benchmark dataset can be used for machine learning and for comparisons with human experts.

It has 7 different classes of skin cancer which are listed below :

" Melanocytic nevi "

" Melanoma "

" Benign keratosis-like lesions "

" Basal cell carcinoma "

" Actinic keratoses "

" Vascular lesions "

" Dermatofibroma "


## Libraries Used: 

• numpy

• keras

• tensorflow

• pandas

• matplotlib

• pillow

• seaborn

• cv2

• glob

• sklearn

• os

you  can install all the librarires using the  command " pip install 'library name'  " 

# Description 

## Skin_Cancer_Detection.ipynb:
This is the Jupyter notebook used to  preprocess , define and train the model.

## CNN Model Summary :

```
Model: "sequential_1"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_3 (Conv2D)           (None, 73, 98, 256)       7168      
                                                                 
 max_pooling2d_3 (MaxPooling  (None, 36, 49, 256)      0         
 2D)                                                             
                                                                 
 dropout_5 (Dropout)         (None, 36, 49, 256)       0         
                                                                 
 conv2d_4 (Conv2D)           (None, 34, 47, 128)       295040    
                                                                 
 max_pooling2d_4 (MaxPooling  (None, 17, 23, 128)      0         
 2D)                                                             
                                                                 
 dropout_6 (Dropout)         (None, 17, 23, 128)       0         
                                                                 
 conv2d_5 (Conv2D)           (None, 15, 21, 64)        73792     
                                                                 
 max_pooling2d_5 (MaxPooling  (None, 7, 10, 64)        0         
 2D)                                                             
                                                                 
 dropout_7 (Dropout)         (None, 7, 10, 64)         0         
                                                                 
 flatten_1 (Flatten)         (None, 4480)              0         
                                                                 
 dense_4 (Dense)             (None, 64)                286784    
                                                                 
 dropout_8 (Dropout)         (None, 64)                0         
                                                                 
 dense_5 (Dense)             (None, 128)               8320      
                                                                 
 dropout_9 (Dropout)         (None, 128)               0
 
 dense_6 (Dense)             (None, 7)                 903       
                                                                 
=================================================================
Total params: 672,007
Trainable params: 672,007
Non-trainable params: 0
_________________________________________________________________
```

## Accuracy :
![92ec7813-4997-4c3b-84e6-621102fc468f](https://user-images.githubusercontent.com/97254178/213926232-38f6d2b6-cdee-4b93-8754-15870ff9194a.png)

![4e1dfab3-2a20-4b81-baa9-5643e4f96edc](https://user-images.githubusercontent.com/97254178/213926253-f348abd7-d5a9-4b7b-ba57-850fc1ff9fb5.png)

## Confusion Matrix Heatmap :

![f68ed521-74a0-438a-89e9-3b05624d44e9](https://user-images.githubusercontent.com/97254178/213926293-1a2cd9e2-1010-481e-a333-3894d7719707.png)
