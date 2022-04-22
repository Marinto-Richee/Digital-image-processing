# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
Developed By:Marinto Richee J
Register Number:212220230031  
import cv2
import numpy as np
import matplotlib.pyplot as plt
org_img=cv2.imread("image.jpeg")
org_img=cv2.cvtColor(org_img,cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(org_img)
row,col,dim=org_img.shape

i)Image Translation
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))
plt.axis("off")
plt.imshow(Translated_image)

ii) Image Scaling
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)

iii)Image Shearing
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image)

iv)Image Reflection
Reflection_matrix_col=np.float32([[-1,0,col],[0,1,0],[0,0,1]])
Reflected_image_col=cv2.warpPerspective(org_img,Reflection_matrix_col,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_col)

Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]])
Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_row)

v)Image Rotation
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)

vi)Image Cropping
cropped_image=org_img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)

```
## Output:
### i)Image Translation
![image](https://user-images.githubusercontent.com/65499285/164649694-2fcb2003-c2fb-491b-a467-99cb90807dee.png)
<br>
<br>

### ii) Image Scaling
![image](https://user-images.githubusercontent.com/65499285/164649789-b4567984-0684-4e79-a55d-7fc2d03873d3.png)
<br>
<br>


### iii)Image Shearing
![image](https://user-images.githubusercontent.com/65499285/164649845-8ede293b-0a7f-4841-b3bd-c372c53f05e1.png)
<br>
<br>


### iv)Image Reflection
![image](https://user-images.githubusercontent.com/65499285/164649888-d86d01d7-84a8-440e-b200-d0b51b7c52da.png)
<br>
![image](https://user-images.githubusercontent.com/65499285/164649921-80058a23-9675-4219-b628-9a22a11b62fc.png)

<br>

### v)Image Rotation
![image](https://user-images.githubusercontent.com/65499285/164649987-c996d927-a3f3-4132-ad11-8f08a8a4dfb3.png)
<br>
<br>



### vi)Image Cropping
![image](https://user-images.githubusercontent.com/65499285/164650039-1d66fa6a-05a1-4fe9-b7a6-e0a6a50cba99.png)
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
