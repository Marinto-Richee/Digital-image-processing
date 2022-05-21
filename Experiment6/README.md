# Implementation of Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the necessary modules.
### Step 2:
For performing smoothing operation on a image. 
- Average filter
```python
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
- Weighted average filter
```python
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```
- Gaussian Blur 
```python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
```
- Median filter
```python 
median_blur=cv2.medianBlur(image,11)
```
### Step 3:
For performing sharpening on a image.
- Laplacian Kernel
```python
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```
- Laplacian Operator
```python
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```
### Step 4:
Display all the images with their respective filters.

## Program:
#### Developed By   :Marinto Richee J
#### Register Number:212220230031
### 1. Smoothing Filters

i) Using Averaging Filter
```Python
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Average Filter image')
plt.imshow(average_filter_image)
plt.show()
```
ii) Using Weighted Averaging Filter
```Python
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image[30:200,50:200])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(wt_average_filter_image[30:200,50:200])
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gaussian Filter image')
plt.imshow(gaussian_blur)
plt.show()
```

iv) Using Median Filter
```Python
median_blur=cv2.medianBlur(image,11)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Median Filter image')
plt.imshow(median_blur)
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Kernel Filter image')
plt.imshow(lap_image)
plt.show()
```
ii) Using Laplacian Operator
```Python
Lap_blur=cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Filter image')
plt.imshow(Lap_blur)
plt.show()
```

## Output:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
![image](https://user-images.githubusercontent.com/65499285/165766783-c7d9ba8a-6a3e-4170-a8d5-970d6919968c.png)
</br>

ii) Using Weighted Averaging Filter
</br>
![image](https://user-images.githubusercontent.com/65499285/165766843-071694a5-4da5-4d6f-81b1-5e2f7fc06270.png)
</br>

iii) Using Gaussian Filter
</br>
![image](https://user-images.githubusercontent.com/65499285/165766935-201ba902-ab8a-4671-aaac-ce1d4c797fb3.png)
</br>

iv) Using Median Filter
</br>
![image](https://user-images.githubusercontent.com/65499285/165766977-ada6db0f-0c17-4802-9cd9-ab704e5efd00.png)
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
![image](https://user-images.githubusercontent.com/65499285/165767006-d3eebdfe-eac9-497b-84ee-dfb5f0dc0612.png)
</br>

ii) Using Laplacian Operator
</br>
![image](https://user-images.githubusercontent.com/65499285/165767030-82cf0efb-da69-4162-9594-05c188cf90b5.png)
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
