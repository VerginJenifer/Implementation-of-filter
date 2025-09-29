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

<img width="918" height="446" alt="image" src="https://github.com/user-attachments/assets/e6636e19-d927-45d2-b523-375d21d183c1" />


ii)Using Weighted Averaging Filter

<img width="492" height="523" alt="image" src="https://github.com/user-attachments/assets/8abd2a40-23e4-4638-8f3c-08abb5a5cb14" />



iii)Using Gaussian Filter

<img width="514" height="516" alt="image" src="https://github.com/user-attachments/assets/a0e64bad-913d-4577-bfe6-099b566599d2" />

iv) Using Median Filter

<img width="496" height="523" alt="image" src="https://github.com/user-attachments/assets/f0438f17-94de-4cd8-b891-0710ed28f2f0" />


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

<img width="499" height="515" alt="image" src="https://github.com/user-attachments/assets/dc4a82b1-d9dc-4ef5-bada-98be8222aca9" />


ii) Using Laplacian Operator
<img width="531" height="492" alt="image" src="https://github.com/user-attachments/assets/66b0f21f-478e-442d-8473-141cae64a09c" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
