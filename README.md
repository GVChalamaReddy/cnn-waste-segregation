# Waste Material Segregation
**Problem Statement:** This project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

**Data Set:** https://drive.google.com/drive/folders/1sajIcvGxBemqK_YIHFoY28EyV1Su_b5M

## Table of Contents
* [General Info](#general-information)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
  ### Business Objective: 
    The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.
    The key goals are:
    - Accurately classify waste materials into categories like cardboard, glass, paper, and plastic.
    - Improve waste segregation efficiency to support recycling and reduce landfill waste.
    - Understand the properties of different waste materials to optimise sorting methods for sustainability.

  ### Approach:
  - All the images were the size of 256×256. Resize of images is done without loosing the data, inorder to reduce the compute memory issue .
  - All the images have 3 channels as RGB.
  - The data has seven categories. Cardboard, Food Waste, Glass, Metal, Other, Paper, Plastic
  - Class distribution was imbalanced. There was a greater number of images in the plastic category.
  - Since there was no equal number of images present in each category, the test and train split was done with stratify=y with an 80/20 ratio.

 ### Techniques:
 Specific tools or methods used at different steps of model building are mentioned below: 
 -	**Data preprocessing**: One-Hot encoding
 -	**Model building**: CNN Network, RESNET50
 -	**Model Optimization**: Dropout, Regularization, Learning Rate, Batch Normalization, Adam Optimizer
 -	**Evaluation metrics**: Accuracy, Confusion Matrix, Recall, Precision, F1-score

## Conclusions
- Started building own CNN model with 3 convolutional layers, but the accuracy was just 0.40, which was very low. I tried configuring hyperparameters like dropouts, and the performance increased to 0.50.
- As own CNN model is overfitting, used RESNET 50 with transfer learning approach.Initially made all the layers trainable as false observed only 0.60 training accuracy, a slight increase from own CNN model.
- Modified the trainable layers to 20 and got the training accuracy as 98 percent and the validation accuracy as 60%. Clearly the model was overfitting.
- To resolve overfitting problem, modified the trainable layers from 20 to 10, and still able to see the model is overfitting.
- Modified model training layer to 5 and increased the dropout from 0.6 to 0.7 and reduced the learning rate. with these configuration training accuracy: 0.86 and val_accuracy: 0.80 are improved signficantly.
- Clearly, the model is able to generalize the training data and produce the desired output.
- From the confusion matrix we are able to see a lot of misclassification is done as a plastic when compared to others, which is very little.
- Overall, the model was able to generalize the data and produce the acceptable prediction; nearly 86% of the data is properly classified.
- The model has performed well on the waste segregation task, achieving overall 84% accuracy with strong generalization.


## Technologies Used
- **python** - 3.13.1
- **numpy** - 2.2.1
- **pandas** - 2.2.3
- **matplotlib** - 3.10.0
- **seaborn** - 0.13.2
- **statsmodels** - 0.14.4
- **sklearn** - 1.6.1
- **keras** - 3.8.0
- **PIL** - 11.1.0
- **tensorflow** - 2.18.0

## Acknowledgements

- This project was inspired by Upgrad IIIT Bangalore PG program on ML and AI.
- This project was based on Convolutional Neural Networks (CNNs)


## Contact
Created by @[GVChalamaReddy](https://github.com/GVChalamaReddy) - feel free to contact me!
