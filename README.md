# Histogram Equalization Using OpenCV (Grayscale & Color Images)

### Developed By:
### Name: KISHORE J
### Register No : 212225240072
---

## Aim

To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

The program performs the following operations:

- Read and display a grayscale image  
- Plot histogram of the grayscale image  
- Apply histogram equalization on grayscale image  
- Read and display a color image  
- Plot histogram of B, G, R channels  
- Convert image to HSV color space  
- Apply histogram equalization on the Value (V) channel  
- Convert the enhanced image back to BGR format  
- Display original and enhanced images with histograms  

---

## Software Used

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (`cv2`)  
- NumPy  
- Matplotlib  

---

## Algorithm

```
1)Import Required Libraries
->Import OpenCV (cv2) and Matplotlib (pyplot) for image processing and visualization.
2)Read the Input Image
->Load the color image from the file using cv2.imread().
3)Convert to Grayscale
->Convert the loaded image into grayscale using cv2.cvtColor().
4)Compute and Display Original Histogram
->Display the grayscale image.
->Calculate its histogram using cv2.calcHist() and plot it.
5)Apply Histogram Equalization
->Enhance the contrast of the grayscale image using cv2.equalizeHist().
6)Compute and Display Equalized Results
->Display the equalized image.
->Calculate and plot the histogram of the equalized image.
```

## Program

### Developed By:
### Name: KISHORE J
### Register No: 212225240072

---
## STEP-1
```
import cv2
from matplotlib import pyplot as plt
```
## STEP-2
```
# Load the color image
image = cv2.imread('myimg.jpeg')
```
## STEP-3
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
## STEP-4
```
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
## STEP-5
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
## STEP-6
```
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
## STEP-7
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
## STEP-8
```
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
## STEP-9
```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
```
## STEP-10
```
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```

##  Output
### Grayscale Histogram Equalization
- Original grayscale image is displayed
<img width="237" height="397" alt="image" src="https://github.com/user-attachments/assets/8d36b518-115b-4a5c-9d90-2e61a969f2a5" />


- Histogram of original grayscale image is plotted
<img width="582" height="436" alt="image" src="https://github.com/user-attachments/assets/d27e4036-7113-4259-97fb-b6d66d45c026" />



- Enhanced image after histogram equalization is displayed
<img width="252" height="396" alt="image" src="https://github.com/user-attachments/assets/0d63eac2-b788-4a2d-88f3-e5c26414a623" />




- Histogram of enhanced grayscale image shows improved contrast  
 <img width="587" height="432" alt="image" src="https://github.com/user-attachments/assets/a969afdc-2b2a-4c56-9cf2-dc29b3be1546" />




---

## Result

Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.
