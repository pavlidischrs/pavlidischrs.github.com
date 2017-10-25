---
layout: post
title: 'Musicology App'
categories: Meta
excerpt: Application for Musicians & Musicologists | Qt SDK, C++
coverImage: "/images/projects/2.musicology/sequence.png"
location: "/meta/2017/10/03/musicology"
---

## Intro

This is an application for exercising in Counterpoint. 

A **Counterpoint System** consists of two pentagrams, where the lower pentagram is filled with a Sequence of Musical Notes and the upper pentagram is empty. The musicologist-user has to fill the upper pentagram with the right Musical Notes according to musicological rules.





<img src="{{ site.github.url }}/images/projects/2.musicology/appImage.png" width="500">




**Note!** Currently, the rules are imaginary so you can see a demo of the app to check the workflow.

<br/>

## Algorithm Description

Each Musical Symbo has an **ID**. Currently we have 10 Musical Notes so IDs are from 0 to 9. 

## Back End

The Given Exercise and the Given Answer are represented with a vector of integers, where each number is the ID of a Musical Symbol.

The evaluation procedure checks if the Given Exercise and Answer obey the rules.



## Front End 

We use the QT Framework to implement the GUI of the app. 

Each Musical Symbol is a **MusicalNoteItem** (inherits from QGraphicsPixmapItem) and it is showed in the GUI with **QGraphicsScene** and **QGraphicsView**.


**More details could be found in the [repo](https://github.com/pavlidischrs/musicology/musicology)**.

## Source Code

It is an Open Source project hosted on GitHub. [Link to repo](https://github.com/pavlidischrs/musicology)
