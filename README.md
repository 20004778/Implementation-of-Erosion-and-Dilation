# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode and Dilate the image.

### Step5:
End Program.

## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
img1=np.zeros((200,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the Text using cv2.putText
cv2.putText(img1,' STARK ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')

```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/75236145/169695788-aba69df4-6ca3-4351-8660-00982a9c41fd.png)

### Display the Eroded Image
![image](https://user-images.githubusercontent.com/75236145/169695806-da54ae26-3b7b-4352-b8bf-81c798386e95.png)

### Display the Dilated Image
![image](https://user-images.githubusercontent.com/75236145/169695819-e8d0d1df-2d91-4ef8-b05e-f8ccb595f8c6.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
