# Edge-Detection...

## Aim:

To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:

Anaconda - Python 3.7 .

## Algorithm:

### Step 1:

Import the required packages for further process.

### Step 2:

Read the image and convert the bgr image to gray scale image.

### Step 3:

Use any filters for smoothing the image to reduse the noise.

### Step 4:

Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step 5:

Display the filtered image using plot and imshow.
 
 
## Program:
Developed by: Gunaseelan G
Register no : 212221230031

```python 

# Import the packages and load the image, Convert to grayscale and remove noise:

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("alaskan.jpg")
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

```

```python

# SOBEL EDGE DETECTOR:

# SOBEL-X:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel-X")
plt.xticks([])
plt.yticks([])
plt.show()

```

```python

# SOBEL-Y:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()

```

```python

# SOBEL-XY:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelxy=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel-XY")
plt.xticks([])
plt.yticks([])
plt.show()

```

```python

# LAPLACIAN EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Blues')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='Blues')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()

```

```python 

# CANNY EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()

```


## Output:

### INPUT IMAGE:

![m5](https://user-images.githubusercontent.com/93427255/233850911-7c6c4712-b165-4c5a-a5a7-ef3cb31b0bd4.jpg)


### SOBEL EDGE DETECTOR:

### SOBEL-X:
![out2](https://user-images.githubusercontent.com/93427255/233850917-f02c4b3c-9aac-46c0-a80b-b93321e361ca.png)


### SOBEL-Y:

![out3](https://user-images.githubusercontent.com/93427255/233850929-892f9819-0434-4d77-aea5-237dbea8cc88.png)


### SOBEL-XY:

![out4](https://user-images.githubusercontent.com/93427255/233850936-46aed98c-a91b-4870-a64f-fe12efe1ab1b.png)


### LAPLACIAN EDGE DETECTOR:

![out5](https://user-images.githubusercontent.com/93427255/233850945-58765493-8ebb-4f93-8543-6a5ea05c393f.png)


### CANNY EDGE DETECTOR:

![out6](https://user-images.githubusercontent.com/93427255/233850956-1330e35e-592f-455c-ae62-d52b3a431ff6.png)


## Result:

Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.


