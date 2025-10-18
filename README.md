
# Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

# Software Used
Anaconda - Python 3.7
# Algorithm
### Step 1:

Import the OpenCV library (cv2).

### Step 2:

Initialize the webcam using cv2.VideoCapture(0).

### Step 3:

Capture frames in a loop, and:

Save a frame as JPG file using cv2.imwrite().

Display the live video stream using cv2.imshow().

### Step 4:

Resize the video frame using cv2.resize() and display it.

### Step 5:

Rotate the frame using cv2.rotate() and display the rotated video.

### Step 6:

Break the loop when the user presses the ‘q’ key and release the camera.

# Program:
### Developed By:Dhivya Dharshini B
### Register No: 212223240031

### i) Write the frame as JPG file
```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time

capture=cv2.VideoCapture(0)
ret,frame=capture.read()
if ret:
    cv2.imwrite("image.jpg",frame)
capture.release()
captured=cv2.imread('image.jpg')

plt.imshow(captured[:,:,::-1])
plt.title('Captured Image')
plt.axis('off')
plt.show()
```

### ii) Display the video
```
Capture=cv2.VideoCapture(0)
for i in range(50):
    ret,frame=Capture.read()
    if not ret:
        break
    org_frame=cv2.cvtColor(frame,cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(org_frame)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)
Capture.release()
```




### iii) Display the video by resizing the window
```
capture=cv2.VideoCapture(0)
for i in range(50):
    ret,frame=capture.read()
    if not ret:
        break
    resized=cv2.resize(frame,(100,150))
    org_frame=cv2.cvtColor(resized,cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(org_frame)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)
capture.release()
```



### iv) Rotate and display the video

```
capture=cv2.VideoCapture(0)
for i in range(50):
    ret,frame=capture.read()
    if not ret:
        break
    rotated=cv2.rotate(frame,cv2.ROTATE_90_CLOCKWISE)
    org_frame=cv2.cvtColor(rotated,cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(org_frame)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)
capture.release()
```

# Output

### i) Write the frame as JPG image
<img width="512" height="411" alt="download" src="https://github.com/user-attachments/assets/b39121f6-4dc5-41a9-94f6-b7c8fcb49394" />



### ii) Display the video


<img width="512" height="389" alt="download" src="https://github.com/user-attachments/assets/208794d1-0355-4f57-9b2c-e0ec228d0efa" />



### iii) Display the video by resizing the window



<img width="266" height="389" alt="download" src="https://github.com/user-attachments/assets/23c746a9-6e16-4f87-b9b5-6401510b00c0" />



### iv) Rotate and display the video

<img width="297" height="389" alt="download" src="https://github.com/user-attachments/assets/16b5e272-e502-41e8-bca2-8bba2a173ed8" />


## Result:
Thus the image is accessed from webcamera and displayed using openCV.
