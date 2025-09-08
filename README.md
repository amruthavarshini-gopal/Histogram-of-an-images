# Histogram-of-an-images
## Aim:
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
# Developed By: Amruthavarshini Gopal
# Register Number: 212223230013

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('pic.jpg')
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
<img width="359" height="522" alt="Screenshot 2025-09-08 105028" src="https://github.com/user-attachments/assets/4c46f070-d967-4aeb-8900-a5aca3d78356" />

<img width="359" height="522" alt="Screenshot 2025-09-08 105028" src="https://github.com/user-attachments/assets/fb69f5f9-8b4a-4074-9bd8-e6ffc017f765" />


### Histogram of Grayscale Image and any channel of Color Image
<img width="359" height="522" alt="Screenshot 2025-09-08 105028" src="https://github.com/user-attachments/assets/b8c94b24-3f3f-46e4-8f01-a37c37a98872" />

<img width="811" height="572" alt="Screenshot 2025-09-08 105156" src="https://github.com/user-attachments/assets/7376fe6e-c958-46fc-9174-5c6ec2c902b1" />


### Histogram Equalization of Grayscale Image.
<img width="334" height="529" alt="Screenshot 2025-09-08 105322" src="https://github.com/user-attachments/assets/6bba5b44-cac4-420d-822f-d0ebcdaa0bd6" />

<img width="809" height="559" alt="Screenshot 2025-09-08 105408" src="https://github.com/user-attachments/assets/df757797-c5ad-44c2-b532-fb85eadfaeec" />

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
