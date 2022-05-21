# Edge Linking using Hough Transform
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Read image and convert it to grayscale image

### Step 2:
Find the edges in the image using canny detector and display
### Step 3:
Detect points that form a line using HoughLinesP

### Step 4:
Draw lines on the image

### Step 5:
Display the result

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


## Program:
#### Developed By   :Marinto Richee J
#### Register Number:212220230031
```Python
# Read image and convert it to grayscale image
import cv2 
import numpy as np
import matplotlib.pyplot as plt
img=cv2.imread("image_line.webp",0)
img_c=cv2.imread("image_line.webp",1)
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
img_c=cv2.cvtColor(img_c,cv2.COLOR_BGR2RGB)
plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img_c)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gray Image')
plt.imshow(img)
plt.show()
# Find the edges in the image using canny detector and display
canny=cv2.Canny(img,120,150)
plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img_c)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Canny')
plt.imshow(canny)
plt.show()

# Detect points that form a line using HoughLinesP
lines=cv2.HoughLinesP(canny,1,np.pi/180,50,20,2)

# Draw lines on the image
blank_image = np.ones(img.shape, dtype=np.uint8)
for lin in lines:
    x1,y1,x2,y2=lin[0]
    cv2.line(blank_image,(x1,y1),(x2,y2),(255,255,0),2)
    
# Display the result
plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img_c)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Hough Transform')
plt.imshow(blank_image)
plt.show()

```
## Output:

### Input image and grayscale image
![image](https://user-images.githubusercontent.com/65499285/168997358-9b3ee0c7-31c1-4f35-be71-75325b9f5761.png)

### Canny Edge detector output
![image](https://user-images.githubusercontent.com/65499285/168997400-32932bd0-198a-4266-bb70-dd93e9cf0889.png)

### Display the result of Hough transform
![image](https://user-images.githubusercontent.com/65499285/168997462-07f59b7a-2f02-4994-adfd-abdf0797d28c.png)

## Result:
Thus the program is written with python and OpenCV to detect lines using Hough transform. 
