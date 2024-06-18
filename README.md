# YOLOv8_Retraining
This repository provides a comprehensive guide on retraining a **YOLO v8.2 network using custom datasets** for precise **traffic signal detection and identification**, typically employed in autonomous vehicle applications. For this purpose, Google Colab and its GPU T4 are utilized to enhance the efficiency of the training process.

<p align="center">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/dataset_.png" width="850" height="500">
</p>

## 1. Data Preparing & Training

The structure of the data folders must be: 

A. Data
- images
  - train
  - val
- labels
  - train
  - val
     
In this way, .yaml files can be created to feed into the network for training. Once the network is trained, **training metrics** such as mAP, accuracy, recall, etc... can be obtained. During training, a run-detect folder is created for training and validation where all metrics, graphs and other data such as the best network parameters and the last run parameters are stored.

B. Runs
- detect
    - train
        - weights
          - best.pt
          - last.pt
    - val

<p align="center">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/metrics_plots.png" width="900" height="400">
</p>

## 2. Predicting new images and videos
Once we have the model created and the **best.pt weight parameters** have been saved, we can load them in order to make predictions. 

<p align="center">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/predicting_images.png" width="950" height="350">
</p>

<p align="center">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/Video_predicting_code.png" width="600" height="500">
</p>


In this case, we employ a YOLO neural network retrained specifically for detecting traffic signals in **images and videos**, analyzing each frame individually. This enables us to obtain accurate and reliable predictions regarding the presence and location of traffic signals in diverse and dynamic environments.

<p align="center">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/real_images_prediction.png" width="400" height="400" style="display: inline-block;">
    <img src="https://github.com/sergio94al/YOLOv8_Retraining/blob/main/Video_predicting.gif" width="400" height="400" style="display: inline-block;">
</p>

## 3. Resources
1. https://docs.ultralytics.com/
2. https://colab.research.google.com/ (Edit - Configurations - GPU T4)
3. https://github.com/kiarashrahmani/Traffic-sign-detection-using-yolo/tree/main/Dataset (Dataset used)

