---
layout: post
title: 'Proactive Machines Project'
categories: Meta
excerpt: Computer Vision & Machine Learning | OpenCV, Caffe, C++
coverImage: "/images/projects/1.proactiveMachines/workflow.png" 
location: "/meta/2017/10/04/proactiveMachines.html"
---
[Implemented \| Will be further developed (see **Future Work** section)]


## Intro

This is a **Computer Vision - Machine Learning (Deep Learning)** application to detect and recognise a digit from the **MNIST** database. 
Detection and Recognition modules have been implemented to detect an image and recognise it (Details Below). 
You can see the workflow of the software in the below image.


<br/>

<img src="{{ site.github.url }}/images/projects/1.proactiveMachines/workflow.png " class="fit image">


<br />



## Detection Module
The detection module uses the **OpenCV** library to extract a part of the Web Camera's image which is on the inside of 3 Markers ([check image](https://github.com/pavlidischrs/proactiveMachines/blob/master/files/imageWithMarkers.png)). 

Exploits the property that the concentric squares (Markers) have **Contours** with the same **Mass Center**. 

The module **detects** the Markers and **extracts** the inner image. 

[It should work with other concentric shapes as well]

## Recognition Module

The recognition module uses the **Caffe framework** and the **LeNet CNN** to classify the image and finally recognise the digit.

A network has been trained with this [network model](https://github.com/pavlidischrs/proactiveMachines/blob/master/files/networkArchtecture.prototxt) and you can find a pre-trained model in [this directory](https://github.com/pavlidischrs/proactiveMachines/blob/master/files/).

It could be used any network and pre-trained model.




## Source Code
 
It is an Open Source project hosted on GitHub. [Link to repo](https://github.com/pavlidischrs/proactiveMachines)

## Future Work

One issue of the detection module is that if you monitor an image with a big angle (which means that the markers are not aligned horizontally and vertically), it extracts a part of the inner image. This issue could be managed with an affine transformation of the image. Since the transformed image will be warped we expect that network performance will be decreased. To resolve this issue we will use the so-called **[1] Spatial Transformer Network** to retain the accuracy of our classification.

[1] Jaderberg, Max, Karen Simonyan, and Andrew Zisserman. "Spatial transformer networks." Advances in Neural Information Processing Systems. 2015.




