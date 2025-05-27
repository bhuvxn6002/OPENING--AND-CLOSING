# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

## Program:
### Name: Bhuvaneshwaran H
### Register Number: 212223240018

``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt

def load_img():
    blank_img = np.zeros((300,700), dtype=np.uint8)
    front = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='RAKSHI', org=(50,200), fontFace=front, 
                fontScale=5, color=(255, 255, 255), thickness=25, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img,title="Original Image"):
    fig=plt.figure(figsize=(10,8))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    ax.set_title(title, fontsize=16)
    plt.show()

img = load_img()
display_img(img)
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (12,12))

image=load_img()
opening_img = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
display_img(opening_img,"Opening Image")

image=load_img()
closing_img = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
display_img(closing_img,"Closing Image")

```
## Output:

### Display the input Image

![download](https://github.com/user-attachments/assets/62afd4b6-1081-4eca-bffc-01fbb45220bf)

### Display the result of Opening

![download](https://github.com/user-attachments/assets/937ca35c-6c80-43de-b5df-88f622811712)

### Display the result of Closing

![download](https://github.com/user-attachments/assets/8a061f5d-7aaf-4907-ad91-c9fb006d1962)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
