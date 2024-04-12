# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary packages
### Step2:
Create an empty window and add text to it

### Step3:
create a structuring element

### Step4:
Do the operation

### Step5:
Show the output image
 
## Program:

Name:ONTEDDU SIRISHA 

Ref.No:212222230103
``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt

input_image_path = 'sirisha.jpg'
color_image = cv2.imread(input_image_path)
gray_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2GRAY)
edges = cv2.Canny(gray_image, 100, 200)

kernel_size = 5  # Define the kernel size
kernel = np.ones((kernel_size, kernel_size), np.uint8)  # Corrected dtype

erosion = cv2.erode(edges, kernel, iterations=1)
dilation = cv2.dilate(edges, kernel, iterations=1)

plt.figure(figsize=(15, 10))
plt.subplot(2, 3, 1)
plt.imshow(cv2.cvtColor(color_image, cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')

plt.subplot(2, 3, 2)
plt.imshow(gray_image, cmap='gray')  # Corrected variable name
plt.title('Black and White Image')
plt.axis('on')

plt.subplot(2, 3, 3)
plt.imshow(edges, cmap='gray')
plt.title('Edge Segmentation')
plt.axis('on')

plt.subplot(2, 3, 4)
plt.imshow(erosion, cmap='gray')
plt.title('Erosion')
plt.axis('on')

plt.subplot(2, 3, 5)
plt.imshow(dilation, cmap='gray')  # Corrected variable name
plt.title('Dilation')
plt.axis('on')

plt.show()

```
## Output:

### Display the input Image
![image](https://github.com/22003264/erosion-dilation/assets/119389139/049b4dec-82d7-400e-918b-6b0f3fe51dd7)


### Display the Eroded Image

![image](https://github.com/22003264/erosion-dilation/assets/119389139/5deddacb-19f9-4903-ab4f-9324794e0ec7)

### Display the Dilated Image
![image](https://github.com/22003264/erosion-dilation/assets/119389139/4020473d-3b0d-4deb-bdee-3029d6a5ba20)
### Full output
![image](https://github.com/22003264/erosion-dilation/assets/119389139/da147c7f-b005-457b-aceb-20bf48389970)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
