# EXP - 6 EDGE-DETECTION
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
### PROGRAM:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('EXP_6.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

## Output:
### ORIGINAL IMAGE:
<img width="506" height="459" alt="image" src="https://github.com/user-attachments/assets/ed4e1d40-9c3e-4888-8879-d0b434743cb8" />

### SOBEL EDGE DETECTOR:


<img width="423" height="434" alt="image" src="https://github.com/user-attachments/assets/c1ca338a-fa36-4b90-adf1-909425e6d7be" />


### LAPLACIAN EDGE DETECTOR:


<img width="406" height="442" alt="image" src="https://github.com/user-attachments/assets/25622cb3-3072-4835-b959-d68ab2362294" />




### CANNY EDGE DETECTOR:

<img width="458" height="446" alt="image" src="https://github.com/user-attachments/assets/7679638b-5d56-43f7-baff-b5453f34e5bc" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
