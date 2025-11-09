# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:

Load the necessary packages.

### Step2:

Read the Image and convert to grayscale.


### Step3:

Use Global thresholding to segment the image.

### Step4:

Use Adaptive thresholding to segment the image.

### Step5:

Use Otsu's method to segment the image and display the results.

## Program

### NAME : AANKARSH J
### REG.NO: 212223233001

# Load the necessary packages
```
import cv2
import matplotlib.pyplot as plt
```




# Read the Image and convert to grayscale
```
image=cv2.imread('flower.jpg')
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
# Original image
```
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

# Use Global thresholding to segment the image
```
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)
```



# Use Adaptive thresholding to segment the image
```
adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```



# Use Otsu's method to segment the image 
```
_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```



# Global Thresholding

```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
# Adaptive Thresholding
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
# Otsu's Method
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
# Show the plot
```
plt.tight_layout()
plt.show()
```
## Output

### Original Image

<img width="243" height="210" alt="download" src="https://github.com/user-attachments/assets/b82293c4-b5d2-4724-8f41-8a7c0e46b639" />


### Global Thresholding

<img width="243" height="210" alt="download" src="https://github.com/user-attachments/assets/8ed2e8ba-f2c0-4e65-9b45-4456241e3722" />


### Adaptive Thresholding

<img width="244" height="210" alt="download" src="https://github.com/user-attachments/assets/7a82a7ce-b58d-4558-9829-46cbf2bba977" />


### Optimum Global Thesholding using Otsu's Method

<img width="244" height="210" alt="download" src="https://github.com/user-attachments/assets/f22081d1-2b86-47ef-86d4-5dfdbbecbcd7" />


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
