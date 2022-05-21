# Thresholding
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages
### Step2:
Read the Image and convert to grayscale
### Step3:
Use Global thresholding to segment the image
### Step4:
Use Adaptive thresholding to segment the image
### Step5:
Use Otsu's method to segment the image 
### Step6:
Display the results
## Program
#### Developed By   :Marinto Richee J
#### Register Number:212220230031
```python
# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read the Image and convert to grayscale
image=cv2.imread("image face.webp",1)
image=cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
image_gray=cv2.imread("image face.webp",0)

# Use Global thresholding to segment the image
ret,thresh_img1=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(image_gray,100,255,cv2.THRESH_TRUNC)

# Use Adaptive thresholding to segment the image
thresh_img7=cv2.adaptive Threshold(image_gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img8=cv2.adaptive Threshold(image_gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)

# Use Otsu's method to segment the image 
ret,thresh_img6=cv2.threshold(image_gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)

# Display the results
titles=["Gray Image","Threshold Image (Binary)","Threshold Image (Binary Inverse)","Threshold Image (To Zero)"
       ,"Threshold Image (To Zero-Inverse)","Threshold Image (Truncate)","Otsu","Adaptive Threshold (Mean)","Adaptive Threshold (Gaussian)"]
images=[image_gray,thresh_img1,thresh_img2,thresh_img3,thresh_img4,thresh_img5,thresh_img6,thresh_img7,thresh_img8]
for i in range(0,9):
    plt.figure(figsize=(10,10))
    plt.subplot(1,2,1)
    plt.title("Original Image")
    plt.imshow(image)
    plt.axis("off")
    plt.subplot(1,2,2)
    plt.title(titles[i])
    plt.imshow(cv2.cvtColor(images[i],cv2.COLOR_BGR2RGB))
    plt.axis("off")
    plt.show()

```
## Output

### Original Image
![image](https://user-images.githubusercontent.com/65499285/169066947-59fe96a2-fb21-4444-af89-a1ba140c2d78.png)


### Global Thresholding
![image](https://user-images.githubusercontent.com/65499285/169067010-b3116dec-6f23-4f98-add8-b0ec3bc6c41d.png)
![image](https://user-images.githubusercontent.com/65499285/169067026-df5a1925-df4e-447a-a54c-8f883d901254.png)
![image](https://user-images.githubusercontent.com/65499285/169067053-7bac14c6-e601-4256-88b5-b610db136464.png)
![image](https://user-images.githubusercontent.com/65499285/169067076-624f128d-e9bf-4269-9df1-822ec3a95c00.png)
![image](https://user-images.githubusercontent.com/65499285/169067098-c603714b-cd79-4a15-9203-63e253f76b7e.png)

### Adaptive Thresholding
![image](https://user-images.githubusercontent.com/65499285/169067229-f9a4ed19-fe51-44f6-8fa5-5cf696f7376d.png)
![image](https://user-images.githubusercontent.com/65499285/169067241-0e38b048-c573-4ba3-acb8-cc949760ad71.png)

### Optimum Global Thesholding using Otsu's Method
![image](https://user-images.githubusercontent.com/65499285/169067266-74a11cf4-68e3-46e2-812f-58ea8f61eceb.png)


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
