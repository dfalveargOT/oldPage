---
layout: post
title: CropCount Pineapple
date: 2020-05-01 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: CropCount.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [DeepLearning, Software, Open-Source, OpenCV] # add tag
---
The importance of technology has been impacting all industrial sectors, such as massive objects production, healthcare, agriculture, and others, giving the prospect of growth due to the huge hand made methods that exist in the industry, furthermore the budget inverted in tech-education as well as they invest in innovation make possible to companies to do big steps and stablish good bases for the competitive future.

### The Why
The CropCount project become in production on early of 2019 at Datarock S.A.S offices,  on a speech about innovation and process improvement, the big challenge proposed is to create a software to support the engineering team for replacing the manual count of pineapple crops, in that time many people were counting big image taken by drones each plant of this fruit, and an exhausted feeling was present by the team for the tedious and monotonous work, the solution suggested gave them a better and a healthy way to do their job, the results of the project were satisfying improving time and reducing health hand problems in the employers, the same quantity that a person can count, the software do it with less time, for plant counting-recognizing takes around 50 milliseconds.

![Cropcount]({{site.baseurl}}/assets/img/cropcount/Cropcount-Process.png)

### The process

The research had two approaches, the first version was consist of many traditional open-source tools, and the second version was developed for solving some important issues on the performance of the first version.

#### Version 1.0
This version consists of traditional computer vision tools using OpenCV, Skimage, numpy and others. In the firsts instance the image has to be load as .jpg or .png format, then is used some color spaces and Fourier transform for show important information of the crops, resalting the characteristics that compound a plant, this step is defined as preprocessing step, suddenly the information is filtered by some morphological operation, and segmentation tools for later pass the data to match core process step, where tools like contours finding and blob detector detect the plants, next is used in filter step some vector coordinates modifications to eliminate duplicated counts and increase the overall performance, finally some space filter condiction as well as counting integration for all layers give the coordinates concerning each plant as well as an image drawing the overall process.

![Cropcount]({{site.baseurl}}/assets/img/cropcount/CropCountV1.0.png)

The issues that became important for the development of the second version was, the difficulty to maintain the performance of the software for light and resolution variation, the testing result in a great score for great image conditions (not always present for sun position, cloud density, and drone altitude), thus and idea of standardizing it became complicated, so the only way to reduce the effect of light, contrast, and resolution is using deep learning tools.

All the implementation is available at [CropCount V1.0 repository](https://github.com/dfalveargOT/CropCount_V1.0.git).

![Cropcount]({{site.baseurl}}/assets/img/cropcount/cp15.jpg)

#### Version 2.0


![Cropcount]({{site.baseurl}}/assets/img/cropcount/CropCountP3.png)

