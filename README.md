# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.

## Program:
```python
# Developed By: Dineshkumar S
# Register Number: 212220230012
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
bw = cv2.imread("flower bw.jpg")
img = cv2.imread("feather.jpg")
plt.imshow(bw)
plt.show()
plt.imshow(img)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
hist = cv2.calcHist([bw],[0],None,[256],[0,256])
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image
Color_image=cv2.imread('feather.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image. 
Gray_image=cv2.imread('flower bw.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot (28)](https://user-images.githubusercontent.com/75234807/165540473-597284fc-b50f-4c91-872d-a991ea4afc4f.png)

### Histogram of Grayscale Image and any channel of Color Image
![Screenshot (29)](https://user-images.githubusercontent.com/75234807/165540578-9928fe07-7227-4ca0-9ee0-0e9ab839110b.png)

### Histogram Equalization of Grayscale Image
![Screenshot (30)](https://user-images.githubusercontent.com/75234807/165540699-3e6198c3-86cd-4b0f-ab04-c26ec461c47d.png)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
