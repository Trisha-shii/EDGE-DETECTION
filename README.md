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

### PROGRAM :

Developed by : TRISHA PRIYADARSHNI PARIDA
Register Number : 212224230293
```
#Original:
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread(r"C:\Users\Trisha Priyadarshni\Downloads\Tigress.jpg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
SOBEL EDGE DETECTOR
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL 

![Screenshot 2025-04-28 132153](https://github.com/user-attachments/assets/520c0d95-8ca0-4cbc-9705-b68bda4dd9e5)

### SOBEL EDGE DETECTOR

![Screenshot 2025-04-28 132158](https://github.com/user-attachments/assets/058b2484-8165-483e-9406-df4939fd5273)

### LAPLACIAN EDGE DETECTOR
![Screenshot 2025-04-28 132204](https://github.com/user-attachments/assets/8b87eb66-5c48-48dc-999f-c0a0362b29c7)



### CANNY EDGE DETECTOR

![Screenshot 2025-04-28 132209](https://github.com/user-attachments/assets/fb4319dd-dd9e-48ea-b082-4eaa4912f145)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
