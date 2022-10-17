# Melanoma Detection

## Table of Contents
* Problem Statement
* Data Loading
* Visualizing the data
* Model Building
* Conclusion

## General Information
1. Problem Statement

To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

  - Actinic keratosis
  - Basal cell carcinoma
  - Dermatofibroma
  - Melanoma
  - Nevus
  - Pigmented benign keratosis
  - Seborrheic keratosis
  - Squamous cell carcinoma
  - Vascular lesion

## Conclusions
- **Model 1 - Vanilla Model**
  - Training the model with basic CNN architecture, having 2 hidden layers and applying softmax as activation function.
  - Our model seems to be overfitting **Training accuracy = 91% and validation accuracy = 48%**.
  - Overfitting was due to lack of dropout layers and no data augmentation.

- **Model 2**
  - Model 2 was built on model 1 and adding drop out layers and augmentation.
  - By training Model 2, we got **Training accuracy = 60% and validation accuracy = 54%**.

- **Model 3**
  - Model 3 was built on model 2 and applied augmentor for balancing the class.
  -  Added 500 samples per class to make sure that none of the classes are sparse.
  - Applied Batch Normalization and l2 regularizer.
  - Training model 3 yielded **Training accuracy of 86% and validation accuracy of 83%**.


## Technologies Used
- Python
- Tensor Flow
