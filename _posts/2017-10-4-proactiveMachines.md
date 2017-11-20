---
layout: post
title: 'Proactive Machines Project'
categories: Meta
excerpt: Computer Vision & Machine Learning | OpenCV, Caffe, C++
coverImage: "/images/projects/1.proactiveMachines/workflow.png" 
location: "/meta/2017/10/04/proactiveMachines.html"
---
[Implemented \| Will be further developed (see **Future Work** section)]

[Click to watch a demo](http://www.youtube.com/watch?feature=player_embedded&v=2vS3Db4MVzU)

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


## Demo

**Click image to wacth a demo**

<a href="http://www.youtube.com/watch?feature=player_embedded&v=2vS3Db4MVzU
" target="_blank"><img src="http://img.youtube.com/vi/2vS3Db4MVzU/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>


## Source Code
 
It is an Open Source project hosted on GitHub. [Link to repo](https://github.com/pavlidischrs/proactiveMachines)

## Future Work

In order to extract the image from the inside of the markers, we apply an affine transformation, which warps the inner image. Since our model is not trained in warped images, the network performance will decrease. To resolve this issue we will train a **[1] Spatial Transformer Network** in a distorted MNIST database, which we expect to give us better results.



[1] Jaderberg, Max, Karen Simonyan, and Andrew Zisserman. "Spatial transformer networks." Advances in Neural Information Processing Systems. 2015.




