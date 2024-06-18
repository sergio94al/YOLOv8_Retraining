# YOLOv8_Retraining
This repository explains how to retrain a YOLO network with our data to do detection.
The structure of the data folders must be: 

Data
- images
  - train
  - val
- labels
  - train
  - val

    
In this way, .yaml files can be created to feed into the network for training. Once the network is trained, training metrics such as mAP, accuracy, recall, etc... can be obtained.

<p align="center">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/metrics_plots.png" width="950" height="400">
</p>

Once we have the model created and the best.pt weight parameters have been saved, we can load them in order to make predictions. 
<p align="center">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/predicting_images.png" width="950" height="400">
</p>
In this case we make predictions on images and on videos frame by frame, getting a correct traffic signal detection.

<p align="center">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/real_images_prediction.png" width="400" height="300" style="display: inline-block;">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/Video_predicting.gif" width="400" height="300" style="display: inline-block;">
</p>



