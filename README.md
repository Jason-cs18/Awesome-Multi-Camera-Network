# Multi-Camera Networks
Multi-camera Networks research notes. **Target venues**: network conferences (*NSDI/SIGCOMM*), mobile conferences (*MobiCom/MobiSys/SenSys/UbiComp*) and computer vision conferences (*ICCV/CVPR/ECCV*).<br>
Inspired by [book](https://dl.acm.org/citation.cfm?id=1643746), I collect papers from four topics in research opportunities: 
1. Camera Calibration. 
2. AI Applications (surveilliance systems, multi-view collaboration, **multi-camera collaboration**, efficient object detection, automatic labeling, **MTMC tracking**). 
3. Video Compression (for efficient communication). 
4. Database (for fast indexing).
5. [**Privacy**](#Privacy) (for privacy-preserving inference/training/transmission).

In the end, I list datasets and useful toolboxes (I will keep maintaining this list).
## Book
1. [Multi-Camera Networks: Principles and Applications. 2005.](https://dl.acm.org/citation.cfm?id=1643746)
2. [Camera Networks: The Acquisition and Analysis of Videos over Wide Areas (Synthesis Lectures on Computer Vision). 2012.](https://epdf.pub/camera-networks-the-acquisition-and-analysis-of-videos-overwide-areas.html)
## Survey
[1] [M.Valera et al. Intelligent distributed surveillance systems: a review. 2005.](https://pdfs.semanticscholar.org/ce96/43fbfcb9c3156c7b26b5c92ec3bc67111202.pdf)<br>
[2] [Wang et al. Intelligent multi-camera video surveillance: a review. 2012.](https://dl.acm.org/citation.cfm?id=2397216)<br>
[3] [Ye et al. Wireless Video Surveillance: A Survey. 2013.](https://www.researchgate.net/publication/270767766_Wireless_Video_Surveillance_A_Survey)<br>
[4] [Zhang et al. Deep Learning in Mobile and Wireless Networking: A Survey. IEEE TRANS 2019.](https://arxiv.org/pdf/1803.04311.pdf)
## Researchers, labs and workshops
### Researchers (organization and research interests)
1. [Ganesh Ananthanarayanan (MSR, USA)](https://www.microsoft.com/en-us/research/people/ga/) - Live video analytics, distributed computing
2. [Yuanchao Shu (MSR, USA)](https://www.microsoft.com/en-us/research/people/yushu/) - Live video analytics, location-based systems
3. [Andrea Cavallaro (QMUL, ENG)](http://www.eecs.qmul.ac.uk/~andrea/) - Low-level vision tasks across camera networks, multi-modal fusion, **privacy-aware video analytics (based on adversarial-training/learning)**
4. [Amit K. Roy-Chowdhury (UC Riverside, USA)](https://vcg.engr.ucr.edu/people/amit-roy-chowdhury) - Deep learning based video analytics (tracking, reID, super-resolution and domain adaptation)
5. [Jenq-Neng Hwang (UW, USA)](https://people.ece.uw.edu/hwang/) - Deep learning based video analytics (tracking, reID, localization, visual odometry)
6. [Hamid K. Aghajan (UGent, BE)](https://dblp.org/pers/a/Aghajan:Hamid_K=.html) - Video analytics across multi-cameras
7. [Umakishore Ramachandran (Gatech, USA)](https://www.cc.gatech.edu/~rama/) - Edge AI (OS, kernel)
8. [Youngki Lee (SNU, KR)](http://youngkilee.blogspot.com/) - Edge AI and AR/VR
9. [Juncheng Jiang (UChicago, USA)](https://people.cs.uchicago.edu/~junchenj/) - Video streaming
10. [Ravi Netravali (Princeton, USA)](https://www.cs.princeton.edu/~ravian/) - Edge AI
11. [Silvio Savarese (Stanford, USA)](https://scholar.google.com/citations?hl=zh-CN&user=ImpbxLsAAAAJ&view_op=list_works&sortby=pubdate) - 3D vision and robotics
12. [Fengyuan Xu (NJU, CN)](https://cs.nju.edu.cn/fxu/) - the Internet of Video Things (IoVT)
### Labs
1. [Live Video Analytics (MSR)](https://www.microsoft.com/en-us/research/project/live-video-analytics/)
2. [Information Processing Lab (Washington)](http://allison.ee.washington.edu/index.htm)
3. [Video Computing Group (UC Riverside)](https://vcg.engr.ucr.edu/)
4. [Vision Research Lab (UCSB)](https://vision.ece.ucsb.edu/)
5. [Audio-visual Signal processing and Communication Systems (Berkeley)](https://people.eecs.berkeley.edu/~kannanr/about.html)
6. [Human-Centered Computer Systems Lab (SNU)](https://hcs.snu.ac.kr/)
### Workshops
1. [The 3rd Workshop on Hot Topics in Video Analytics and Intelligent Edges (*ACM MobiCom'21*)](https://www.microsoft.com/en-us/research/event/the-3rd-workshop-on-hot-topics-in-video-analytics-and-intelligent-edges/#!call-for-papers) - focus on deep learning based video analytics.
### Courses
1. [CS231A: Computer Vision, From 3D Reconstruction to Recognition (Winter 2021, Stanford)](https://web.stanford.edu/class/cs231a/) - focus on basic concepts behind many computer vision tasks across multi-camera networks (camera models, calibration, single- and multiple-view geometry, stereo systems, sfm, stereo, matching, depth estimation, optical flow and optimal estimation). 
2. [CS239: ML-driven Video Analytics Systems (Fall 2020, UCLA)](http://web.cs.ucla.edu/~ravi/CS239_F20/index.html) - target to recent research interests on video analytics (_Strong Recommendation_)
3. [CS34702 Topics in Networks: Machine Learning for Networking and Systems (Fall 2020, UChicago)](https://people.cs.uchicago.edu/~junchenj/34702-f20/syllabus.html) - target to awesome recent research works on netwoking system (_video streaming and cloud scheduing_ are recommended)
## Research opportunities
### Camera calibration
[1] [Calibration Wizard: A Guidance System for Camera Calibration Based on Modeling Geometric and Corner Uncertainty. In *ICCV'19*.](https://arxiv.org/pdf/1811.03264.pdf)
### AI applications (todo)
#### Surveilliance systems (reducing deployment cost)
[1] [Zhang et al. The Design and Implementation of a Wireless Video Surveillance System. In *MobiCom'15*.](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/08/Bahl-MobiCom-2015.pdf)<br>
[2] [Jain et al. Scaling Video Analytics Systems to Large Camera Deployments. In *HotMobile'19*.](https://rtcl.eecs.umich.edu/yuanchao/paper/hotmobile19video.pdf)<br>
[3] [Xu et al. Approximate Query Service on Autonomous IoT Cameras. In *MobiSys'20*.](https://arxiv.org/pdf/1909.00841.pdf)<br>
[4] [Bhardwaj et al. Ekya: Continuous Learning of Video Analytics Models on Edge Compute Servers. In *NSDI'22*.](https://arxiv.org/abs/2012.10557) - target to solve when to retrain models and how to reduce resource usage for multi-tasks (many inference and retraining tasks). <br>
[5] [Suprem et al. ODIN: Automated Drift Detection and Recovery in Video Analytics. In *VLDB'21*.](http://www.vldb.org/pvldb/vol13/p2453-suprem.pdf) - target to detect domain drift and update corresponding models automatically. 
#### Multi-View Collaboration (epipolar geometry)
[1] [Kocabas et al. Self-Supervised Learning of 3D Human Pose using Multi-view Geometry. In *CVPR'19*.](https://arxiv.org/abs/1903.02330)<br>
[2] [Yao et al. MONET: Multiview Semi-supervised Keypoint Detection via Epipolar Divergence. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Yao_MONET_Multiview_Semi-Supervised_Keypoint_Detection_via_Epipolar_Divergence_ICCV_2019_paper.pdf)<br>
[3] [Qiu et al. Cross View Fusion for 3D Human Pose Estimation. In *ICCV'19*.](https://arxiv.org/pdf/1909.01203.pdf)<br>
[4] [Brickwedde et al. Mono-SF: Multi-View Geometry Meets Single-View Depth for Monocular Scene Flow Estimation of Dynamic Traffic Scenes. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Brickwedde_Mono-SF_Multi-View_Geometry_Meets_Single-View_Depth_for_Monocular_Scene_Flow_ICCV_2019_paper.pdf)<br>
[5] [Trinidad et al. Multi-view Image Fusion. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Trinidad_Multi-View_Image_Fusion_ICCV_2019_paper.pdf)<br>
[6] [Nassar et al. Simultaneous multi-view instance detection with learned geometric soft-constraints. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Nassar_Simultaneous_Multi-View_Instance_Detection_With_Learned_Geometric_Soft-Constraints_ICCV_2019_paper.pdf)<br>
#### Multi-Camera Collaboration (exploring collaboration in a large camera networks, such as drone networks)
[1] [Liu et al. Who2com: Collaborative Perception via Learnable Handshake Communication. In *ICRA'20*.](https://arxiv.org/abs/2003.09575)<br>
[2] [Liu et al. When2com: Multi-Agent Perception via Communication Graph Grouping. In *CVPR'20*.](http://openaccess.thecvf.com/content_CVPR_2020/papers/Liu_When2com_Multi-Agent_Perception_via_Communication_Graph_Grouping_CVPR_2020_paper.pdf)<br>
[3] [Tong et al. Large-Scale Vehicle Trajectory Reconstruction with Camera Sensing Network. In *MobiCom'21*.](https://wands.sg/publications/full_list/papers/MobiCom_21_1.pdf)
#### Efficient Object Detection (popular in autonomous cars or surveilliance cameras)
[1] [Jiwoong et al. Gaussian YOLOv3: An Accurate and Fast Object Detector Using Localization Uncertainty for Autonomous Driving. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Choi_Gaussian_YOLOv3_An_Accurate_and_Fast_Object_Detector_Using_Localization_ICCV_2019_paper.pdf) [Public Code](https://github.com/jwchoi384/Gaussian_YOLOv3) [Note](https://github.com/YanLu-nyu/Awesome-Multi-Camera-Network/blob/master/Efficient_Object_Detection.md) <br>
[2] [Wang et al. Learning Rich Features at High-Speed for Single-Shot Object Detection. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Wang_Learning_Rich_Features_at_High-Speed_for_Single-Shot_Object_Detection_ICCV_2019_paper.pdf) [Public Code](https://github.com/vaesl/LRF-Net) [Note](https://github.com/YanLu-nyu/Awesome-Multi-Camera-Network/blob/master/Efficient_Object_Detection.md)
#### Automatic Labeling (object detection and reID)
[1] [H. Aghdam et al. Active Learning for Deep Detection Neural Networks. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Aghdam_Active_Learning_for_Deep_Detection_Neural_Networks_ICCV_2019_paper.pdf) [Public Code](https://gitlab.com/haghdam/deep_active_learning) [Note](https://github.com/YanLu-nyu/Awesome-Multi-Camera-Network/blob/master/Automatic_Labeling.md)
#### MTMC tracking (todo)
##### Deployment
[1] [Qiu et al. Kestrel: Video Analytics for Augmented Multi-Camera Vehicle Tracking. In *IOTDI'18*.](https://vision.ece.ucsb.edu/sites/default/files/publications/2018_iotdi.pdf)<br>
[2] [Xu et al. STTR: A System for Tracking All Vehicles All the Time At the Edge of the Network. In *DEBS'18*.](https://dl.acm.org/citation.cfm?id=3210291)<br>
[3] [Gupta et al. FogStore: A Geo-Distributed Key-Value Store Guaranteeing Low Latency for Strongly Consistent Access. In *DEBS'18*.](https://dl.acm.org/citation.cfm?id=3210297)<br>
[4] [Hung et al. Wide-area Analytics with Multiple Resources. In *EuroSys'18*.](http://minlanyu.seas.harvard.edu/talk/eurosys18.pdf)<br>
[5] [Jiang et al. Networked Cameras Are the New Big Data Clusters. In *MobiCom’19 workshop*.](https://www.microsoft.com/en-us/research/uploads/prod/2019/08/hotedgevideo19camera.pdf)<br>
[6] [Emmons et al. Cracking open the DNN black-box: Video Analytics with DNNs across the Camera-Cloud Boundary. In *MobiCom’19 workshop*.](https://www.microsoft.com/en-us/research/uploads/prod/2019/08/Split-brain_HotEdgeVideo19.pdf)<br>
[7] [Xu et al. Space-Time Vehicle Tracking at the Edge of the Network. In *MobiCom’19 workshop*.](https://dl.acm.org/citation.cfm?id=3356025)<br>
[8] [Xu et al. Coral-Pie: A Geo-Distributed Edge-compute Solution for Space-Time Vehicle Tracking. In *Middleware'20*.](https://dl.acm.org/doi/abs/10.1145/3423211.3425686)<br>
[9] [Li et al. Reducto: On-Camera Filtering for Resource-Efficient Real-Time Video Analytics. In *SIGCOMM'20*.](https://dl.acm.org/doi/pdf/10.1145/3387514.3405874)
##### Algorithms (MTMC Tracking)
[1] [Yu et al. The Solution Path Algorithm for Identity-Aware Multi-Object Tracking. In *CVPR'16*.](https://zpascal.net/cvpr2016/Yu_The_Solution_Path_CVPR_2016_paper.pdf)<br>
[2] [Ristani et al. Features for Multi-Target Multi-Camera Tracking and Re-Identification. In *CVPR'18*.](http://zpascal.net/cvpr2018/Ristani_Features_for_Multi-Target_CVPR_2018_paper.pdf)<br>
[3] [Feng et al. Challenges on Large Scale Surveillance Video Analysis. In *CVPR'18 workshop*.](http://openaccess.thecvf.com/content_cvpr_2018_workshops/papers/w3/Feng_Challenges_on_Large_CVPR_2018_paper.pdf)
##### Algorithms (collaborative learning between reID and detection)
[1] [Gidaris et al. LocNet: Improving Localization Accuracy for Object Detection. In *CVPR'16*.](https://www.zpascal.net/cvpr2016/Gidaris_LocNet_Improving_Localization_CVPR_2016_paper.pdf)<br>
[2] [Li et al. Video Object Segmentation with Joint Re-identification and Attention-Aware Mask Propagation. In *ECCV'18*.](http://openaccess.thecvf.com/content_ECCV_2018/papers/Xiaoxiao_Li_Video_Object_Segmentation_ECCV_2018_paper.pdf)<br>
[3] [Huang et al. Adversarially Occluded Samples for Person Re-identification. In *CVPR'18*.](http://openaccess.thecvf.com/content_cvpr_2018/papers/Huang_Adversarially_Occluded_Samples_CVPR_2018_paper.pdf)<br>
[4] [Wang et al. Resource Aware Person Re-identification across Multiple Resolutions. In *CVPR'18*.](http://home.bharathh.info/pubs/pdfs/WangCVPR2018b.pdf)<br>
[5] [Gong et al. Improving Multi-stage Object Detection via Iterative Proposal Refinement. In *BMVC'19*.](https://bmvc2019.org/wp-content/uploads/papers/0545-paper.pdf)<br>
[6] [Luo et al. Detect or Track: Towards Cost-Effective Video Object Detection/Tracking. In *AAAI'19*.](https://www.microsoft.com/en-us/research/uploads/prod/2019/02/AAAI-LuoH.pdf)<br>
[7] [He et al. Bounding Box Regression with Uncertainty for Accurate Object Detection. In *CVPR'19*.](http://openaccess.thecvf.com/content_CVPR_2019/papers/He_Bounding_Box_Regression_With_Uncertainty_for_Accurate_Object_Detection_CVPR_2019_paper.pdf)<br>
[8] [Qi et al. A Novel Unsupervised Camera-aware Domain Adaptation Framework for Person Re-identification. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Qi_A_Novel_Unsupervised_Camera-Aware_Domain_Adaptation_Framework_for_Person_Re-Identification_ICCV_2019_paper.pdf)<br>
[9] [Zhu et al. Intra-Camera Supervised Person Re-Identification: A New Benchmark. In *ICCV'19 workshop*.](http://openaccess.thecvf.com/content_ICCVW_2019/papers/RLQ/Zhu_Intra-Camera_Supervised_Person_Re-Identification_A_New_Benchmark_ICCVW_2019_paper.pdf)<br>
[10] [Wang et al. Exploit the Connectivity: Multi-Object Tracking with TrackletNet. In *MM'19*.](https://dl.acm.org/doi/10.1145/3343031.3350853)
### Video compression (including video streaming)
[1] [Naderiparizi et al. Towards Battery-Free HD Video Streaming. In *NSDI’18*.](https://batteryfreevideo.cs.washington.edu/files/batteryfreevideo.pdf)<br>
[2] [Baig et al. Jigsaw: Robust Live 4K Video Streaming. In *MobiCom'19*.](http://www.cs.utexas.edu/~jianhe/jigsaw-mobicom19.pdf)<br>
[3] [Rippel et al. Learned Video Compression. In *ICCV'19*.](https://arxiv.org/abs/1811.06981)<br>
[4] [Djelouah et al. Neural Inter-Frame Compression for Video Coding. In *ICCV'19*.](https://openaccess.thecvf.com/content_ICCV_2019/papers/Djelouah_Neural_Inter-Frame_Compression_for_Video_Coding_ICCV_2019_paper.pdf)<br>
[5] [Habibian et al. Video Compression With Rate-Distortion Autoencoders. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Habibian_Video_Compression_With_Rate-Distortion_Autoencoders_ICCV_2019_paper.pdf)<br>
[6] [Xu et al. Non-Local ConvLSTM for Video Compression Artifact Reduction. In *ICCV'19*.](https://arxiv.org/pdf/1910.12286.pdf)<br>
[7] [Y. Yan et al. Learning in situ: a randomized experiment in video streaming. In *NSDI'20*.](https://www.usenix.org/conference/nsdi20/presentation/yan)<br>
[8] [Kim et al. Neural-Enhanced Live Streaming: Improving Live Video Ingest via Online Learning. In *SIGCOMM'20*.](https://dl.acm.org/doi/abs/10.1145/3387514.3405856)<br>
[9] [Du et al. Server-Driven Video Streaming for Deep Learning Inference. In *SIGCOMM'20*.](https://dl.acm.org/doi/pdf/10.1145/3387514.3405887)<br>
[10] [Han et al. ViVo: Visibility-aware Mobile Volumetric Video Streamin. In *MobiCom'20*.](https://dl.acm.org/doi/10.1145/3372224.3380888)<br>
[11] [Zhang et al. SENSEI: Aligning Video Streaming Quality with Dynamic User Sensitivity. In *NSDI'21*.](https://www.usenix.org/conference/nsdi21/presentation/zhang-xu)<br>
### Database
[1] [Saurez et al. A drop-in middleware for serializable DB clustering across geo-distributed sites. In VLDB'20.](https://dl.acm.org/doi/10.14778/3415478.3415555)
### Privacy
|   Useful external links  | Keywords |
|  ----  | ----  |
| [Tutorial on privacy-preserving data analysis (The Alan Turing Institute)](https://www.turing.ac.uk/research/interest-groups/privacy-preserving-data-analysis)  | todo |
| [The Second AAAI Workshop on Privacy-Preserving Artificial Intelligence (PPAI-21)](https://ppai21.github.io/)  | todo |
| [A Dive into Privacy Preserving Machine Learning (OpML'21)](https://www.usenix.org/conference/opml20/presentation/pham) | todo |

[1] [(TAMU and Adobe Research) Wu et al. Towards Privacy-Preserving Visual Recognition via Adversarial Training: A Pilot Study. In _ECCV'18_.](https://openaccess.thecvf.com/content_ECCV_2018/papers/Zhenyu_Wu_Towards_Privacy-Preserving_Visual_ECCV_2018_paper.pdf)<br>
[2] [(CMU) Wang et al. Enabling Live Video Analytics with a Scalable and Privacy-Aware Framework. In _2018 ACM Transactions on Multimedia Computing, Communications, and Applications (TOMM'18)_.](https://www.privacyassistant.org/media/publications/tomm2018.pdf)<br>
[3] [(KAIST, USTC, Rice, NJU, SNU, PKU and MSRA) Lee et al. Occlumency: Privacy-preserving Remote Deep-learning Inference Using SGX. In _MobiCom'19_.](https://dl.acm.org/doi/10.1145/3300061.3345447)<br>
[4] [(NUS) Shen et al. Human-imperceptible Privacy Protection Against Machines. In _MM'19_.](https://dl.acm.org/doi/10.1145/3343031.3350963)<br>
[5] [(PSU and Facebook) Khazbak et al. TargetFinder: Privacy Preserving Target Search through IoT Cameras. In _IoTDI'19_. (Best Paper Award)](http://mcn.cse.psu.edu/paper/youssef/iotdi-youssef19.pdf)<br>
[6] [(Tsinghua and USTC) Li et al. Invisible: Federated Learning over Non-Informative Intermediate Updates against Multimedia Privacy Leakages. In _MM'20_.](https://dl.acm.org/doi/abs/10.1145/3394171.3413923)<br>
[7] [(UCB and MSR) Poddar et al. Visor: Privacy-Preserving Video Analytics as a Cloud Service. In _29th	Usenix Security Symposium (Security'20)_.](https://www.usenix.org/conference/usenixsecurity20/presentation/poddar)<br>
[8] [(NJU, Cornell and MSRA) Wu et al. PECAM: privacy-enhanced video streaming and analytics via securely-reversible transformation. In _MobiCom'21_.](https://dl.acm.org/doi/abs/10.1145/3447993.3448618)<br>
[9] [(CMU, UCSD and MSR) Dsouza et al. Amadeus: Scalable, Privacy-Preserving Live Video Analytics. _arXiv prePrint 2011.05163_.](https://arxiv.org/pdf/2011.05163.pdf)<br>
[10] [(MIT, Princeton, UChicago and Rutgers) Cangialosi et al. Privid: Practical, Privacy-Preserving Video Analytics Queries. _arXiv prePrint 2106.12083_.](https://arxiv.org/pdf/2106.12083.pdf)<br>
[11] read recent privacy-preserving data processing papers published in **VLDB and SIGMOD** (to find interesting issues on privacy-preserving video processing).
## Dataset
1. [Duke MTMC (8 cameras, non-overlapping)](http://vision.cs.duke.edu/DukeMTMC/)
2. [Nvidia CityFlow (>40 cameras, overlapping and non-overlapping)](https://www.aicitychallenge.org/)
3. [EPFL WildTrack (7 cameras, overlapping)](https://www.epfl.ch/labs/cvlab/data/data-wildtrack/)
4. [EPFL-RLC (3 cameras, overlapping)](https://www.epfl.ch/labs/cvlab/data/data-rlc/)
5. [CMU Panoptic Dataset (>50 cameras, overlapping)](http://domedb.perception.cs.cmu.edu/index.html)
6. [University of Illinois STREETS (100 cameras, non-overlapping)](https://databank.illinois.edu/datasets/IDB-3671567)
7. [Awesome reID dataset](https://github.com/NEU-Gou/awesome-reid-dataset)
## Toolbox
1. [CHUK-mmcv](https://github.com/open-mmlab/mmcv): a foundational python library for computer vision research and supports many research projects (2D/3D detection, semantic segmentation, image and video editing, pose estimation, action understanding and image classification).
2. [JDCV-fastreid](https://github.com/JDAI-CV/fast-reid): a python library implementing SOTA re-identification methods (including pedestrian and vehicle re-identification). They also provided a good documentation.
