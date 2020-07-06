# DashCamp_CarSpeed


## Introduction

This repos is an solution to the commaai challenge. that challenge to predict the car speed with only video from Dash Cam located under mirror in front. 

Check this link for more details about the challenge and downloading the data: [speedchallenge](https://github.com/commaai/speedchallenge).


## Optical Flow  

Based on previous attempts, one of the fastest approach in terms of training and performance is to apply the **Optical flow**.

Optical flow is one of the most basic concepts in computer vision, and refers to the apparent motion of objects in the image due to the relative motion between the camera and the scene.

Using Optical flow, can calculate the two components of speed(u,v) using the following equations: 

![equation](OpticalFlowEquation.png)

where **V** and **\omega** are the linear and angular velocities of the camera and **h** is the distance between the camera and the plane(road).

In this approach the angular velocity is neglected and focused on linear velocity. for more details can take a look at this blog and its paper refrencese:[Car speed estimation from a windshild camera](https://nicolovaligi.com/car-speed-estimation-windshield-camera.html).


## Performance   

The train dataset(train.mp4) is divided into the data into **train(95%) and validation(5%)**. 
The mean squared error for train and validation are as follows: 
- Train - 4.7
- Validation - 2.66

## Plot 

### The training graph:

![Train Graph](/training_dataset.png) 


### The valiation graph: 

![Validation Graph](/Validation_Dataset.png)


The speed prediction for test video(test.mp4) is generated and saved in this repo as **test.txt**.


