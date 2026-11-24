## YOLOv8-Object-Detection-Using-Laptop-Camera

## Aim:

To access the laptop camera, capture an image, and detect objects using YOLOv8.

## Software Requirements:

* Anaconda
* Jupyter Notebook
* Laptop Camera

## Steps:

* Open Jupyter Notebook using Anaconda.
* Access your laptop camera using OpenCV.
* Wait for 5 seconds and capture an image.
* Display the captured image.
* Apply YOLOv8 object detection.
* Display the detected image with bounding boxes and labels.

## Algorithm:

```
Laptop Camera
      ↓
Capture Image
      ↓
Display Image
      ↓
YOLOv8 Detection
      ↓
Display Detected Objects
```

## Student Task:

* Capture your own image using the laptop camera.
* Detect the objects present in the image.
* Display the final output.
* Perform the experiment with 3 different scenes.

## Program:

```
from ultralytics import YOLO
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
```

```
model = YOLO("yolov8m.pt")
```

```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time

print("Libraries imported successfully!")
```

```
cap = cv2.VideoCapture(0)

if not cap.isOpened():
    print("Webcam not detected!")
else:
    ret, frame = cap.read()

    if ret:
        plt.imshow(cv2.cvtColor(frame, cv2.COLOR_BGR2RGB))
        plt.title("Webcam Capture")
        plt.axis("off")
        plt.show()

cap.release()
```

## Output:

<img width="637" height="507" alt="image" src="https://github.com/user-attachments/assets/48676a60-9cf7-4bf7-adf8-0995891371ab" />

## Result: 

Thus the Object Detection Using Web camera was successfully completed
