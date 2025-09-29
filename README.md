# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1: 
Import the required libraries

### Step2
Read the image and convert from BGR to RGB

### Step3
Apply the required filters separately 

### Step4
Plot the original and filtered images using matplotlib.pyplot

### Step5
End of program

## Program:
### Developed By   : D VERGIN JNEIFER
### Register Number: 212223240174
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("/content/tree.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()


```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.

```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
<img width="930" height="448" alt="image" src="https://github.com/user-attachments/assets/a62fa604-9eb7-4a3e-8b00-5ff74f131929" />


ii)Using Weighted Averaging Filter
<img width="577" height="519" alt="image" src="https://github.com/user-attachments/assets/145a836a-dc56-46bf-ad93-ed369a011c91" />


iii)Using Gaussian Filter
<img width="511" height="522" alt="image" src="https://github.com/user-attachments/assets/a3654445-c483-41ea-81eb-5921c4a8d81e" />


iv) Using Median Filter


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
<img width="525" height="509" alt="image" src="https://github.com/user-attachments/assets/f50c556d-d635-4e0b-a582-06d1311b2c32" />


ii) Using Laplacian Operator
<img width="510" height="512" alt="image" src="https://github.com/user-attachments/assets/407495e6-15f4-48e8-86d0-231ecd518905" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
