# READ AND WRITE AN IMAGE

## AIM:
To write a python program using OpenCV to do the following image manipulations. 
i) Read and display the image
ii) Write the image
iii) Shape of the Image
iv) Access rows and columns
v) Cut and paste portion of image
## SOFTWARE REQUIRED:
Anaconda - Python 3.7
## ALGORITHM:
### Step 1: 
Choose an image and save it as image.jpg
### Step 2:
Use imread(image, flags) to read the file.
### Step 3:
Use imshow(window_name, image) to display the image.
### Step 4:
Use imwrite(filename, image) to write the image.
### Step 5:
End the program and close the output image windows.
## PROGRAM:
```
# Developed By: Y Chethan 
# Register Number: 212220230008
# To Read,display the image

import cv2
image=cv2.imread("/Downloads/images.jpg",1)
cv2.imshow("21220230008_monkey",image)
cv2.waitKey(60)
cv2.destroyWindow()

# To write the image

cv2.imwrite("img.jpg",image)

# Find the shape of the Image

image.shape

# To access rows and columns

column=image.shape[1]
row=image.shape[0]
image=cv2.imread("image.jpg",1)
for i in range(95,129):
  for j in range(95,129):
    image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2.imshow(image)
cv2.waitKey(60)
cv2.destroyWindow()

# To cut and paste portion of image

cut=image[80:120,80:120]
image[40:80,40:80]=cut
cv2.imshow(image)
cv2.waitKey(60)
cv2.destroyWindow()
```

## OUTPUT:
### i) Read and display the image
![](images/show.png)
### ii)Write the image
![](images/write.png)
### iii)Shape of the Image
![](images/shape.png)
### iv)Access rows and columns
![](images/access.png)
### v)Cut and paste portion of image
![](images/cut.png)
## RESULT:
Thus the images are read, displayed, and written successfully using the python program.
