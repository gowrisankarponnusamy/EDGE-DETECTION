# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('image.jpg')  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)
sobel_combined = cv2.magnitude(sobel_x, sobel_y)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.show()
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.show()
```
## Output:
### ORIGINAL
![image](https://github.com/user-attachments/assets/0345b05a-84cd-4600-9600-9ee90c5343ab)

### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/c9c82e39-514b-4917-9fb9-8d2497dfbb04)

### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/bc320315-16e1-462a-a78e-8a3a2f43dfc1)

### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/a21317da-bdb5-4eae-8dd0-42e92aca475b)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
