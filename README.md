# Multi-Camera Networks
- Multi-camera Networks research notes. **Target venues**: system conferences (OSDI/SOSP/ATC/EuroSys), network (*NSDI/SIGCOMM/SoCC*), mobile (*MobiCom/MobiSys/SenSys/UbiComp*), data analytics (*VLDB/SIGMOD*) and computer vision (*ICCV/CVPR/ECCV/ICML/ICLR/NeurIPS*).
- Unlike [book](https://dl.acm.org/citation.cfm?id=1643746), I collect papers from system and AI perspective, respectively. To avoid diving into details of specific vision tasks (*eg.,* object detection), I only list **low-resource learning**, **domain adaptation & continual learning** and **dynamic deep neural networks** in [AI Algorithm](#AI-Algorithm) because I think these three topics are generalized on all vision tasks and are useful to help us deploy deep learning based vision applications. In the end, I list datasets and useful toolboxes.

Note: specific vision algorithms (tracking, object detection, segmentation and action recognition) are not collected in this note. If you want to learn or try them, you can refer to [SenseTime-CHUK Open-MMLab](https://github.com/open-mmlab/mmcv), which provides a suit of toolboxes to help AI researcher/engineers implement vision algorithms. For example, you can try 50+ image-based object detection models using the same [mmdetection](https://mmdetection.readthedocs.io/en/latest/) API and try 10+ video-based object detection methods using the same [mmtracking](https://github.com/open-mmlab/mmtracking) API. 
## Outline
- [Book and Survey](#Book-and-Survey) - a starting point to understand basic concepts behind multi-camera networks
- [Researchers, Workshops and Courses](#Researchers-and-Workshops&Courses) - follow them to get recent research trends in multi-camera networks
- [Topics](#Topics) - group recent papers in different sub-topics (*i.e.,* Camera calibration)
  - [System](#System)
    - [Edge video analytics](#Edge-video-analytics) - speed up analysis pipeline
    - [Configuration search](#Configuration-search) - search most suitable configuration file
    - [Database](#Database) - distributed data processing
    - [Video streaming](#Video-streaming) - video compression
    - [Resource management](#Resource-aware-video-analytics) - resource managment
    - [Prediction serving and model update](#Prediction-serving-and-model-update) - model exchange, prediction serving, model monitoring and model updates
    - [Multi-Camera Collaboration](#Multi-Camera-Collaboration) - improve performance and reduce deployments' cost
    - [Privacy](#Privacy) - data privacy, model privacy and computation privacy
  - [AI Algorithm](#AI-Algorithm)
    - [Low-resource learning](#Low-resource-learning) - efficient learning under limited data/annotations/computation/(time)
      - In AI, low-resource learning is often named low-shot learning (few-/one-/zero-shot learning), which expect to retrain or train from the sratch with only a few new data. Inspired by [style transfer](https://www.youtube.com/watch?v=IIRxJvW6bE4), many image/speech synthesis tasks leverage [Adaptive Instance Normalization layer (AdaIN)](https://zhuanlan.zhihu.com/p/158657861) to calibrate the distribution of inputing data. But in object detection, there is not existing many works on low-resource learning and I only found two related papers ([SpotTune, *CVPR'19*, Citation=159](https://openaccess.thecvf.com/content_CVPR_2019/papers/Guo_SpotTune_Transfer_Learning_Through_Adaptive_Fine-Tuning_CVPR_2019_paper.pdf) and [Budget-Aware Adapters, *ICCV'19*, Citation=10](https://openaccess.thecvf.com/content_ICCV_2019/papers/Berriel_Budget-Aware_Adapters_for_Multi-Domain_Learning_ICCV_2019_paper.pdf)), which are not based on detection architectures and suitable for all CNN models.
    - [Domain adaptation and continual learning](#Domain-adaptation-and-continual-learning) - robustness and sustainability
      - For continual learning, most AI works focus on how to learn unseen classes and how to memory seen classes (avoid catastrophic forgetting). Thus, it is also named incremental learning.
      - For domain adaptation, AI researchers target to improve generalization of existing pretrained models. Based on given target data (labeled or unlabeled), existing algorithms can be split into two categories: (1) supervised retraining; (2) unsupervised domain adaptation (source-free and source-target-joint training).
      - Recent works about **Model Exchange & Serving** and **Model Monitoring & Updates** are summarized in this [slide](https://mboehm7.github.io/teaching/ss21_amls/12_ModelDeployment.pdf) provided by *Architecture of ML Systems* (SS2021, Graz University of Technology).
    - [Dynamic deep neural networks](#Dynamic-deep-neural-networks) - computing flexibility
- [Dataset](#Dataset) - test your ideas on popular datasets
- [Toolbox](#Toolbox) - verify your ideas quickly using toolbox
## Book and Survey
1. [Multi-Camera Networks: Principles and Applications. 2005.](https://dl.acm.org/citation.cfm?id=1643746)
2. [Camera Networks: The Acquisition and Analysis of Videos over Wide Areas (Synthesis Lectures on Computer Vision). 2012.](https://epdf.pub/camera-networks-the-acquisition-and-analysis-of-videos-overwide-areas.html)
3. [M.Valera et al. Intelligent distributed surveillance systems: a review. 2005.](https://pdfs.semanticscholar.org/ce96/43fbfcb9c3156c7b26b5c92ec3bc67111202.pdf)<br>
4. [Wang et al. Intelligent multi-camera video surveillance: a review. 2012.](https://dl.acm.org/citation.cfm?id=2397216)<br>
5. [Ye et al. Wireless Video Surveillance: A Survey. 2013.](https://www.researchgate.net/publication/270767766_Wireless_Video_Surveillance_A_Survey)<br>
6. [Zhang et al. Deep Learning in Mobile and Wireless Networking: A Survey. IEEE TRANS 2019.](https://arxiv.org/pdf/1803.04311.pdf)
## Researchers, Workshops and Courses
### Researchers (organization and research interests)
- System (live video analytics, distributed computing, video streaming, privacy, collaborative/continual learning)
  - [Matthias Boehm (Graz University of Technology, Austria)](https://mboehm7.github.io/#teaching) - data management and deep learning based data analytics
  - [Arun Kumar (University of California San Diego, USA)](https://cseweb.ucsd.edu//~arunkk/) - data management and deep learning based data analytics
  - [Ganesh Ananthanarayanan (Microsoft Research, USA)](https://www.microsoft.com/en-us/research/people/ga/) - live video analytics, distributed computing
  - [Yuanchao Shu (Microsoft Research, USA)](https://www.microsoft.com/en-us/research/people/yushu/) - live video analytics, collobarative/continual learning
  - [Feng Qian (University of Minnesota Twin Cities, USA)](https://www-users.cse.umn.edu/~fengqian/pub.html) - video streaming
  - [Juncheng Jiang (The University of Chicago, USA)](https://people.cs.uchicago.edu/~junchenj/) - video streaming
  - [Ravi Netravali (Princeton, USA)](https://www.cs.princeton.edu/~ravian/) - edge video AI
  - [Fengyuan Xu (Nanjing University, China)](https://cs.nju.edu.cn/fxu/) - the Internet of Video Things (IoVT) and **privacy-preserving edge AI**
  - [Shivaram Venkataraman (University of Wisconsin-Madison, USA)](https://shivaram.org/#pubs) - real-time video processing
- Deep based algorithms (tracking, object detection, segmentation and action recognition)
  - [Andrea Cavallaro (Queen Mary University of London, UK)](http://www.eecs.qmul.ac.uk/~andrea/) - multi-modal fusion, **privacy-aware video analytics (based on adversarial-training/learning)**
  - [Amit K. Roy-Chowdhury (UC Riverside, USA)](https://vcg.engr.ucr.edu/people/amit-roy-chowdhury) - tracking, reID, super-resolution and domain adaptation
  - [Jenq-Neng Hwang (University of Washington, USA)](https://people.ece.uw.edu/hwang/) - tracking, reID, localization and visual odometry
  - [Hamed Haddadi (Imperial College London, UK)](https://haddadi.github.io/about/) - **privacy-preserving edge AI**
  - [Ying Wu (Northwestern, USA)](http://users.eecs.northwestern.edu/~yingwu/) - tracking, detection, reID and segmentation
  - [Gaoang Wang (Zhejiang University, China)](https://www.vipazoo.cn/people/gaoangwang) - scene-aware multi-object tracking
  - [Haibin Ling (Stony Brook University, USA)](https://www3.cs.stonybrook.edu/~hling/) - visual tracking in drones
  - [Mubarak Shah (University of Central Florida, USA)](https://www.crcv.ucf.edu/person/mubarak-shah/) - zero/few-shot learning in video based tracking/segmentation/action recognition
  - [Ming-Hsuan Yang (UC Merced, USA)](https://faculty.ucmerced.edu/mhyang/) - low-resources (data or compute) learning for tracking/detection/segmentation
### Workshops (video analytics)
1. [The 3rd Workshop on Hot Topics in Video Analytics and Intelligent Edges (*ACM MobiCom'21*)](https://www.microsoft.com/en-us/research/event/the-3rd-workshop-on-hot-topics-in-video-analytics-and-intelligent-edges/#!call-for-papers) - focus on deep learning based video analytics
2. [Multi-camera Multiple People Tracking Workshop (*IEEE ICCV'21*)](https://iccv2021-mmp.github.io/) - track multiple people from indoor scenes using multiple RGB cameras
3. [Multimedia Systems Conference (*ACM MMSys'21*)](https://2021.acmmmsys.org/program.php#overview) - contain multiple topics in video analysis
<!-- 2. [Video Stream Analytics Reading List (Vrije Universiteit Amsterdam)](https://linwang.info/publications/) - general, edge-cloud hybrid, edge-based, cloud-based, privacy and camera virtualization.
3. [Literature of video streaming research (Stony Brook)](https://github.com/VideoForage/Video-Lit) - video streaming -->
### Courses
1. [CS294: Machine Learning Systems (Fall 2019, Berkeley)](https://ucbrise.github.io/cs294-ai-sys-fa19/) - contain all concepts/background behind machine learning systems (the best reference website!)
2. [706.550: Architecture of ML Systems (Summer 2021, Graz University of Technology)](https://mboehm7.github.io/teaching/ss21_amls/index.htm) - the architecture and essential concepts of modern ML systems for both local and large-scale machine learning (based on non-deep ML analytics)
3. [CS231A: Computer Vision, From 3D Reconstruction to Recognition (Winter 2021, Stanford)](https://web.stanford.edu/class/cs231a/) - focus on basic concepts behind many computer vision tasks across multi-camera networks (camera models, calibration, single- and multiple-view geometry, stereo systems, sfm, stereo, matching, depth estimation, optical flow and optimal estimation)
4. [CS239: ML-driven Video Analytics Systems (Fall 2020, UCLA)](http://web.cs.ucla.edu/~ravi/CS239_F20/index.html) - target to recent research interests on video analytics (_Strong Recommendation_)
5. [CS34702 Topics in Networks: Machine Learning for Networking and Systems (Fall 2020, UChicago)](https://people.cs.uchicago.edu/~junchenj/34702-f20/syllabus.html) - target to awesome recent research works on netwoking system (_video streaming and cloud scheduing_ are recommended)
6. [CSE 234: Data Systems for Machine Learning (Fall 2021, UCSD)](https://cseweb.ucsd.edu/classes/fa21/cse234-a/index.html) - focus on the lifecycle of ML-based data analytics, including data sourcing and preparation for ML, programming models and systems for scalable ML model building, and systems for faster ML deployment
## Topics
### System
#### Edge video analytics
[1] [Li et al. Reducto: On-Camera Filtering for Resource-Efficient Real-Time Video Analytics. In *SIGCOMM'20*.](https://dl.acm.org/doi/pdf/10.1145/3387514.3405874)<br>
[2] [Xu et al. Video Analytics with Zero-streaming Cameras. In *ATC'21*.](https://www.usenix.org/conference/atc21/presentation/xu)<br>
[3] [Jha et al. Visage: Enabling Timely Analytics for Drone Imagery. In *MobiCom'21*.](https://www.microsoft.com/en-us/research/publication/visage-enabling-timely-analytics-for-drone-imagery/)<br>
[4] [Jiang et al. Flexible High-resolution Object Detection on Edge Devices with Tunable Latency. In *MobiCom'21*.](https://dl.acm.org/doi/abs/10.1145/3447993.3483274)
#### Configuration search
[1] [Romero et al. Llama: A Heterogeneous & Serverless Framework for Auto-Tuning Video Analytics Pipelines. In *SoCC'21*.](http://web.stanford.edu/~faromero/llama.pdf)
#### Database
[1] [Saurez et al. A drop-in middleware for serializable DB clustering across geo-distributed sites. In VLDB'20.](https://dl.acm.org/doi/10.14778/3415478.3415555)
#### Video streaming
[1] [Y. Yan et al. Learning in situ: a randomized experiment in video streaming. In *NSDI'20*.](https://www.usenix.org/conference/nsdi20/presentation/yan)<br>
[2] [Kim et al. Neural-Enhanced Live Streaming: Improving Live Video Ingest via Online Learning. In *SIGCOMM'20*.](https://dl.acm.org/doi/abs/10.1145/3387514.3405856)<br>
[3] [Du et al. Server-Driven Video Streaming for Deep Learning Inference. In *SIGCOMM'20*.](https://dl.acm.org/doi/pdf/10.1145/3387514.3405887)<br>
[4] [Han et al. ViVo: Visibility-aware Mobile Volumetric Video Streamin. In *MobiCom'20*.](https://dl.acm.org/doi/10.1145/3372224.3380888)<br>
[5] [Zhang et al. SENSEI: Aligning Video Streaming Quality with Dynamic User Sensitivity. In *NSDI'21*.](https://www.usenix.org/conference/nsdi21/presentation/zhang-xu)<br>
#### Resource management
[1] [Zhang et al. The Design and Implementation of a Wireless Video Surveillance System. In *MobiCom'15*.](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/08/Bahl-MobiCom-2015.pdf)<br>
[2] [Xu et al. Approximate Query Service on Autonomous IoT Cameras. In *MobiSys'20*.](https://arxiv.org/pdf/1909.00841.pdf)<br>
[3] [Bhardwaj et al. Ekya: Continuous Learning of Video Analytics Models on Edge Compute Servers. In *NSDI'22*.](https://arxiv.org/abs/2012.10557) - target to solve when to retrain models and how to reduce resource usage for multi-tasks (many inference and retraining tasks). <br>
[4] [Zhou et al. Octo: INT8 Training with Loss-aware Compensation and Backward Quantization for Tiny On-device Learning. In *ATC'21*.](https://www.usenix.org/conference/atc21/presentation/zhou-qihua)
#### Prediction serving and model update
[1] [Suprem et al. ODIN: Automated Drift Detection and Recovery in Video Analytics. In *VLDB'21*.](http://www.vldb.org/pvldb/vol13/p2453-suprem.pdf) - target to detect domain drift and update corresponding models automatically. <br>
[2] [Romero et al. INFaaS: Automated Model-less Inference Serving. In *ATC'21*. **Best paper award!**](https://www.usenix.org/system/files/atc21-romero.pdf) - the first model-less prediction serving system <br>
[3] [Feng et al. Palleon: A Runtime System for Efficient Video Processing toward Dynamic Class Skew. In *ATC'21*.](https://www.usenix.org/conference/atc21/presentation/feng-boyuan) - model selection based on the automatically detected class skews<br>
[4] [Wang et al. SmartHarvest: Harvesting Idle CPUs Safely and Efficiently in the Cloud. In *EuroSys'21*.](https://dl.acm.org/doi/10.1145/3447786.3456225) - identify and harvest idle resources<br>
[5] [Gunasekaran et al. Cocktail: Leveraging Ensemble Learning for Optimized Model Serving in Public Cloud. In *NSDI'22*.](https://arxiv.org/abs/2106.05345) - expect to improve prediction serving's performance via ensembling learning<br>
[6] [Hu et al. Scrooge: A Cost-Effective Deep Learning Inference System. In *SoCC'21*.](https://dl.acm.org/doi/10.1145/3472883.3486993) - consider input complexity 
[7] [Ling et al. RT-mDL: Supporting Real-Time Mixed Deep Learning Tasks on Edge Platforms. In *SenSys'21*.](https://dl.acm.org/doi/10.1145/3485730.3485938) - scheduling multiple DL jobs in resource-constrainted devices
#### Multi-Camera Collaboration
[1] [Jain et al. Scaling Video Analytics Systems to Large Camera Deployments. In *HotMobile'19*.](https://rtcl.eecs.umich.edu/yuanchao/paper/hotmobile19video.pdf)<br>
[2] [Liu et al. Who2com: Collaborative Perception via Learnable Handshake Communication. In *ICRA'20*.](https://arxiv.org/abs/2003.09575)<br>
[3] [Liu et al. When2com: Multi-Agent Perception via Communication Graph Grouping. In *CVPR'20*.](http://openaccess.thecvf.com/content_CVPR_2020/papers/Liu_When2com_Multi-Agent_Perception_via_Communication_Graph_Grouping_CVPR_2020_paper.pdf)<br>
[4] [Tong et al. Large-Scale Vehicle Trajectory Reconstruction with Camera Sensing Network. In *MobiCom'21*.](https://wands.sg/publications/full_list/papers/MobiCom_21_1.pdf)
#### Privacy
|   Useful external links  | Keywords |
|  ----  | ---- |
| [Tutorial on privacy-preserving data analysis (The Alan Turing Institute)](https://www.turing.ac.uk/research/interest-groups/privacy-preserving-data-analysis)  | todo |
| [The Second AAAI Workshop on Privacy-Preserving Artificial Intelligence (PPAI-21)](https://ppai21.github.io/)  | todo |
| [A Dive into Privacy Preserving Machine Learning (OpML'20)](https://www.usenix.org/conference/opml20/presentation/pham) | todo |
| [CrypTen (Facebook AI Research)](https://github.com/facebookresearch/CrypTen) | Privacy Preserving Machine Learning framework, PyTorch, [Multi-Party Computation (MPC)](https://en.wikipedia.org/wiki/Secure_multi-party_computation) |

[1] [(TAMU and Adobe Research) Wu et al. Towards Privacy-Preserving Visual Recognition via Adversarial Training: A Pilot Study. In _ECCV'18_.](https://openaccess.thecvf.com/content_ECCV_2018/papers/Zhenyu_Wu_Towards_Privacy-Preserving_Visual_ECCV_2018_paper.pdf)<br>
[2] [(CMU) Wang et al. Enabling Live Video Analytics with a Scalable and Privacy-Aware Framework. In _2018 ACM Transactions on Multimedia Computing, Communications, and Applications (TOMM'18)_.](https://www.privacyassistant.org/media/publications/tomm2018.pdf)<br>
[3] [(KAIST, USTC, Rice, NJU, SNU, PKU and MSRA) Lee et al. Occlumency: Privacy-preserving Remote Deep-learning Inference Using SGX. In _MobiCom'19_.](https://dl.acm.org/doi/10.1145/3300061.3345447)<br>
[4] [(NUS) Shen et al. Human-imperceptible Privacy Protection Against Machines. In _MM'19_.](https://dl.acm.org/doi/10.1145/3343031.3350963)<br>
[5] [(PSU and Facebook) Khazbak et al. TargetFinder: Privacy Preserving Target Search through IoT Cameras. In _IoTDI'19_ (Best Paper Award).](http://mcn.cse.psu.edu/paper/youssef/iotdi-youssef19.pdf)<br>
[6] [(Tsinghua and USTC) Li et al. Invisible: Federated Learning over Non-Informative Intermediate Updates against Multimedia Privacy Leakages. In _MM'20_.](https://dl.acm.org/doi/abs/10.1145/3394171.3413923)<br>
[7] [(UCB and MSR) Poddar et al. Visor: Privacy-Preserving Video Analytics as a Cloud Service. In _29th	Usenix Security Symposium (Security'20)_.](https://www.usenix.org/conference/usenixsecurity20/presentation/poddar)<br>
[8] [(ICL, QMUL, Telefónica Research and Samsung AI) Mo et al. DarkneTZ: Towards Model Privacy at the Edge using Trusted Execution Environments. In _MobiSys'20_.](https://www.youtube.com/watch?v=mEAlONq3MU4)<br>
[9] [(NJU, Cornell and MSRA) Wu et al. PECAM: privacy-enhanced video streaming and analytics via securely-reversible transformation. In _MobiCom'21_.](https://dl.acm.org/doi/abs/10.1145/3447993.3448618)<br>
[10] [(ASU) Hu et al. LensCap: Split-Process Framework for Fine-Grained Visual Privacy Control for Augmented Reality Apps. In _MobiSys'21_.](https://dl.acm.org/doi/10.1145/3458864.3467676)<br>
[11] [(CUHK) Ouyang et al. ClusterFL: A Similarity-Aware Federated Learning System for Human Activity Recognition. In _MobiSys'21_.](https://dl.acm.org/doi/10.1145/3458864.3467681)<br>
[12] [(ICL and Telefónica Research) Mo et al. PPFL: Privacy-preserving Federated Learning with Trusted Execution Environments. In _MobiSys'21_ (Best paper award).](https://dl.acm.org/doi/10.1145/3458864.3466628)<br>
[13] [(CMU, UCSD and MSR) Dsouza et al. Amadeus: Scalable, Privacy-Preserving Live Video Analytics. _arXiv prePrint 2011.05163_.](https://arxiv.org/pdf/2011.05163.pdf)<br>
[14] [(MIT, Princeton, UChicago and Rutgers) Cangialosi et al. Privid: Practical, Privacy-Preserving Video Analytics Queries. In _NSDI'22_.](https://arxiv.org/pdf/2106.12083.pdf)<br>
### AI Algorithm
#### Low-resource learning
[1] [H. Aghdam et al. Active Learning for Deep Detection Neural Networks. In *ICCV'19*.](http://openaccess.thecvf.com/content_ICCV_2019/papers/Aghdam_Active_Learning_for_Deep_Detection_Neural_Networks_ICCV_2019_paper.pdf) [Public Code](https://gitlab.com/haghdam/deep_active_learning) [Note](https://github.com/YanLu-nyu/Awesome-Multi-Camera-Network/blob/master/Automatic_Labeling.md)
#### Domain adaptation and continual learning
xxx
#### Dynamic deep neural networks
xxx
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
3. [Cheetah](https://github.com/YanLu-nyu/Cheetah): an end-to-end deep learning based prediction serving server that speeds up deployment of image classification, object detection, segmentation and tracking techniques, which is based on NVIDIA Trition server and docker.
4. [Chameleon](https://github.com/YanLu-nyu/Chameleon): an efficient continuous adaptation framework based on NVIDIA TAO.
