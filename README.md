# Triplet-Based-Iris-Recognition

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/19x3JzRwZhG4WwpDHTAZH3did6xsE6ppb?usp=sharing)

A new iris recognition system. The core of it is a CNN trained using the triplet based training framework.

Here, we will use Ubiris dataset http://iris.di.ubi.pt/ubiris2.html we used a subset of the dataset which in total contains images from 105 different identities.
For each person, there are 15 different images.
![Screenshot](https://github.com/moeinheidari/Triplet-Based-Iris-Recognition/blob/main/Images/dataset.png)

# Network Architecture 
We used a siamese network with triplet loss. The architecture consists of a resnet-101 backbone and a then 128 resulting feature map in the last layer.
Each image goes through the network and results in a vector of size 128, the triplet loss between anchor, positive(image with same identity as anchor image) and  negative(image with different identity as anchor image)  is computed as follows :
![Screenshot](https://github.com/moeinheidari/Triplet-Based-Iris-Recognition/blob/main/Images/network.png)
![Screenshot](https://github.com/moeinheidari/Triplet-Based-Iris-Recognition/blob/main/Images/Triplet_loss.png)
# Results

Training curves :

![Screenshot](https://github.com/moeinheidari/Triplet-Based-Iris-Recognition/blob/main/Images/loss.png)

Dissimilarity scores for pairs of images in validation set :

*Note that the leftmost image is the anchor image, the middle one is the positive and the rightmost image is the negative one.

![Screenshot](https://github.com/moeinheidari/Triplet-Based-Iris-Recognition/blob/main/Images/test.png)

