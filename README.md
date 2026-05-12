# Implementation-of-Filters

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br> Convert the image from BGR to RGB.
</br> 

### Step3
</br>Apply the required filters for the image separately. </br> 

### Step4
</br> Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>End the program.
</br> 

## Program:
### Developed By   :KATHI HASINI
### Register Number:212224240074
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python


import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Imgage2.jpg")
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
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
</br>
<img width="960" height="768" alt="image" src="https://github.com/user-attachments/assets/80b29d72-cc04-449e-8ca9-257dc1ce19eb" />

</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br>
<img width="668" height="517" alt="image" src="https://github.com/user-attachments/assets/d43f5bce-1f19-479d-949a-5ff82b39cb5d" />

</br>
</br>

iii)Using Gaussian Filter
</br>
<img width="654" height="516" alt="image" src="https://github.com/user-attachments/assets/fd1c40cc-7d21-405e-8ce1-433405489190" />

</br>
</br>
</br>

iv) Using Median Filter
</br>
</br>
</br>
<img width="961" height="764" alt="image" src="https://github.com/user-attachments/assets/39d9a10a-f49b-4646-8eca-1c52ab39a71d" />

</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
<img width="685" height="519" alt="image" src="https://github.com/user-attachments/assets/ef43aee9-b170-4378-ac88-58b4ba8b5cb1" />

</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
<img width="652" height="508" alt="image" src="https://github.com/user-attachments/assets/54934dcb-13e7-4718-91ca-400e4752d798" />

</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
