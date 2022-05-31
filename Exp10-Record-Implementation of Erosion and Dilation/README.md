# Implementation of Erosion and Dilation

## AIM:
To implement Erosion and Dilation using Python and OpenCV.
## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Erode the image.
### Step 5:
Dilate the image.

## PROGRAM:
```
/*
Developed by   : Y Chethan
Register Number: 212220230008
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img1,'Y Chethan',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img1)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Erode the image
image_erode1=cv2.erode(img1,kernel)
plt.axis('off')
plt.imshow(image_erode1)
plt.show()

# Dilate the image
image_dilate1=cv2.dilate(img1,kernel)
plt.axis('off')
plt.imshow(image_dilate1)
plt.show()
```
## OUTPUT:

### Display the input Image
![download](https://user-images.githubusercontent.com/75234991/169637861-57666945-2a48-4cb1-8b9c-4be68dbfe5f3.png)

### Display the Eroded Image
![download (1)](https://user-images.githubusercontent.com/75234991/169637864-7c64ff44-e458-4cad-9fcf-6abe3beeea2e.png)

### Display the Dilated Image
![download (2)](https://user-images.githubusercontent.com/75234991/169637867-f09041a5-46f5-4ae7-a459-27a08accd362.png)

## RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.
