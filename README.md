# Kick Detection and Pose Estimation

This project is designed to detect and count kicks, standing postures, and punches in a video. It combines the power of *Mediapipe* for pose estimation and *YOLOv3/YOLOv5* for multi-person object detection, overcoming the limitations of pose detection models for multi-person scenarios. A machine learning model has been trained on custom datasets to classify actions into three categories: *Kick, **Standing, and **Punches*.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Demo](#demo)
- [References](#references)

---

## Project Overview

### Key Objectives:
1. *Kick Detection*: Detect and count kicks performed by individuals in the video.
2. *Standing Detection*: Identify standing postures for activity tracking.
3. *Punches Detection*: Detect punching actions for comprehensive activity analysis.

### Why YOLO?
- Mediapipe is efficient for pose detection but works best with a single person in the frame. To address multi-person scenarios, *YOLOv3/YOLOv5* is integrated to detect multiple people and track their actions efficiently.

---

## Features

1. *Multi-Person Detection*:
   - YOLOv3/YOLOv5 is used to detect persons (class=0 in YOLO) in a frame and draw bounding boxes.
   - Non-Maximum Suppression (NMS) is applied to remove overlapping bounding boxes and retain the one with the highest confidence.

2. *Pose Estimation*:
   - Mediapipe is used for pose detection within each bounding box to track landmarks for each individual.

3. *Custom Model Training*:
   - A custom dataset for "Kick," "Standing," and "Punches" classes is created using Mediapipe.
   - The dataset is stored in a CSV file and used to train the model. (Refer to fitness_poses_csvs_out.csv for the dataset.)

4. *Action Classification*:
   - The trained model is applied to classify detected actions and count the occurrences.

---

## Demo 
https://github.com/Sourabh-Singh-Tech/Combat-Profiler/blob/main/Combat%20Profiler%20Demo.mp4
## References
https://developers.google.com/mediapipe/solutions/vision/pose_landmarker/python
<br />
https://github.com/google/mediapipe/blob/master/docs/solutions/pose.md
<br />
https://github.com/nachi-hebbar/Object-Detection-Yolo-V3-Darknet/blob/main/YOLO_V3.ipynb

