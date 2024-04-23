# EX-02   Image_Acqusition-_using_Web_Camera
## Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
## Step 1:
Import cv2 and capture the viedo using cv2.ViedoCapture(0).
<br>
## Step 2:
Write the capture image using cv2.imwrite("NewPicture.jpg",frame).
<br>
## Step 3:
Resize the image using cv2.resize(frame,(0,0),fx=0.5,fy=0.5).
<br>
## Step 4:
Display the image until the loop gets over.
<br>
## Step 5:
Rotate the image using cv2.rotate(smaller_frame,cv2.ROTATE_180)
<br>
## Program:
 Python
### Developed By: SRI SAI PRIYA.S
### Register No: 212222240103

<br>
<br>
<br>
<br>
<br>

## i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("clouds.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('cycle',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

## iii) Display the video by resizing the window
```import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('cycle',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('cycle',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
</br>
</br>

![image](https://github.com/SriSaiPriyaSenthilvel/Image_Acqusition-_using_Web_Camera/assets/119475702/01fb3153-18c4-4ba5-a101-0c03e2a6c887)

### ii) Display the video
</br>
</br>

![image](https://github.com/SriSaiPriyaSenthilvel/Image_Acqusition-_using_Web_Camera/assets/119475702/0571b043-5c0d-4a6c-84cb-c4a3190566c3)

### iii) Display the video by resizing the window
</br>
</br>

![WhatsApp Image 2024-02-28 at 08 04 12_e71510bb](https://github.com/SriSaiPriyaSenthilvel/Image_Acqusition-_using_Web_Camera/assets/119475702/af7b6e8a-74e8-4f63-9a2e-2d253feb1aa4)

### iv) Rotate and display the video
</br>
</br>

![image](https://github.com/SriSaiPriyaSenthilvel/Image_Acqusition-_using_Web_Camera/assets/119475702/fae2f3fa-18d9-4b28-9d63-f5860356c277)

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
