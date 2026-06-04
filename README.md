
# Object Detection Using Webcam and YOLOv4

## Overview

This project implements a **Real-Time Object Detection System** using a webcam and the **YOLOv4 (You Only Look Once Version 4)** deep learning model. The system captures live video from a webcam, detects multiple objects in real time, draws bounding boxes around detected objects, and displays their class labels along with confidence scores.

YOLOv4 is a state-of-the-art object detection algorithm known for its high speed and accuracy, making it suitable for real-time applications such as surveillance systems, autonomous vehicles, smart monitoring, and human-computer interaction.

---

## Aim

To implement a real-time object detection system using a webcam and YOLOv4, identify objects from live video streams, and display bounding boxes with class labels and confidence scores.

---

## Author

**Name:** Deepak S

**Register Number:** 212224230053

---

## Software Requirements

* Python 3.7 or above
* OpenCV (`opencv-python`)
* NumPy
* Matplotlib
* Jupyter Notebook / Anaconda
* YOLOv4 Configuration File (`yolov4.cfg`)
* YOLOv4 Weights File (`yolov4.weights`)
* COCO Class Labels File (`coco.names`)

---

## Algorithm

### Step 1

Import the required libraries such as OpenCV, NumPy, Matplotlib, and IPython display utilities.

### Step 2

Load the YOLOv4 network using the configuration (`yolov4.cfg`) and pretrained weights (`yolov4.weights`) files.

### Step 3

Load the COCO dataset class labels from the `coco.names` file.

### Step 4

Obtain the names of the YOLO output layers required for object detection.

### Step 5

Initialize webcam video capture using `cv2.VideoCapture(0)`.

### Step 6

Capture video frames continuously from the webcam.

### Step 7

Convert each frame into a blob using `cv2.dnn.blobFromImage()` and resize it to 416 × 416 pixels.

### Step 8

Pass the blob through the YOLOv4 network to perform forward propagation and obtain detection outputs.

### Step 9

Extract object detection information such as:

* Class ID
* Confidence Score
* Bounding Box Coordinates

### Step 10

Filter detections based on a confidence threshold (0.5) to retain only reliable detections.

### Step 11

Apply Non-Maximum Suppression (NMS) using `cv2.dnn.NMSBoxes()` to remove overlapping and duplicate bounding boxes.

### Step 12

Draw bounding boxes around detected objects and display corresponding class labels with confidence scores.

### Step 13

Convert the frame from BGR to RGB format for proper visualization.

### Step 14

Display the processed frame containing detected objects in real time.

### Step 15

Continue detection until the user stops the program.

---

## Output

### Webcam Input

Live video feed captured from the webcam.

### Object Detection

Objects detected using the YOLOv4 deep learning model.

### Bounding Boxes

Green rectangular boxes drawn around detected objects.

### Object Labels

Class names displayed above each detected object.

### Confidence Scores

Detection confidence values shown alongside object labels.

### Real-Time Detection Display

Continuous display of processed frames with object annotations.

---

## Result

The real-time object detection system was successfully implemented using YOLOv4 and OpenCV. Objects appearing in the webcam feed were accurately detected and classified with bounding boxes and confidence scores. The use of Non-Maximum Suppression improved detection quality by eliminating redundant detections.
