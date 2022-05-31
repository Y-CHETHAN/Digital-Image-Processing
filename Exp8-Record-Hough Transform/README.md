# Edge Linking using Hough Transform

## AIM:
To write a Python program to detect the lines using Hough Transform.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Read image and convert it to grayscale image.

### Step 2:
Find the edges in the image using canny detector and display.

### Step 3:
Detect points that form a line using HoughLinesP.

### Step 4:
Draw lines on the image.

### Step 5:
Display the result.

## PROGRAM:
```
/*
Developed by   : Y Chethan
Register Number: 212220230008
*/
```
```Python
# Read image and convert it to grayscale image
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("img.jpg",0)
img_c=cv2.imread("img.jpg",1)
img_c=cv2.cvtColor(img_c,cv2.COLOR_BGR2RGB)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.figure(figsize=(13,13))
plt.subplot(1,2,1)
plt.imshow(img_c)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gray)
plt.title("Gray Image")
plt.axis("off")
plt.show()

# Find the edges in the image using canny detector and display
canny=cv2.Canny(gray,120,150)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

# Detect points that form a line using HoughLinesP
lines=cv2.HoughLinesP(canny,1,np.pi/180,threshold=80,minLineLength=50,maxLineGap=250)

# Draw lines on the image
for line in lines:
    x1,y1,x2,y2=line[0]
    cv2.line(img_c,(x1,y1),(x2,y2),(255,0,0),3)

# Display the result
plt.imshow(img_c)
plt.title("Result Image")
plt.axis("off")
plt.show()

```
## OUTPUT:

### Input image and grayscale image

![1](https://user-images.githubusercontent.com/75234991/169073193-edb7dc65-76c9-4d79-a35f-0225a2fb9dab.png)

### Canny Edge detector output

![2](https://user-images.githubusercontent.com/75234991/169073230-479b5772-805d-463f-afac-97ad89786c3c.png)

### Display the result of Hough transform

![3](https://user-images.githubusercontent.com/75234991/169073275-5fe84886-cbb2-446e-8dd6-b2930b90b457.png)

## RESULT:
Thus, the program is written with python and OpenCV to detect lines using Hough transform. 
