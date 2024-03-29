﻿# face_detection
Project Overview

The aim of this project is to create a classifier which, when given an image, can identify and mark any human faces within the image.


Our Implementation

For the purpose of our project, we used a public implementation of Multi-task Cascaded Neural Networks (MTCNN).

This implementation works in three stages.

In the first stage, the image is scaled multiple times to construct an image pyramid, and each image is passed through the Convolutional Neural Network (CNN) appropriate to the scaling.
In stage two the image is split into patches, and sent through another CNN.
Stage three looks for facial landmarks (and in finding those landmarks, automatically aligns the face).

The training data is passed through the three stages, and thus a detector is created.

We can than feed our program an image, and it will then proceed to first detect faces in the image, and then mark them.

The result is then displayed via Matplotlib.

Results
For the purpose of testing our program, we took ten images from Google Images, with the idea of having varied situations. (Images included in the ‘images’ folder)

The images consist of a varying number of people, with varying lighting conditions and distance to the camera. Two of the images do not contain people, one being of dogs and one of masks modeled after people.

What we observed was that the detector was able to find most of the faces in the images. However, it struggled to detect partial faces, faces at a distance, and partially turned faces.

It correctly detected the face of one dog, with a false positive in another part of the image (which frankly says more about the dog than the detector).
It detected most of the masks as well.
