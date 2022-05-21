# Edge Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7


## Algorithm:
### Step 1:
Import the necessary modules.
### Step 2:
For performing edge detection on a image. 
- Sobel 
```python
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)
```
- Laplacian
```python
Laplacian=cv2.Laplacian(img,cv2.CV_64F)
```
- Canny
```python
canny=cv2.Canny(img,120,150)
```
### Step 3:
Display all the images with their respective edge detected images.
 
## Program:
#### Developed By   :Marinto Richee J
#### Register Number:212220230031
``` Python
# Import the packages
import cv2 
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("images.jfif",0)
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
img=cv2.GaussianBlur(img,(3,3),0)
plt.imshow(img)
plt.axis("off")
plt.show()

# SOBEL EDGE DETECTOR
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)

# LAPLACIAN EDGE DETECTOR
Laplacian=cv2.Laplacian(img,cv2.CV_64F)

# CANNY EDGE DETECTOR
canny=cv2.Canny(img,120,150)

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel X axis')
plt.imshow(sobelx)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel Y axis')
plt.imshow(sobely)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel X and Y axis')
plt.imshow(sobelxy)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Canny')
plt.imshow(canny)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian')
plt.imshow(Laplacian)
plt.show()

```
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Output:
### SOBEL EDGE DETECTOR
![sobelx](https://user-images.githubusercontent.com/65499285/168112550-6d99db26-e4b2-4a02-ac41-231c204442dd.png)
![sobely](https://user-images.githubusercontent.com/65499285/168112574-b9e59804-fc44-47f6-bd46-3d22c3ea23fa.png)
![sobelxy](https://user-images.githubusercontent.com/65499285/168112564-bd0d9fa7-d8ef-4460-93f3-618be4106560.png)

### LAPLACIAN EDGE DETECTOR
![lap](https://user-images.githubusercontent.com/65499285/168112779-fb06102b-4427-4efd-9cd0-5ae269c2db89.png)

### CANNY EDGE DETECTOR
![image](https://user-images.githubusercontent.com/65499285/168112104-c5b6759e-5c34-453b-99e0-e19df87d184e.png)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
