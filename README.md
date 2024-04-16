# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary pacakages
<br>

### Step2:
Create the text using cv2.putText
<br>

### Step3:
Create the structuring element
<br>

### Step4:
Erode the image
<br>

### Step5:
Dilate the Image
<br>

 
## Program:

```python
DEVELOPED BY : RAJA R
REGISTER NO : 21222210041

### Import the necessary packages:

import io
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


### Create the Text using cv2.putText:
```python
img = np.zeros((100,400), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,"eldorado",(5,70),font,2,(255,255,255),5,cv2.LINE_AA)
```


### Create the structuring element:
```python
kernel = np.ones((5,5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


### Erode the image:
```python
img_erode = cv2.erode(img,kernel1)
```



### Dilate the image:
```python
img_dilate = cv2.dilate(img,kernel1)
```

### Display Result:
```python
plt.imshow(img, cmap = 'gray')
plt.axis("off")

plt.imshow(img_erode, cmap = 'gray')
plt.axis("off")

plt.imshow(img_dilate, cmap = 'gray')
plt.axis("off")
```
## Output:

### Display the input Image:

![Screenshot 2024-04-16 210302](https://github.com/Raja8334/erosion-dilation/assets/120719634/6926261b-74ae-426b-b0e5-e61a314bee18)


### Display the Eroded Image:

![Screenshot 2024-04-16 210148](https://github.com/Raja8334/erosion-dilation/assets/120719634/0335b69a-736b-4634-a09d-2d09ff922dd0)


### Display the Dilated Image:

![Screenshot 2024-04-16 210201](https://github.com/Raja8334/erosion-dilation/assets/120719634/75992d0b-0c15-410f-8119-4946e4d94b2c)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
