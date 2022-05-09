# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the necessary modules.

### Step2
 * Average filter

```python3 
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)

```

### Step3
* Weighted average filter
```python3

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)

```
### Step4
* Gaussian Blur
```python3


gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)

```

### Step5
* Median filter
```python3

median=cv2.medianBlur(image2,13)


``` 

## Program:
### Developed By   : PRIYADARSHINI R
### Register Number: 212220230038

```python 3
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("con.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)

```


### 1. Smoothing Filters

i) Using Averaging Filter
```Python

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
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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

iv) Using Median Filter
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python


kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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


i) Using Averaging Filter

![image](https://user-images.githubusercontent.com/81132849/167433168-ff878e55-1cf1-42e9-992b-fe94badc7e7f.png)

ii) Using Weighted Averaging Filter

![image](https://user-images.githubusercontent.com/81132849/167433406-f0c3659f-23ac-441a-a13f-e0be8271412e.png)

iii) Using Weighted Averaging Filter

![image](https://user-images.githubusercontent.com/81132849/167433510-2935108b-06a6-4944-b320-34a518e4b19b.png)

iv) Using Median Filter

![image](https://user-images.githubusercontent.com/81132849/167433727-21385531-9b4a-420f-8230-f639bb387c66.png)


### 2. Sharpening Filters


i) Using Laplacian Kernal

![image](https://user-images.githubusercontent.com/81132849/167433998-58dcf7bc-a4a0-4bfe-a5b9-f860df3f4b8d.png)

ii) Using Laplacian Operator

![image](https://user-images.githubusercontent.com/81132849/167434116-0f9f9722-84c7-48c7-8f3b-a08242119d55.png)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
