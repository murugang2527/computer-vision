# Basic Image Processing Operations using OpenCV

  Description:

    This experiment demonstrates multiple basic image processing techniques using OpenCV. It includes grayscale conversion, cropping, resizing, thresholding, contour detection, and blob detection.
  
  Objective:
  
    To perform grayscale conversion
    To crop and resize an image
    To apply thresholding
    To detect contours in an image
    To perform blob detection

  Requirements:
  
    Python 3.x
    OpenCV
    NumPy
    
# Code

import cv2 
import numpy as np
from google.colab.patches import cv2_imshow
from google.colab import files

# ---- Upload Image ----
uploaded = files.upload()    # Upload sample.jpg

# ---- Load the image ----
image = cv2.imread("sample.jpg")
if image is None:
    print("Image not found!")
else:
    print("Image Loaded Successfully!")

# Convert to grayscale
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Crop the image
cropped = image[50:200, 100:300]

# Resize the image
resized = cv2.resize(image, (300, 200))

# Thresholding
_, thresh = cv2.threshold(gray, 127, 255, cv2.THRESH_BINARY)

# Find contours
contours, _ = cv2.findContours(thresh, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)
contour_img = image.copy()
cv2.drawContours(contour_img, contours, -1, (0, 255, 0), 2)

# Blob detection
params = cv2.SimpleBlobDetector_Params()
params.filterByArea = True
params.minArea = 150
detector = cv2.SimpleBlobDetector_create(params)
keypoints = detector.detect(gray)
blob_img = cv2.drawKeypoints(image, keypoints, np.array([]), (0,0,255),
                             cv2.DRAW_MATCHES_FLAGS_DRAW_RICH_KEYPOINTS)

# ---- Display outputs ----
print("Cropped Image:")
cv2_imshow(cropped)

print("Resized Image:")
cv2_imshow(resized)

print("Threshold Image:")
cv2_imshow(thresh)

print("Contour Detection:")
cv2_imshow(contour_img)

print("Blob Detection:")
cv2_imshow(blob_img)

  Input:

    Image file uploaded by the user (e.g., sample.jpg)

  Output:

    The following outputs are displayed:
  
    Cropped Image
    Resized Image
    Threshold Image
    Contour Detection Image
    Blob Detection Image

  Conclusion

    This experiment successfully demonstrates multiple fundamental image processing operations and helps in understanding how different techniques are applied in computer vision.
