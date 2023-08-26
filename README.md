# Image-Acquisition-from-Web-Cameraa
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import cv2 and capture the viedo using cv2.ViedoCapture(0).
<br>

### Step 2:
Write the capture image using cv2.imwrite("NewPicture.jpg",frame).
<br>

### Step 3:
Resize the image using cv2.resize(frame,(0,0),fx=0.5,fy=0.5).
<br>

### Step 4:
Display the image until the loop gets over.
<br>

### Step 5:
Rotate the image using cv2.rotate(smaller_frame,cv2.ROTATE_180).
<br>

## Program:
``` Python
### Developed By:M.Chandru
### Register No:212222230026
```
## i) Write the frame as JPG file
```python
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("dimp.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```

## ii) Display the video
```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('212222230026-MChandru',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

## iii) Display the video by resizing the window
```python
import numpy as np
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
    cv2.imshow('212222230026-MChandru',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

## iv) Rotate and display the video
```python
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
    cv2.imshow('212222230026-MChandru',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

## Output

### i) Write the frame as JPG image
![di](https://github.com/chandrumathiyazhagan/Image-Acquisition-from-Web-Cameraa/assets/119393023/ef0d3767-56f7-4467-bd17-eaf227c15845)

</br>
</br>


### ii) Display the video


![Screenshot from 2023-08-26 21-25-34](https://github.com/chandrumathiyazhagan/Image-Acquisition-from-Web-Cameraa/assets/119393023/9460a4d3-357e-402b-a5e9-9c6e00276024)

</br>
</br>


### iii) Display the video by resizing the window

![Screenshot from 2023-08-26 21-28-35](https://github.com/chandrumathiyazhagan/Image-Acquisition-from-Web-Cameraa/assets/119393023/f36a22c6-5d44-419e-b779-00101f4f5ba6)

</br>
</br>



### iv) Rotate and display the video

![Screenshot from 2023-08-26 21-31-01](https://github.com/chandrumathiyazhagan/Image-Acquisition-from-Web-Cameraa/assets/119393023/1aa6a207-3954-465b-a73b-b95ccad23d05)

</br>
</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
