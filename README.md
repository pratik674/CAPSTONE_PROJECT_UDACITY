# Motivation
You may be quite well versed with identification of  different breeds of dog, for example a Retriever or German SHepherd. There are different types of dog in a particular breed based on color, shape, demography, coat type etc. It gets increasingly difficult to spot differences to an untrained eye. An intuitive way is to compare the image to a prior identified image of the same breed. Convolutional Neural Networks (CNNs) are particularly well-suited for image identification tasks due to their unique architecture and characteristics. 
The architecture of a CNN is in itself  inspired by the visual processing mechanisms of the human brain. It consists of multiple layers of interconnected neurons, organized in a hierarchical manner to progressively learn and extract meaningful features from the input data.
The idea is to use CNN to make our lives easier in letting the algorithm decide which breed of dog it is.

# Project Title 
Convolutional Neural Network approach to dog breed Identification

# Project Description
In this project, we learn how to build a pipeline to process real-world, user-supplied images. Given an image of a dog, my algorithm will identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed. 

# Table of Contents
1. Project Objective
2. Data Exploration
3. Methodology
4. Results
5. Conclusion
6. Libraries installed 
7. Licensing & Acknowledgment

## Project Description
The objective of this project is to come up with an algorithm that will detect dog in the image and identify the breed of the dog. In case it detects human in an image, the algorithm will identify the closest breed of dog resembling the human. 

## Data Exploration
Dataset provided has 8351 dogs and 133 breeds of dog labelled. In addition the human images dataset comprises 13233 images. 

## Methodology
There are 3 main steps in the process:
1. Detection of Dogs in an image
2. Detection of Humans in an image
3. Dog Breed classification (provided that a dog or human was detected)

Deep Learning and specifically CNNs are used for (1) and (3). Human detection is done using facedetection from the OpenCV library. Data Preprocessing of the images consist of transforming images to tensors. This includes resizing and normalizing pixel values.

In this project we first try and implement a CNN from scratch , and we have also attempted to use InceptionV3 pre-trained model without its pre-trained weights.Then we use VGG16 and InceptionV3 via transfer learning, where we use bottleneck features as input to our fully connected neural network.
Finally we take this InceptionV3 model and implement in our algorithm where we input an image and the output shows the classification.

## Results
Face detection , on a limited test, had a perfect recall. Dog detection worked very well on the limited samples tested. The dog breed classification achieved 81% accuracy among the 133 classes, which we consider is a good result, leading to a usable system.

## Conclusion
We have used only two models, and we see that transfer learning aids the image classification process. Our use of InceptionV3 model with pretrained weights shows an accuracy of 81%. Also the training and validation accuracy gap is lower which is indicative that the model was not over fitting data. Neverthless there should be further scope to increase the test accuracy and decrease the validation loss. 

## Libraries installed
Install the following libraries to use this project:
1. Keras
2. OpenCV
3. Matplotlib
4. NumPy
5. Tensorflow
6. glob
7. Jupyter

## Datasets used

Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dog_images.zip). Unzip the folder and place it in the repo, at location `path/to/dog-project/dog_images.`

Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip). Unzip the folder and place it in the repo, at location `path/to/dog-project/lfw.` If you are using a Windows machine, you are encouraged to use 7zip to extract the folder.

Download the [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz) for the dog dataset. Place it in the repo, at location `path/to/dog-project/bottleneck_features.`

Download the [ResNet-50 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogResnet50Data.npz) for the dog dataset. Place it in the repo, at location `path/to/dog-project/bottleneck_features.`

Download the [InceptionV3 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogInceptionV3Data.npz)) for the dog dataset. Place it in the repo, at location `path/to/dog-project/bottleneck_features.`

Download the [Xception bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogXceptionData.npz) for the dog dataset. Place it in the repo, at location ``path/to/dog-project/bottleneck_features.

## Licensing and Acknowledgement
I would like to extend thanks to Udacity( Data Scientist Program) to provide a very smooth and hands on training platform to learn and implement codes pertaining to CNNs

 
