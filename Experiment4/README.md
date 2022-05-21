# Histogram and Histogram Equalization of an image
## Aim:
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:<br>

Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step 2:<br>

Calculate the Histogram of Gray scale image and each channel of the color image.

### Step 3:<br>

Display the histograms with their respective images.

### Step 4:<br>

Equalize the grayscale image.

### Step 5:

Display the grayscale image.
<br><br><br><br><br>
## Program:
#### Developed By   :Marinto Richee J
#### Register Number:212220230031
```python
import cv2
import matplotlib.pyplot as plt
Color_image=cv2.imread('img.jfif')
Color_image=cv2.cvtColor(Color_image,cv2.COLOR_BGR2RGB)
Gray_image=cv2.imread('img.jfif',0)
Gray_image=cv2.cvtColor(Gray_image,cv2.COLOR_BGR2RGB)
plt.subplot(1,2,1)
plt.title("Color Image")
plt.axis("off")
plt.imshow(Color_image)
plt.subplot(1,2,2)
plt.title("Gray Scale Image")
plt.axis("off")
plt.imshow(Gray_image)
plt.show()

# Write your code to find and display the histogram of gray scale image and color image channels.
hist=cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.subplot(2,1,1)
plt.title("Red Channel Histogram")
plt.xlabel("Intensity value")
plt.ylabel("pixel count")
plt.stem(hist)
Red=Color_image[:,:,0]
plt.subplot(2,1,2)
plt.title("Red Channel Image")
plt.axis("off")
plt.imshow(Red)
plt.tight_layout()
plt.show()

hist=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.subplot(2,1,1)
plt.title("Green Channel Histogram")
plt.xlabel("Intensity value")
plt.ylabel("pixel count")
plt.stem(hist)
Green=Color_image[:,:,1]
plt.subplot(2,1,2)
plt.title("Green Channel Image")
plt.axis("off")
plt.imshow(Green)
plt.tight_layout()
plt.show()

hist=cv2.calcHist([Color_image],[2],None,[256],[0,256])
plt.subplot(2,1,1)
plt.title("Blue Channel Histogram")
plt.xlabel("Intensity value")
plt.ylabel("pixel count")
plt.stem(hist)
Blue=Color_image[:,:,2]
plt.subplot(2,1,2)
plt.title("Blue Channel Image")
plt.axis("off")
plt.imshow(Blue)
plt.tight_layout()
plt.show()


# Write the code to perform histogram equalization of the image. 
equ=cv2.equalizeHist(cv2.imread('img.jfif',0))
equ=cv2.cvtColor(equ,cv2.COLOR_BGR2RGB)
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ)

```
## Output:
### Input Grayscale Image and Color Image

<br>![1](https://user-images.githubusercontent.com/65499285/164491965-07b8931a-5a5b-4eac-8f32-8a2b9094ef09.png)
<br>
<br><br><br><br><br><br>
### Histogram of Grayscale Image and any channel of Color Image
<br>![2](https://user-images.githubusercontent.com/65499285/164492333-af64de22-4c19-46b5-9c3c-5beed6313863.png)
<br>
![3](https://user-images.githubusercontent.com/65499285/164492436-901f7194-9a37-4fe5-b719-4152025e57e5.png)
<br>
![4](https://user-images.githubusercontent.com/65499285/164492793-3a7afec8-605b-41c0-8d22-6fc55d7ad553.png)
<br>

### Histogram Equalization of Grayscale Image
<br>![6](https://user-images.githubusercontent.com/65499285/164492215-8e4b874f-ecb1-433c-8188-9389544892ff.png)
<br>


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
