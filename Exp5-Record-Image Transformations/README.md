# IMAGE TRANSFORMATION
## AIM:
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step 2:
Translate the image.
### Step 3:
Scale the image.
### Step 4:
Shear the image.
### Step 5:
Reflect of image.
### Step 6:
Rotate the image.
### Step 7:
Crop the image.
### Step 8:
Display all the Transformed images.
## PROGRAM:
```
/*
Developed by   : Y Chethan
Register Number: 212220230008
*/
```
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("img.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape

# Image Translation
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

# Image Scaling
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

# Image shearing
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()

# Image Reflection
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

# Image Rotation
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

# Image Cropping
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```

<br><br><br><br><br>

## OUTPUT:
### i) Image Translation
![img1](https://user-images.githubusercontent.com/75234991/165430561-76159820-7f51-4f1a-889d-8cb76b4ddda3.png)

### ii) Image Scaling
![img2](https://user-images.githubusercontent.com/75234991/165430570-3d03f8d0-31fe-4569-8cc6-39ed21b057b6.png)

### iii) Image shearing
![img3_1](https://user-images.githubusercontent.com/75234991/165430639-a69b3056-98cf-4bc8-97d6-46a9c693cc6d.png)

![img3_2](https://user-images.githubusercontent.com/75234991/165430664-252e01db-0ac9-4483-90ca-103f9b4c9933.png)

### iv) Image Reflection
![img4_1](https://user-images.githubusercontent.com/75234991/165430691-a654c5ec-8a25-4724-bcfd-6fce08d1acb4.png)

![img4_2](https://user-images.githubusercontent.com/75234991/165430702-eeac0fff-05ef-4bd4-b3e1-c64827988c20.png)

<br><br><br><br><br><br>

### v) Image Rotation
![img5](https://user-images.githubusercontent.com/75234991/165430723-964c9038-8ac9-48fa-bfe0-30e4dbc8a6b1.png)

### vi) Image Cropping
![img6](https://user-images.githubusercontent.com/75234991/165430744-9370b364-0ebc-458c-8495-390da967fd19.png)

## RESULT:
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
