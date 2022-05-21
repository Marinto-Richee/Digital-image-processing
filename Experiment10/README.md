# Implementation of Erosion and Dilation
## Aim:
To implement Erosion and Dilation using Python and OpenCV.
## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element
### Step 4:
Erode and Dilate the image
### Step 5:
Display all the results

<br>
<br>
<br>
<br>
<br>

## Program:
#### Developed By: Marinto Richee
#### Register Number: 212220230031
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image_white=np.full((100,600),20,dtype='uint8')
image_white=cv2.cvtColor(image_white,cv2.COLOR_BGR2RGB)
image_white = cv2.copyMakeBorder(image_white, 10, 10, 10, 10, cv2.BORDER_CONSTANT, value=[255, 255, 0])
name_image=cv2.putText(image_white,"Marinto Richee J",(35,80),cv2.FONT_HERSHEY_DUPLEX,2,255,5,cv2.LINE_AA)
plt.axis("off")
plt.title("Original image")
plt.imshow(name_image)
plt.show()

# Create the structuring element
kernel=np.ones((6,6),np.uint8)

# Erode the image
image_erode=cv2.erode(name_image,kernel)

# Dilate the image
image_dilate=cv2.dilate(name_image,kernel)

#Display the images
plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title("Dilate")
plt.imshow(image_dilate)
plt.subplot(1,2,2)
plt.axis("off")
plt.title("Erode")
plt.imshow(image_erode)
plt.show()
```
<br>
<br>
<br>

## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/65499285/169638750-e5d7840d-d6b8-4668-a08c-c430c65097ed.png)
### Display the Eroded Image and Dilated Image
![image](https://user-images.githubusercontent.com/65499285/169638756-25cc2233-39d4-4dc0-a317-1ad41e682e01.png)

## Result:
Thus the generated text image is eroded and dilated using python and OpenCV.
