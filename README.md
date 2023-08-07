![image](https://github.com/aziegert/classification_alien_vs_predator/assets/123495041/daea6da7-51b6-4977-9d96-1184a0ebf7e4)

# Deep Learning Model for Alien vs. Predator Image Classification

This repository contains a deep learning model for classifying images of aliens and predators. The model utilizes the ResNet101 architecture and is trained using PyTorch. The code includes data loading, preprocessing, model creation, training, and evaluation steps. It also explores the impact of different image transformations on model performance.

## Dataset
The dataset employed for this project can be found on Kaggle: [Alien vs. Predator Images Dataset](https://www.kaggle.com/datasets/pmigdal/alien-vs-predator-images)

## Transformations
Before selecting the model, an analysis of various image transformations was performed to optimize the predictive capabilities of our model. By systematically evaluating a number of transformations, including changes in color, orientation, and other visual properties, three transformations were identified that yielded the highest validation accuracy.
![image](https://github.com/aziegert/classification_alien_vs_predator/assets/123495041/5c0dfeab-7311-43be-b2d1-6eb3231f9d94)

## Models
Several models were constructed based on the three transformations that gave the best results: RandomInvert(), RandomAutocontrast() and RandomEqualize(). In addition, the use of transformations available in the PyTorch library: TrivialAugmentWide() and AutoAugmentPolicy.IMAGENET was tested. These models were trained and evaluated.
![image](https://github.com/aziegert/classification_alien_vs_predator/assets/123495041/1862a085-cbf9-42d3-b62c-2a9470bcd5b8)

![image](https://github.com/aziegert/classification_alien_vs_predator/assets/123495041/3c7beced-2874-4326-8622-8c684d1d22fa)

The best trained model: 'few_transformation' is loaded for further evaluation. Model performance is evaluated on a test dataset. Accuracy and loss for the test data set:
Accuracy for test dataset: 0.9400
Loss for test dataset: 0.1772

## Sample Predictions
To showcase the model's predictions, a set of sample images is randomly selected from the test dataset. The model's predicted class (alien or predator) and the corresponding prediction probabilities for both classes are displayed alongside each image.
![image](https://github.com/aziegert/classification_alien_vs_predator/assets/123495041/302ebc0f-12e0-4e58-8e32-cbdbe8888dba)
