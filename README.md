# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Program:
## Developed by: T Ajay
## Register number: 212223230007
## PROGRAM
```

import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'T Ajay' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')
```

## Output:

### Display the input Image

![WhatsApp Image 2025-05-21 at 15 26 46_1296e48e](https://github.com/user-attachments/assets/12f9ee02-e7c7-448f-b4d2-08702b5b13b4)


### Display the Eroded Image

![WhatsApp Image 2025-05-21 at 15 26 54_ebfc2ab5](https://github.com/user-attachments/assets/43f30731-d95e-424c-a515-ebd5aad91b32)


### Display the Dilated Image

![WhatsApp Image 2025-05-21 at 15 27 07_67f455bc](https://github.com/user-attachments/assets/325fb64a-eea7-4357-8f7d-d1398dcaf18a)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
