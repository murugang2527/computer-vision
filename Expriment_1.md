## Image Upload and Display using OpenCV:
  
  Description:
  
    This experiment demonstrates how to upload an image in Google Colab, read it using OpenCV, and display it. It helps in understanding basic image handling operations in computer vision.
    
  Objective:
  
    To upload an image using Google Colab
    To read the image using OpenCV (cv2)
    To display the image using cv2_imshow
    
  Requirements:
  
    Python 3.x
    OpenCV library
  How to Run:
  
    Open Google Colab
    Copy and paste the code below
    Run the cell
    Upload any image (e.g., sample.jpg) when prompted
    The uploaded image will be displayed
    
# CODE:
  
# Install OpenCV (run once)
!pip install opencv-python

# Import required libraries
import cv2
from google.colab.patches import cv2_imshow
from google.colab import files

# Step 1: Upload the image
uploaded = files.upload()   # Upload any image (e.g., sample.jpg)

# Step 2: Get the uploaded file name
image_path = list(uploaded.keys())[0]

# Step 3: Read the uploaded image
image = cv2.imread(image_path)

# Step 4: Check and display
if image is None:
    print("Error: Image not found or path is incorrect")
else:
    print("Image successfully loaded!")
    cv2_imshow(image)
    
# Input:

  User uploads an image file (e.g., JPG, PNG)
  
# Output:

  The uploaded image is displayed in the output cell

# Conclusion:

  This experiment successfully demonstrates how to upload, read, and display an image using OpenCV in Google Colab.
