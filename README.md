# UFC-FIGHT-ANALYZER
# Kick-Detection-and-pose-estimation
This project is used to detect and count number of kicks in a sample video. It uses Mediapipe for Pose detection and drawing the landmarks over it, it also uses Yolov3 to tackle a problem of multiple person detection which occurs with Mediapipe. A Machine learning model is trained on a dataset for "Kicking" and "Standing" and uses it for detection.
<br />
Note: To run this project on local system download the files and follow the steps mentioned in the notebook

## Clone darknet folder and Load YOLOv3 model
```
!git clone https://github.com/pjreddie/darknet
```
## Download the weights and make the file
``` 
!make
```
```
!wget https://pjreddie.com/media/files/yolov3.weights
```
### With mediapipe there's a problem that it can detect and perform pose landmark detection over a single person, but our project aim was to perfrom kick detection over multiple person so we integrated Yolov3 object detection model to solve this problem.
<br />
## The Yolov3 model in our project is used to detect "Person" which has class=0 in Yolo and draw a box over them so that to run mediapipe on each person and run our model over it
## Apply NMS
## Applying Mediapipe Pose landmark detection
## Training a custom dataset of "Kicking" and "Standing" class using mediapipe and storing the data in a output CSV file
To directly use this model refer to the "fitness_poses_csvs_out.csv" file otherwise create your custom dataset for your different class for example pushup, punch or jump using the steps mentioned in the notebook.
## Apply the tranied model and use it to on detected multiple person to detect and count number of kicks
## References
https://developers.google.com/mediapipe/solutions/vision/pose_landmarker/python
<br />
https://github.com/google/mediapipe/blob/master/docs/solutions/pose.md
<br />
https://github.com/nachi-hebbar/Object-Detection-Yolo-V3-Darknet/blob/main/YOLO_V3.ipynb

