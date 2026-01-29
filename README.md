Computer Vision Image Transformations using OpenCV

Overview:

This project demonstrates fundamental image transformation techniques used in Computer Vision and Image Processing.
Using Python and OpenCV, the project implements and visualizes the following transformations:

✓Translation

✓Rotation

✓Scaling

✓Shearing

✓Affine Transformation

✓Perspective Transformation

These transformations are essential for tasks such as image alignment, object detection preprocessing, camera calibration, and 3D vision.

Objectives:

✓To understand geometric transformations in computer vision

✓To implement image transformations using OpenCV

✓To visualize the effect of each transformation on an image

✓To build a beginner-friendly reference project for learning OpenCV

✓To create a reusable codebase suitable for academic and practical applications

Technological Use:

✓Programming Language: Python

✓Library: OpenCV (cv2)

✓Platform Support:

✓Google Colab

✓Local PC (Windows / Linux)

Why OpenCV?

Fast and optimized image processing

Industry-standard library

Widely used in AI, robotics, and embedded vision systems

How to Run the Project

Option 1: Google Colab (Recommended)

Open Google Colab

Upload image.jpg into the Colab environment

Install OpenCV:

pip install opencv-python


Run the Python script

Output images will be displayed using cv2_imshow()

Option 2: Local System

Install Python (3.8 or above)

Install required libraries:

pip install opencv-python numpy


Place image.jpg in the project folder

Run the script:

python main.py


Output windows will open for each transformation

Project Structure
Computer-Vision-Transformations/

 image.jpg
 main.py
 README.md

Applications

Image preprocessing for Machine Learning

Object detection and tracking

Camera calibration

Robotics and autonomous systems

Medical image analysis

Augmented Reality (AR)

LEARNING OUTCOMES 

After completing this project, users will:

Understand the math behind image transformations

Gain hands-on experience with OpenCV

Be able to modify and apply transformations in real-world projects

COMPUTER VISION IMAGE PYRAMID

Observations
Pyramid Level	Image Resolution	Detail Visibility	Computation
Level 0	High	Fine details visible	High
Level 1	Medium	Moderate details	Medium
Level 2	Low	Large structures only	Low
Level 3	Very Low	Very coarse features	Very Low

Algorithm
1.	Read the input image
2.	Convert the image from BGR to RGB format
3.	Display the original image (Pyramid Level 0)
4.	Apply pyrDown() to generate Level 1 of the pyramid
5.	Repeat downsampling to generate multiple pyramid levels
6.	Display all pyramid levels
7.	Observe image resolution changes and detail loss
8.	Apply edge detection on each pyramid level for comparison
