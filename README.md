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
## Developed by: 
## Register number: 
## PROGRAM
```

import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'L yagnesh' ,(5,70),font,4,(255),2,cv2.LINE_AA)


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


![WhatsApp Image 2025-05-21 at 15 26 46_5e243332](https://github.com/user-attachments/assets/72a2c2f4-d00b-4d1c-aa23-4c5e7ebe929d)


### Display the Eroded Image
![WhatsApp Image 2025-05-21 at 15 26 54_f98b605a](https://github.com/user-attachments/assets/aa726ef6-c478-415d-b8f9-e7b8120936c8)



### Display the Dilated Image

![WhatsApp Image 2025-05-21 at 15 27 07_abe1863c](https://github.com/user-attachments/assets/9c7e8725-32f7-4e67-99e4-8ae1ffa53c48)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
