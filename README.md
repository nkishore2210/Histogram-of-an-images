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
```
# Developed By: KISHORE N
# Register Number: 212222240049
```
```python
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('d naa.png')
```
```python
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
### OUTPUT:
![Screenshot 2024-10-03 154554](https://github.com/user-attachments/assets/d45a4695-851c-494a-a313-acbed98d53bc)

```python
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
### OUTPUT:
![Screenshot 2024-10-03 154732](https://github.com/user-attachments/assets/fae3959b-957d-4c4b-8e49-1717ed335d0a)

```python
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
### OUTPUT:
![Screenshot 2024-10-03 154836](https://github.com/user-attachments/assets/1c370e09-0bdb-4f28-9476-b82fa09d9c09)

```python
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
````
### OUTPUT:
![Screenshot 2024-10-03 154846](https://github.com/user-attachments/assets/137f838a-d1ac-4487-ac1d-bc732ee9e7f6)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
