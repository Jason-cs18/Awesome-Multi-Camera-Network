# Efficient Object Detection
## 1. Gaussian YOLOv3: An Accurate and Fast Object Detector Using Localization Uncertainty for Autonomous Driving. In ICCV'19.
1. Summary: this paper designed a new loss function for YOLOv3 to predict localization uncertainty. Previous work built a uncertainty model for two-stage object detection models. But two-stage object detection approaches have large computational cost and brings too much latency for inference. Thus, the popular object detection models in autonomous driving or other camera-based environment are one-stage detection models. Unfortunately, one-stage detection models are less accurate than two-stage approaches. The accuracy in real world setting brings too many problems of security in driving. Thus, they reconstructed a new loss function for object detection models and improved its accuracy without afftecting speed. Inspired by prior work, they adopted gaussian models to predict the range of localization and utilized localization uncertainty to train a robust one-stage detector. In experiments, they reduced the FP by 41.40% and 40.62%, respectively, and increases the TP by 7.26% and 4.3%, respectively, on the KITTI and BDD datasets.
2. Modifications on YOLOv3: 
  * Transform the output to:
  ![alt text](https://github.com/YanLu-nyu/Awesome-Multi-Camera-Network/blob/master/Images/gaussian_yolo1.png) 
  * Transform the loss function of localization (x, y, w, h) to:
  ![alt text](https://github.com/YanLu-nyu/Awesome-Multi-Camera-Network/blob/master/Images/gaussian_yolo2.png) 


