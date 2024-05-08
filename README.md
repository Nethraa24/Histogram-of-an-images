# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: J Nethraa
# Register Number: 212222100031
```
### Input Grayscale Image and Color Image
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("ajith.jpg")
color_image = cv2.imread("vijay.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image and any channel of Color Image
### Grayscale Image
```python
import numpy as np
import cv2
Gray_image = cv2.imread("ajith.jpg")
Color_image = cv2.imread("vijay.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```

### Color Image
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
### Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("ajith.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![3a](https://github.com/Nethraa24/Histogram-of-an-images/assets/121215786/f6d47cca-b418-4910-b96f-4b953232ecae)


## Histogram of Grayscale Image and any channel of Color Image
### Grayscale Image
![3b1](https://github.com/Nethraa24/Histogram-of-an-images/assets/121215786/214a41b5-a5df-4ea4-9b52-8714e13353f2)

![3b2](https://github.com/Nethraa24/Histogram-of-an-images/assets/121215786/71d756e5-1cf2-41b4-b881-192c321374ce)


### Color Image
![3c1](https://github.com/Nethraa24/Histogram-of-an-images/assets/121215786/7702c233-8a75-4837-890f-5a4ab601c763)

![3c2](https://github.com/Nethraa24/Histogram-of-an-images/assets/121215786/2d3c4e93-df96-485b-8cf3-e6157c1de4f8)

### Histogram Equalization of Grayscale Image.
![3d](https://github.com/Nethraa24/Histogram-of-an-images/assets/121215786/96dbfad7-cefc-4fdf-8998-99f6bb26d0e9)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
