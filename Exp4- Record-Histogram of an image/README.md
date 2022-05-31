# Histogram and Histogram Equalization of an image
## AIM:
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
### Step 2:
Calculate the Histogram of Gray scale image and any one channel of the color image.
### Step 3:
Display the histograms.
### Step 4:
Equalize the grayscale image.
### Step 5:
Display the equalized grayscale image.

<br><br><br><br>

## PROGRAM:
```
/*
Developed by   : Y Chethan
Register Number: 212220230008
*/
```
```python
import cv2
import matplotlib.pyplot as plt
gray_img=cv2.imread("img1.jpg",0)
color_img=cv2.imread("img.jpg",-1)
gray_img=cv2.cvtColor(gray_img,cv2.COLOR_BGR2RGB)
color_img=cv2.cvtColor(color_img,cv2.COLOR_BGR2RGB)
plt.subplot(1,2,1)
plt.title("Color Image")
plt.axis("off")
plt.imshow(color_img)
plt.subplot(1,2,2)
plt.title("Gray Scale Image")
plt.axis("off")
plt.imshow(gray_img)
plt.show()

# Write your code to find the histogram of gray scale image and color image channels.
hist=cv2.calcHist([gray_img],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("grayscale value")
plt.ylabel("pixel count")
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image
hist=cv2.calcHist([color_img],[0],None,[256],[0,256])
plt.title("Histogram of Color Image:Red Channel")
plt.xlabel("Intensity value")
plt.ylabel("pixel count")
plt.stem(hist)
plt.show()

# Write the code to perform histogram equalization of the image. 
equ=cv2.equalizeHist(cv2.imread('img1.jpg',0))
equ=cv2.cvtColor(equ,cv2.COLOR_BGR2RGB)
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ)
plt.show()
```

## OUTPUT:
### Input Grayscale Image and Color Image
![output1](https://user-images.githubusercontent.com/75234991/164647799-e2175ac2-186d-44fb-8718-3cff54e56648.jpg)

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### Histogram of Grayscale Image and any channel of Color Image
![output2](https://user-images.githubusercontent.com/75234991/164647826-b4940043-2ff5-49eb-a144-c57298206971.jpg)

### Histogram Equalization of Grayscale Image
![output3](https://user-images.githubusercontent.com/75234991/164647852-9c38eb00-d8fe-43a4-8fbb-ef20f0cfb927.jpg)

## RESULT:
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also, histogram equalization is done for the gray scale image using OpenCV.
