# Multi-Camera Networks
Multi-camera Networks research notes
## Book
[Multi-Camera Networks: Principles and Applications. 2005.](https://dl.acm.org/citation.cfm?id=1643746)
## Survey
[1] [M.Valera et al. Intelligent distributed surveillance systems: a review. 2005.](https://pdfs.semanticscholar.org/ce96/43fbfcb9c3156c7b26b5c92ec3bc67111202.pdf)<br>
[2] [Wang et al. Intelligent multi-camera video surveillance: a review. 2012.](https://dl.acm.org/citation.cfm?id=2397216)<br>
[3] [Ye et al. Wireless Video Surveillance: A Survey. 2013.](https://www.researchgate.net/publication/270767766_Wireless_Video_Surveillance_A_Survey)<br>
[4] [Zhang et al. Deep Learning in Mobile and Wireless Networking: A Survey. IEEE TRANS 2019.](https://arxiv.org/pdf/1803.04311.pdf)
## Researchers and labs
### Researchers
1. [Ganesh Ananthanarayanan (MSR)](https://www.microsoft.com/en-us/research/people/ga/)
2. [Andrea Cavallaro (QMUL)](http://www.eecs.qmul.ac.uk/~andrea/)
### Labs
1. [Live Video Analytics (MSR)](https://www.microsoft.com/en-us/research/project/live-video-analytics/)
2. [Information Processing Lab (Washington)](http://allison.ee.washington.edu/index.htm)
## Research opportunities
### Camera calibration
[1] [Calibration Wizard: A Guidance System for Camera Calibration Based on Modeling Geometric and Corner Uncertainty. ICCV’19.](https://arxiv.org/pdf/1811.03264.pdf)
### AI applications (todo)
#### Surveilliance systems (reducing deployment cost)
[1] [Zhang et al. The Design and Implementation of a Wireless Video Surveillance System. MobiCom 2015.](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/08/Bahl-MobiCom-2015.pdf)<br>
[2] [Jain et al. Scaling Video Analytics Systems to Large Camera Deployments. HotMobile’19.](https://rtcl.eecs.umich.edu/yuanchao/paper/hotmobile19video.pdf)<br>
#### Multi-View Collaboration (epipolar geometry)
[1] [Kocabas et al. Self-Supervised Learning of 3D Human Pose using Multi-view Geometry. CVPR'19.](https://arxiv.org/abs/1903.02330)<br>
[2] [Yao et al. MONET: Multiview Semi-supervised Keypoint Detection via Epipolar Divergence. ICCV'19.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Yao_MONET_Multiview_Semi-Supervised_Keypoint_Detection_via_Epipolar_Divergence_ICCV_2019_paper.pdf)<br>
[3] [Qiu et al. Cross View Fusion for 3D Human Pose Estimation. ICCV'19.](https://arxiv.org/pdf/1909.01203.pdf)<br>
[4] [Brickwedde et al. Mono-SF: Multi-View Geometry Meets Single-View Depth for Monocular Scene Flow Estimation of Dynamic Traffic Scenes. ICCV'19.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Brickwedde_Mono-SF_Multi-View_Geometry_Meets_Single-View_Depth_for_Monocular_Scene_Flow_ICCV_2019_paper.pdf)<br>
[5] [Trinidad et al. Multi-view Image Fusion. ICCV'19.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Trinidad_Multi-View_Image_Fusion_ICCV_2019_paper.pdf)<br>
[6] [Nassar et al. Simultaneous multi-view instance detection with learned geometric soft-constraints. ICCV'19.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Nassar_Simultaneous_Multi-View_Instance_Detection_With_Learned_Geometric_Soft-Constraints_ICCV_2019_paper.pdf)<br>
[7] [Yao et al. Multiview Cross-supervision for Semantic Segmentation. WACV'20.](https://arxiv.org/abs/1812.01738)<br>
[8] [Zhang et al. Multiview Supervision By Registration. WACV'20.](https://arxiv.org/abs/1811.11251)
#### Efficient Object Detection (popular in autonomous cars or surveilliance cameras)
[1] [Jiwoong et al. Gaussian YOLOv3: An Accurate and Fast Object Detector Using Localization Uncertainty for Autonomous Driving.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Choi_Gaussian_YOLOv3_An_Accurate_and_Fast_Object_Detector_Using_Localization_ICCV_2019_paper.pdf) [Public Code](https://github.com/jwchoi384/Gaussian_YOLOv3)
#### MTMC tracking (todo)
##### Deployment
[1] [Qiu et al. Kestrel: Video Analytics for Augmented Multi-Camera Vehicle Tracking. IOTDI'18.](https://vision.ece.ucsb.edu/sites/default/files/publications/2018_iotdi.pdf)<br>
[2] [Xu et al. STTR: A System for Tracking All Vehicles All the Time At the Edge of the Network. DEBS'18.](https://dl.acm.org/citation.cfm?id=3210291)<br>
[3] [Gupta et al. FogStore: A Geo-Distributed Key-Value Store Guaranteeing Low Latency for Strongly Consistent Access. DEBS'18.](https://dl.acm.org/citation.cfm?id=3210297)<br>
[4] [Hung et al. Wide-area Analytics with Multiple Resources. EuroSys'18.](http://minlanyu.seas.harvard.edu/talk/eurosys18.pdf)<br>
[5] [Jiang et al. Networked Cameras Are the New Big Data Clusters. MobiCom’19 workshop.](https://www.microsoft.com/en-us/research/uploads/prod/2019/08/hotedgevideo19camera.pdf)<br>
[6] [Emmons et al. Cracking open the DNN black-box: Video Analytics with DNNs across the Camera-Cloud Boundary. MobiCom’19 workshop.](https://www.microsoft.com/en-us/research/uploads/prod/2019/08/Split-brain_HotEdgeVideo19.pdf)<br>
[7] [Xu et al. Space-Time Vehicle Tracking at the Edge of the Network. MobiCom’19 workshop.](https://dl.acm.org/citation.cfm?id=3356025)
##### Algorithms (MTMC Tracking)
[1] [Yu et al. The Solution Path Algorithm for Identity-Aware Multi-Object Tracking. CVPR'16.](https://zpascal.net/cvpr2016/Yu_The_Solution_Path_CVPR_2016_paper.pdf)<br>
[2] [Ristani et al. Features for Multi-Target Multi-Camera Tracking and Re-Identification. CVPR'18.](http://zpascal.net/cvpr2018/Ristani_Features_for_Multi-Target_CVPR_2018_paper.pdf)<br>
[3] [Feng et al. Challenges on Large Scale Surveillance Video Analysis. CVPR'18 workshop.](http://openaccess.thecvf.com/content_cvpr_2018_workshops/papers/w3/Feng_Challenges_on_Large_CVPR_2018_paper.pdf)
##### Algorithms (collaborative learning between reID and detection)
[1] [Gidaris et al. LocNet: Improving Localization Accuracy for Object Detection. CVPR'16.](https://www.zpascal.net/cvpr2016/Gidaris_LocNet_Improving_Localization_CVPR_2016_paper.pdf)<br>
[2] [Li et al. Video Object Segmentation with Joint Re-identification and Attention-Aware Mask Propagation. ECCV'18.](http://openaccess.thecvf.com/content_ECCV_2018/papers/Xiaoxiao_Li_Video_Object_Segmentation_ECCV_2018_paper.pdf)<br>
[3] [Huang et al. Adversarially Occluded Samples for Person Re-identification. CVPR'18.](http://openaccess.thecvf.com/content_cvpr_2018/papers/Huang_Adversarially_Occluded_Samples_CVPR_2018_paper.pdf)<br>
[4] [Wang et al. Resource Aware Person Re-identification across Multiple Resolutions. CVPR'18.](http://home.bharathh.info/pubs/pdfs/WangCVPR2018b.pdf)<br>
[5] [Gong et al. Improving Multi-stage Object Detection via Iterative Proposal Refinement. BMVC'19.](https://bmvc2019.org/wp-content/uploads/papers/0545-paper.pdf)<br>
[6] [Luo et al. Detect or Track: Towards Cost-Effective Video Object Detection/Tracking. AAAI'19.](https://www.microsoft.com/en-us/research/uploads/prod/2019/02/AAAI-LuoH.pdf)<br>
[7] [He et al. Bounding Box Regression with Uncertainty for Accurate Object Detection. CVPR'19.](http://openaccess.thecvf.com/content_CVPR_2019/papers/He_Bounding_Box_Regression_With_Uncertainty_for_Accurate_Object_Detection_CVPR_2019_paper.pdf)<br>
[8] [Qi et al. A Novel Unsupervised Camera-aware Domain Adaptation Framework for Person Re-identification. ICCV’19.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Qi_A_Novel_Unsupervised_Camera-Aware_Domain_Adaptation_Framework_for_Person_Re-Identification_ICCV_2019_paper.pdf)<br>
[9] [Zhu et al. Intra-Camera Supervised Person Re-Identification: A New Benchmark. ICCV'19 workshop.](http://openaccess.thecvf.com/content_ICCVW_2019/papers/RLQ/Zhu_Intra-Camera_Supervised_Person_Re-Identification_A_New_Benchmark_ICCVW_2019_paper.pdf)
### Video compression
[1] [Naderiparizi et al. Towards Battery-Free HD Video Streaming. NSDI’18.](https://batteryfreevideo.cs.washington.edu/files/batteryfreevideo.pdf)<br>
[2] [Baig et al. Jigsaw: Robust Live 4K Video Streaming. MobiCom'19.](http://www.cs.utexas.edu/~jianhe/jigsaw-mobicom19.pdf)<br>
[3] [Rippel et al. Learned Video Compression. ICCV 2019.](https://arxiv.org/abs/1811.06981)<br>
[4] [Djelouah et al. Neural Inter-Frame Compression for Video Coding. ICCV 2019.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Djelouah_Neural_Inter-Frame_Compression_for_Video_Coding_ICCV_2019_paper.pdf)<br>
[5] [Habibian et al. Video Compression with Rate-Distortion Autoencoders. ICCV 2019.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Habibian_Video_Compression_With_Rate-Distortion_Autoencoders_ICCV_2019_paper.pdf)<br>
[6] [Xu et al. Non-Local ConvLSTM for Video Compression Artifact Reduction. ICCV 2019.](https://arxiv.org/pdf/1910.12286.pdf)
## Datasets
1. [Duke MTMC (8 cameras)](http://vision.cs.duke.edu/DukeMTMC/)
2. [Nvidia CityFlow (>40 cameras)](https://www.aicitychallenge.org/)
3. [EPFL WildTrack (7 cameras)](https://www.epfl.ch/labs/cvlab/data/data-wildtrack/)
4. [EPFL-RLC (3 cameras)](https://www.epfl.ch/labs/cvlab/data/data-rlc/)
5. [CMU Panoptic Dataset (>50 cameras)](http://domedb.perception.cs.cmu.edu/index.html)
