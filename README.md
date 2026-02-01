# Image_Acqusition-_using_Web_Camera
## Name: SAJITH AHAMED F
## Register no: 212223240144

## Aim:

To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import OpenCV Package.

### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.


## Program:
### Developed By: SAJITH AHAMED F
### Register No: 212223240144


## i) Write the frame as JPG file

```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("Sajith.jpg", frame)
cap.release()
captured_image = cv2.imread('Sajith.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.axis('off')
plt.show()

```


## ii) Display the video

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```


## iii) Display the video by resizing the window

```

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
  

```


## iv) Rotate and display the video

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release() 
```

## Output

### i) Write the frame as JPG image
<img width="960" height="681" alt="image" src="https://github.com/user-attachments/assets/a97012c1-8dd5-4f4b-aeed-1085493f6e20" />



### ii) Display the video
<img width="1024" height="682" alt="image" src="https://github.com/user-attachments/assets/44a26793-f33a-4b56-99f9-d3e26dd3ef4b" />





### iii) Display the video by resizing the window
<img width="456" height="686" alt="image" src="https://github.com/user-attachments/assets/5c47acf1-28a4-470b-a893-97c81328643a" />







### iv) Rotate and display the video
<img width="331" height="613" alt="image" src="https://github.com/user-attachments/assets/f1ec8f2d-12fc-43c2-b25e-99433acd8331" />




## Result:
Thus the image is accessed from webcamera and displayed using openCV.
