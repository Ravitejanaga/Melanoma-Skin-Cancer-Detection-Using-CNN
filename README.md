# Melanoma Skin Cancer Detection
### Problem statement: 
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
### Objective: 
Build a multiclass classification model using a custom convolutional neural network in tensor flow.

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant. The data set contains the following diseases:
1.	Actinic keratosis
2.	Basal cell carcinoma
3.	Dermatofibroma
4.	Melanoma
5.	Nevus
6.	Pigmented benign keratosis
7.	Seborrheic keratosis
8.	Squamous cell carcinoma
9.	Vascular lesion

### Contents:
•	Data Reading/Data Understanding → Defining the path for train and test images
•	Dataset Creation→ Created train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
•	Dataset visualisation → Created a code to visualize one instance of all the nine classes present in the dataset.
•	Model Building & training: Created a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0, 1).
•	Chosen an appropriate optimiser and loss function for model training
•	Train the model with ~20 epochs
•	Written the findings after the model fit, seen if there is evidence of model over fit or under fit
•	Chosen an appropriate data augmentation strategy to resolve under fitting/over fitting Model Building & training on the augmented data.
Data Reading/Data Understanding:
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images.
The data set contains the following diseases:
 
CNN Architecture Design:
Model: "sequential_1"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 rescaling_1 (Rescaling)     (None, 180, 180, 3)       0         
                                                                 
 conv2d_3 (Conv2D)           (None, 178, 178, 32)      896       
                                                                 
 max_pooling2d_3 (MaxPooling 2D)(None, 89, 89, 32)       0         
                                                             
                                                                 
 conv2d_4 (Conv2D)           (None, 87, 87, 64)        18496     
                                                                 
 max_pooling2d_4 (MaxPooling 2D)(None, 43, 43, 64)       0         
                                                             
                                                                 
 conv2d_5 (Conv2D)           (None, 41, 41, 128)       73856     
                                                                 
 max_pooling2d_5 (MaxPooling 2D)(None, 20, 20, 128)      0         
                                                             
                                                                 
 dropout_2 (Dropout)         (None, 20, 20, 128)       0         
                                                                 
 flatten_1 (Flatten)         (None, 51200)             0         
                                                                 
 dense_2 (Dense)             (None, 128)               6553728   
                                                                 
 dropout_3 (Dropout)         (None, 128)               0         
                                                                 
 dense_3 (Dense)             (None, 9)                 1161      
                                                                 
=================================================================
Total params: 6,648,137
Trainable params: 6,648,137
Non-trainable params: 0
____________________________

## Technologies Used
Python
Google Colab

## Acknowledgements
Give credit here.
- This project was inspired by upGrad Learning Portal
- References if any...
- This project was based on https://learn.upgrad.com.


## Contact
Created by [@https://github.com/Ravitejanaga] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
