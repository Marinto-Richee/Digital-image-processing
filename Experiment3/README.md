# Color Conversion
## Aim:
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step 1:
Read an image using imread() and
Convert BGR and RGB to HSV and GRAY<br/>
using:<br/>cv2.cvtColor(image,cv2.COLOR_RGB2HSV)<br/>cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)<br/>cv2.cvtColor(image,cv2.COLOR_BGR2HSV)<br/>cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)<br/>
### Step 2:
Convert HSV to RGB and BGR<br/>
using:<br/>
cv2.cvtColor(image,cv2.COLOR_HSV2RGB)<br/>
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)<br/>
### Step 3:
Convert RGB and BGR to YCrCb<br/>
using:<br/>cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)<br/>cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)<br/>

<br>
<br>
<br>
<br>


### Step 4:
Split and Merge RGB Image
<br>using:<br/>blue = image[:,:,0]<br/>green = image[:,:,1]<br/>red = image[:,:,2]<br/>cv2.merge((blue,green,red))<br/>
### Step 5:
Split and merge HSV Image
<br>using:<br/>hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)<br/>h, s, v = cv2.split(hsv)<br/>cv2.merge((h,s,v))<br/>
## Program:
#### Developed By: Marinto Richee
#### Register Number: 212220230031
```Python 
# i) Convert BGR and RGB to HSV and GRAY

import cv2
image=cv2.imread("212220230031.jpg")
cv2.imshow("Input",image)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY",BGR_GRAY)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY",RGB_GRAY)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb",BGR_YCrCb)
cv2.imshow("Input",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image

blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged",merged)
cv2.imshow("Input",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image

h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>
<br>
<br>

## Output:

### i) BGR and RGB to HSV and GRAY

<img width="168" alt="img1" src="https://user-images.githubusercontent.com/65499285/162554460-943f9a37-9b39-44ed-97bb-a28d28b72ea8.png">

<img width="340" alt="img2" src="https://user-images.githubusercontent.com/65499285/162554524-35dcff11-9be1-4f9f-b728-a274b1591e51.png">

<img width="338" alt="img3" src="https://user-images.githubusercontent.com/65499285/162554722-ada6a3b1-51c7-4a9a-91be-4591272ff027.png">

<br>
<br>
<br>
<br>
<br>
<br>
<br>

### ii) HSV to RGB and BGR

<img width="509" alt="img4" src="https://user-images.githubusercontent.com/65499285/162554738-45ae93e3-0ecb-4a25-855d-e8746e0e6a98.png">

### iii) RGB and BGR to YCrCb

<img width="509" alt="img5" src="https://user-images.githubusercontent.com/65499285/162554744-475ae704-7239-47c7-a28a-1d10e1631e05.png">

### iv) Split and merge RGB Image

<img width="512" alt="img6" src="https://user-images.githubusercontent.com/65499285/162554753-53073027-21c4-4043-8312-0a31fa3b4267.png">

<img width="341" alt="img7" src="https://user-images.githubusercontent.com/65499285/162554755-570ad917-2724-4965-a38f-9d33c6b2a7d6.png">

### v) Split and merge HSV Image

<img width="506" alt="img8" src="https://user-images.githubusercontent.com/65499285/162554765-35e1940a-7aeb-432c-8eaa-5154b66b8471.png">

<img width="341" alt="img9" src="https://user-images.githubusercontent.com/65499285/162554769-1032ac7c-e8a7-40ab-8340-dadf12e9129d.png">

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
