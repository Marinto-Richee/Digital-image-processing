# Opening and Closing

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages
### Step 2:
Read the image
### Step 3:
Create the structuring element
### Step 4:
Use Opening operation
### Step 5:
Use Closing Operation
### Step 6:
Display all the output images

## Program:
#### Developed By: Marinto Richee
#### Register Number: 212220230031

``` Python
# Import the necessary packages
import cv2
import matplotlib.pyplot as plt

# Read the image
image=cv2.imread("image_open_close.jpg",0)
image=cv2.cvtColor(image,cv2.COLOR_GRAY2RGB)

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(image,cv2.MORPH_OPEN,kernel)

# Use Closing Operation
image2=cv2.morphologyEx(image,cv2.MORPH_CLOSE,kernel)

```
## Output:

### Display the input Image

![image](https://user-images.githubusercontent.com/65499285/169962223-42584e37-02d9-4d42-a755-8b45fb24b5b1.png)

### Display the result of Opening

![image](https://user-images.githubusercontent.com/65499285/169962180-eb254419-7507-4736-86b4-f86690c9a714.png)

### Display the result of Closing

![image](https://user-images.githubusercontent.com/65499285/169962269-d3389943-3b21-4f8a-8fa7-f4e8ba1d79cc.png)

## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
