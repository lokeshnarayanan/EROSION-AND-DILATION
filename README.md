# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary packages
<br>


### Step2:
Create a empty window and add text in it
<br>

### Step3:
create a structuring element
<br>

### Step4:
Do the operation
<br>

### Step5:
Show the Output Image
<br>

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image= np.zeros((100,600),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,'LOKESH N',(5,70), font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Original",image)

# Create the structuring element
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
erodeImage = cv2.erode(image,kernel1)
cv2.imshow("Erode Image",erodeImage)

# Dilate the image
dilationImage = cv2.dilate(image,kernel1)
cv2.imshow("Dilated Image",dilationImage)

cv2.waitKey(0)
cv2.destoryAllWindows




```
## Output:

### Display the input Image
![Screenshot from 2023-10-10 14-46-58](https://github.com/lokeshnarayanan/EROSION-AND-DILATION/assets/119393019/d9df64d4-20dc-4846-9545-644c06536502)


### Display the Eroded Image

![Screenshot from 2023-10-10 14-47-13](https://github.com/lokeshnarayanan/EROSION-AND-DILATION/assets/119393019/492c6ad3-5731-4ad6-a08b-1e53a69846b9)

### Display the Dilated Image

![Screenshot from 2023-10-10 14-47-29](https://github.com/lokeshnarayanan/EROSION-AND-DILATION/assets/119393019/1e1c72a9-e005-440c-96a9-2bb1f8913783)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
