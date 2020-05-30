# plant-pathology-competition
Kaggle competition to identify diseases in apple trees using computer vision.

## Introduction
Misdiagnosis of the many diseases impacting agricultural crops can lead to misuse of chemicals leading to the emergence of resistant pathogen strains, increased input costs, and more outbreaks with significant economic loss and environmental impacts. Current disease diagnosis based on human scouting is time-consuming and expensive, and although computer-vision based models have the promise to increase efficiency, the great variance in symptoms due to age of infected tissues, genetic variations, and light conditions within trees decreases the accuracy of detection.

## Specific Objectives
Objectives of ‘Plant Pathology Challenge’ are to train a model using images of training dataset to 1) Accurately classify a given image from testing dataset into different diseased category or a healthy leaf; 2) Accurately distinguish between many diseases, sometimes more than one on a single leaf; 3) Deal with rare classes and novel symptoms; 4) Address depth perception—angle, light, shade, physiological age of the leaf; and 5) Incorporate expert knowledge in identification, annotation, quantification, and guiding computer vision to search for relevant features during learning.

## Model
In this competition I tried to avoid using any transfer learning. I created from scratch a ResNet50 in the notebook and trained on the images from scratch. There were promising results despite this method, when using a 4 fold cross validation, and the predictions achieved a top 16% in the competition. A DenseNet algorithm was also coded from scratch, however I was unable to employ an ensemble of the two models due to computation cost. 

In future I'm keen to compare the results of a ResNet50 model using transfer learning and a ResNet50 model coded from scratch on the same dataset.

## Requirements
 - pandas >= 1.0.4
 - numpy >= 1.18.4
 - tqdm >= 4.46.0
 - matplotlib >= 3.2.1
 - opencv-python >= 4.2.0.34
 - imgaug >= 0.4.0
 - sklearn >= 0.23.1
 - tensorflow >= 2.2.0
 - keras >= 2.3.1
