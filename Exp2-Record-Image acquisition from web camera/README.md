# Image Acquisition from Web Camera

## AIM:
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
<br/>i) Write the frame as JPG
<br/>ii) Display the video
<br/>iii) Display the video by resizing the window
<br/>iv) Rotate and display the video

## SOFTWARE REQUIRED:

Anaconda - Python 3.7

## ALGORITHM:

### Step 1:
Write the frame as JPG.
### Step 2:
Display the video.
### Step 3:
Display the video by resizing the window.
### Step 4:
Rotate and display the video.
### Step 5:
End the program and close the output image windows.

<br><br><br>

## PROGRAM:
```
/*
Developed by   : Y Chethan
Register Number: 212220230008
*/
```
```python
# Write the frame as JPG file
import cv2
image = cv2.VideoCapture(0)
while(True):
    ret,frame = image.read()
    cv2.imwrite("NewPicture.jpg",frame)
    result = False
image.release()

# Display the video
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('frame', frame)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

# Display the video by resizing the window
import numpy as np
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=frame.shape[1]
    height=frame.shape[0]
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2] =smaller_frame
    image[:height//2,width//2:]=smaller_frame
    image[height//2:,width//2:]=smaller_frame
    image[height//2:,:width//2]=smaller_frame
    cv2.imshow('resize', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()


# Rotate and display the video
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=frame.shape[1]
    height=frame.shape[0]
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2] =cv2.rotate(smaller_frame,cv2.cv2.ROTATE_180)
    image[:height//2,width//2:]=cv2.rotate(smaller_frame,cv2.cv2.ROTATE_180)
    image[height//2:,width//2:]=smaller_frame
    image[height//2:,:width//2]=smaller_frame
    cv2.imshow('rotate', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```
## OUTPUT:

### i) Write the frame as JPG image
![](images/capture.png)

<br><br>

### ii) Display the video
![](images/videocapture.png)

<br><br><br><br><br><br><br>

### iii) Display the video by resizing the window
![](images/resize.png)

### iv) Rotate and display the video
![](images/rotate.png)

## RESULT:
Thus, the image is accessed from webcamera and displayed using openCV.
