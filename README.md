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
### Developed By: MUGIL MURUGAN
### Register Number: 212223230127

### (i) Input Grayscale Image and Color Image
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
### (ii) Histogram of Grayscale Image and any channel of Color Image
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


### (iii) Colour Image
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
### (iv) Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("vijay.png",0)
cv2.imshow('Gray Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### (i) Input Grayscale Image and Color Image
![Screenshot 2025-04-24 084516](https://github.com/user-attachments/assets/ccfa872e-b933-4e4c-8b75-a3d1589bf74f)
### (ii) Histogram of Grayscale Image and any channel of Color Image
### Grayscale Image
![Screenshot 2025-04-24 084851](https://github.com/user-attachments/assets/ac347c80-b144-4dc4-851c-230cb704df84)


![Screenshot 2025-04-24 084914](https://github.com/user-attachments/assets/e57d8725-3265-4df4-a408-23e6af74e1ac)

### (iii) Colour Image




![Screenshot 2025-04-24 084922](https://github.com/user-attachments/assets/842f71e0-31dc-4a01-b085-72efc7309c8a)



![Screenshot 2025-04-24 084930](https://github.com/user-attachments/assets/388be77b-1442-42ee-97e5-a03ee105d792)
### (iv) Histogram Equalization of Grayscale Image.

![Screenshot 2025-04-24 084814](https://github.com/user-attachments/assets/d3766318-85fc-4125-8134-a5e85f71ee95)






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
