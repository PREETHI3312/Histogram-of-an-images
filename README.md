# Histogram-of-an-images
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
```python
# Developed By: PREETHI A K
# Register Number: 212223230156

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('boy.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])



plt.subplot(2, 2, 4)
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()
```
## Output:
### Input Grayscale Image and Color Image

<img width="503" height="502" alt="image" src="https://github.com/user-attachments/assets/15f26fd8-1dc6-4b6c-9c28-ea8bae7d1dab" />


<img width="469" height="424" alt="image" src="https://github.com/user-attachments/assets/91422e3e-a4cf-4ff7-8bf2-ead16c7d43f3" />


### Histogram of Grayscale Image and any channel of Color Image

<img width="427" height="416" alt="image" src="https://github.com/user-attachments/assets/1effb045-165c-4cda-bf3a-7c7a09154720" />
<img width="614" height="432" alt="image" src="https://github.com/user-attachments/assets/408dc3ed-e3a2-49ad-bc7c-34e9d7d0eae1" />

### Histogram Equalization of Grayscale Image.

<img width="640" height="443" alt="image" src="https://github.com/user-attachments/assets/966dc33b-afd1-4998-849d-bb3187d69f92" />
<img width="418" height="415" alt="image" src="https://github.com/user-attachments/assets/00c7e7d9-a4d1-4dd2-8b0e-39f6de60d534" />

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
