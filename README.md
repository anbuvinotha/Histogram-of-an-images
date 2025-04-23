# EX 03 Histogram-of-an-images
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
# Developed By: ANBU VINOTHA.S
# Register Number: 212223230015

```
## Output:

### Input Grayscale Image and Color Image
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("vijay.png")
color_image = cv2.imread("ajith.png",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/swedha333/Histogram-of-an-images/assets/121165979/82f3ebc9-e4da-47c9-a226-2d6f5137d0da)

![image](https://github.com/swedha333/Histogram-of-an-images/assets/121165979/10ae6209-3c88-4dd2-ad46-8b47c12be03d)


### Histogram of Grayscale Image and any channel of Color Image
```python
import numpy as np
import cv2
Gray_image = cv2.imread("vijay.png")
Color_image = cv2.imread("ajith.png")
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
![image](https://github.com/swedha333/Histogram-of-an-images/assets/121165979/b115339e-d983-40be-9372-306a2f6c20aa)

## Grayscale Image

![image](https://github.com/Leann4468/Histogram-of-an-images/assets/121165979/7f0dd33d-fbf9-4afa-9423-fd7435a4fbf5)

![image](https://github.com/Leann4468/Histogram-of-an-images/assets/121165979/06f6e521-2354-48df-b6ee-71650e8e1160)

## Colour Image
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
![image](https://github.com/Leann4468/Histogram-of-an-images/assets/121165979/6eaa5904-c2ea-4907-842c-36a59092c15f)

![image](https://github.com/Leann4468/Histogram-of-an-images/assets/121165979/3f080261-60c2-49c2-b0ea-4fb794a388f3)

![image](https://github.com/Leann4468/Histogram-of-an-images/assets/121165979/e58ee811-2e85-4597-b68a-ff8658d79c14)

### Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("vijay.png",0)
cv2.imshow('Gray Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Leann4468/Histogram-of-an-images/assets/121165979/8e3733b4-03ec-4d81-aaaf-b883c8a5d706)

![image](https://github.com/Leann4468/Histogram-of-an-images/assets/121165979/34a4d171-1bf2-44dd-bb95-77744638b693)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
