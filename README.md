# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step 1:
Import the necessary modules.

## Step 2:
Perform edge detection on a image.

Sobel
Laplacian
Canny
## Step 3:
Display the original images with edge detected images.




 
## Program:

``` 
import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
from cv2 import COLOR_BGR2GRAY
image=cv2.imread("dog.png")
gray=cv2.cvtColor(image,COLOR_BGR2GRAY)
img = cv2.GaussianBlur(gray,(3,3),0)
sobelx = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)

plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(img,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])
plt.subplot(2,2,2)
plt.imshow(sobelx)
plt.title('sobelx')
plt.xticks([]), plt.yticks([])
plt.subplot(2,2,3)
plt.imshow(sobely)
plt.title('sobely')
plt.xticks([]), plt.yticks([])
plt.subplot(2,2,4)
plt.imshow(sobelxy)
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()

laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.imshow(laplacian)
plt.title('laplacian')

plt.show()

canny_edges = cv2.Canny(img, 120, 150)
plt.imshow(canny_edges)
plt.title('canny_edges')

plt.show()

```
## Output:
### SOBEL EDGE DETECTOR
![image](https://user-images.githubusercontent.com/94165326/234520197-ca4c8bde-2989-4d43-8999-9533d2ca4101.png)


### LAPLACIAN EDGE DETECTOR
![image](https://user-images.githubusercontent.com/94165326/234520622-3d6c405c-b7a4-4881-bb6e-3b5218e26580.png)


### CANNY EDGE DETECTOR
![image](https://user-images.githubusercontent.com/94165326/234520795-8202f64d-279c-49c5-a038-230f8843e78b.png)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
