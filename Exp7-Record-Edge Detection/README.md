# Edge Detection

## AIM:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary modules.

### Step 2:
Perform edge detection on a image. 
- Sobel 
- Laplacian
- Canny

### Step 3:
Display the original images with edge detected images.

<br><br><br><br><br><br><br><br><br>

## PROGRAM:
```
/*
Developed by   : Y Chethan
Register Number: 212220230008
*/
```
``` Python
# Import the packages
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("img.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

# SOBEL EDGE DETECTOR
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

# LAPLACIAN EDGE DETECTOR
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

# CANNY EDGE DETECTOR
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```
## OUTPUT:
### SOBEL EDGE DETECTOR
![1](https://user-images.githubusercontent.com/75234991/168417180-31fa9de4-2c3d-4b05-896e-f5c7a051211c.png)

![2](https://user-images.githubusercontent.com/75234991/168417182-c154b351-8b89-4038-bad5-a83abdab35a7.png)

![3](https://user-images.githubusercontent.com/75234991/168417186-cbd69075-77a2-4e6e-9cab-afaefd69a479.png)

### LAPLACIAN EDGE DETECTOR

![4](https://user-images.githubusercontent.com/75234991/168417194-b1f17c38-d18b-4e66-9a6e-7d61ae14bd97.png)

### CANNY EDGE DETECTOR

![5](https://user-images.githubusercontent.com/75234991/168417218-a9a403a3-1c6d-4362-b524-4352cc9693db.png)

## RESULT:
Thus, the edges are detected using Sobel, Laplacian, and Canny edge detectors.
