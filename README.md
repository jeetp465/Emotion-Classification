# Emotion-Classification
This repository is to experiment on Transfer Learning of different state of the art models and understand their efficiency in learning Human Emotions

## Dataset
The dataset used for carrying out experiments is WEBEmo, based on the paper [Contemplating Visual Emotions: Understanding and Overcoming Dataset Bias](https://rpand002.github.io/Papers/ECCV_2018.pdf)
More information about the dataset can be obtained [here](https://rpand002.github.io/emotion.html)

## Experiments
* CNN.ipynb is a basic VGG-like network to verify the effectiveness of learning emotion features directly from scratch.
* Resnet34.ipynb pertains to use transfer learning to classify the image into 1 of 25 categories.
* Resnet34 Level1.ipynb pertains to the first step of Curriculum guided Learning. It classifies the image into first hierarchichal level i.e positive or negative.
* Resnet50 Level2.ipynb pertains to the second step of Curriculum guided Learning. It is one of the experiments to classify images into second hierarchical level i.e six emotion categories based on the features learned from first level.

## Results & Observations
* CNN model and normal Resnet34 were unable to extract meaningful features to classify the images into 25 emotion categories.
* Resnet34 Level1 managed to classify the images into positive or negative with *65.52%* accuracy on the test set after 10 epochs. This can further be improved by optimizing the learning rate.
* Resnet50 Level2 classifies the images into positive and negative with *70.37%* accuracy on the test set after 10 epochs with learning rate scheduler. Level 2 experiment pending.
