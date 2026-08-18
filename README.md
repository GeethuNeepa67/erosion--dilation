# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:
Create a blank image using NumPy.

## Step 3:
Insert text onto the image using OpenCV's text drawing function.

## Step 4:
Display the original image.

## Step 5:
Create a structuring element (kernel) of suitable size.

## Step 6: Image Erosion
Apply the erosion operation using the created kernel.
Remove pixels from the boundaries of foreground objects.
Display the eroded image.
## Step 7: Image Dilation
Apply the dilation operation using the same kernel.
Add pixels to the boundaries of foreground objects.
Display the dilated image.
## Step 8:
Compare the original, eroded, and dilated images.

 Name: GEETHUNEEPA TK
 Register no: 212225220033
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((300, 600), dtype=np.uint8)

cv2.putText(
    image,
    "EROSION AND DILATION",
    (50, 160),
    cv2.FONT_HERSHEY_SIMPLEX,
    1.2,
    255,
    3
)

kernel = np.ones((5, 5), np.uint8)

eroded = cv2.erode(image, kernel, iterations=1)

dilated = cv2.dilate(image, kernel, iterations=1)

plt.figure(figsize=(8, 4))
plt.imshow(image, cmap="gray")
plt.title("Input Image")
plt.axis("off")
plt.show()

plt.figure(figsize=(8, 4))
plt.imshow(eroded, cmap="gray")
plt.title("Eroded Image")
plt.axis("off")
plt.show()

plt.figure(figsize=(8, 4))
plt.imshow(dilated, cmap="gray")
plt.title("Dilated Image")
plt.axis("off")
plt.show()

```
## Output:

### Display the input Image
<br>
<br>
<br>
<img width="738" height="341" alt="image" src="https://github.com/user-attachments/assets/d8cefa7c-bbf4-4be3-bf71-38f2075a85f0" />

<br>
<br>
<br>

### Display the Eroded Image
<br>
<br>
<br>
<img width="682" height="325" alt="image" src="https://github.com/user-attachments/assets/76e57345-efc6-4090-a0d5-886b981ddd78" />

<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<br>
<img width="606" height="316" alt="image" src="https://github.com/user-attachments/assets/8626a512-e7c2-4679-a2ad-b70d1ec71b8f" />

<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
