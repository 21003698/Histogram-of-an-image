# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
<br>
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
<br>
Display the histograms with their respective images.

### Step4:
<br>
Equalize the grayscale image.

### Step5:
<br>
Display the grayscale image.

## Program:
```python
# Developed By:challa sandeep
# Register Number:212221240011
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
~~~
import cv2
import matplotlib.pyplot as plt
gray_image=cv2.imread('a.jpg')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
~~~




# Display the histogram of gray scale image and any one channel histogram from color image
~~~
import cv2
import matplotlib.pyplot as plt
color_image=cv2.imread('a1.jpg')
hist=cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('colorscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

~~~




# Write the code to perform histogram equalization of the image. 
~~~
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('k.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
~~~






```
## Output:
### Input Grayscale Image and Color Image
<br>
<br>
<br>
<br>
![pigeon 1](https://user-images.githubusercontent.com/93427522/166959296-f6906805-d998-4d84-b952-89dec8f975d3.png)





### Histogram of Grayscale Image and any channel of Color Image
<br>
<br>
<br>
<br>
![pigeon 2](https://user-images.githubusercontent.com/93427522/166959372-cee3354b-052d-4e2c-9567-78a282cd2c13.png)




### Histogram Equalization of Grayscale Image
<br>
<br>
<br>
<br>
![pigeon 4](https://user-images.githubusercontent.com/93427522/166959454-2ecf8c81-7eae-4caf-8283-a471c4f13c5a.png)
![pigeon 5](https://user-images.githubusercontent.com/93427522/166959478-59efff07-4faf-42eb-9917-9826f54a3c5f.png)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
