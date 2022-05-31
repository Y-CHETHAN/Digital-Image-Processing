# Color Conversion
## AIM:
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Convert BGR and RGB to HSV and GRAY.
### Step 2:
Convert HSV to RGB and BGR.
### Step 3:
Convert RGB and BGR to YCrCb.
### Step 4:
Split and Merge RGB Image.
### Step 5:
Split and merge HSV Image.

<br><br><br><br><br><br><br>

## PROGRAM:
```
/*
Developed by   : Y Chethan
Register Number: 212220230008
*/
```
```python
# Convert BGR and RGB to HSV and GRAY
import cv2
image=cv2.imread("rgb.jpg")
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV image",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY image",BGR_GRAY)
cv2.imshow("212220230008",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV image",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY image",RGB_GRAY)
cv2.imshow("212220230008",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Convert HSV to RGB and BGR
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV image",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB image",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR image",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Convert RGB and BGR to YCrCb
RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb image",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb image",BGR_YCrCb)
cv2.imshow("212220230008",image)
cv2.waitKey(0)
cv2.destroyAllWindows()


# Split and Merge RGB Image
blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged Image",merged)
cv2.imshow("212220230008",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Split and merge HSV Image
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV image",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## OUTPUT:

### i) BGR and RGB to HSV and GRAY
<img width="662" alt="img1" src="https://user-images.githubusercontent.com/75234991/162476234-ba56823c-26df-47bd-b047-bab33ac3ddd1.png">

<img width="662" alt="img2" src="https://user-images.githubusercontent.com/75234991/162476250-cad28f92-e920-4f64-a064-8dda408dae51.png">

<br><br><br><br><br><br><br>

### ii) HSV to RGB and BGR
<img width="663" alt="img3" src="https://user-images.githubusercontent.com/75234991/162479618-e5a065ec-d5e6-432c-9cf9-0bc603264dbe.png">

### iii) RGB and BGR to YCrCb
<img width="661" alt="img4" src="https://user-images.githubusercontent.com/75234991/162476321-298a4480-1e5b-4807-9374-98ee46ebcbc0.png">

### iv) Split and merge RGB Image
<img width="659" alt="img5" src="https://user-images.githubusercontent.com/75234991/162476371-6eff61ae-866e-41b9-bcd9-fc50464fa9bc.png">

<img width="661" alt="img6" src="https://user-images.githubusercontent.com/75234991/162476410-6f1402f0-0356-4794-92aa-3b63ad0920f4.png">

### v) Split and merge HSV Image
<img width="663" alt="img7" src="https://user-images.githubusercontent.com/75234991/162476425-463a36eb-d460-4b88-ad32-f55088d41f12.png">

<img width="661" alt="img8" src="https://user-images.githubusercontent.com/75234991/162476435-53dc2c4d-7d10-40b4-a178-3f8cf9520101.png">

## RESULT:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
