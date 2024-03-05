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
 Developed By: Sivabalan S  
 Register Number: 212222240100
```

### Input Grayscale Image and Color Image :
```py
import cv2
import matplotlib.pyplot as plt
from google.colab.patches import cv2_imshow

# Load the images
gray_image = cv2.imread("grayscale.jpg", 0)
color_image = cv2.imread("shitzu.jpg")

# Display the images
cv2_imshow(gray_image)
cv2_imshow(color_image)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image :

```py
import numpy as np
import cv2
Gray_image = cv2.imread("grayscale.jpg")
Color_image = cv2.imread("shitzu.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

### Histogram Equalization of Grayscale Image :
```py
import cv2
gray_image = cv2.imread("grayscale.jpg",0)
cv2_imshow(gray_image)
equ = cv2.equalizeHist(gray_image)
cv2_imshow(equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-06 000537](https://github.com/sivabalan28/Histogram-of-an-images/assets/113497347/b9a37ada-308e-4348-8410-3edc9d191bdf)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-06 000702](https://github.com/sivabalan28/Histogram-of-an-images/assets/113497347/d5495fca-4216-4bb7-887b-1f95b96ecf27)
![Screenshot 2024-03-06 000720](https://github.com/sivabalan28/Histogram-of-an-images/assets/113497347/2662b1b8-d177-474b-973f-e79dc9adbde9)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-06 002642](https://github.com/sivabalan28/Histogram-of-an-images/assets/113497347/a61a972a-971f-42fb-ba34-9fcdd8a24a34)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
