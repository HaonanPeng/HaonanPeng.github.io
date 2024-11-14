---
title: "Research"
permalink: /research/
classes: wide
---

## Sensorless Contact Force Estiamtion

This is an ongoing project, which aim to utilize AI and data-driven models to estimate the contact force based on the original robot states, without any extra sensors. In order to collect training data of the robot states under external froce with different directions and amplitude, a cable-driven parallal robotics force actuation system is developed, which can apply force to robot arms while passively following the movement of the robot arm.

<iframe src="https://drive.google.com/file/d/1vR_DdvScEdm9MZkkixAmRlco93jXZdes/preview" width="640" height="480" allow="autoplay" allowfullscreen></iframe>  
*Video: Force actuation on RAVEN-II surgical Robot*

![Force Unit](/assets/images/force_unit.png)   
*Fig.1. Force actuation unit*

## Efficient Positional Calibration for Cable-driven Surgical Robot

[GitHub](https://github.com/HaonanPeng/Efficient-Data-driven-Joint-level-Calibration-of-Cable-driven-Surgical-Robots)   

Cable-driven laparoscopic surgical robots such as RAVEN-II have flexible, light, and compact arms and tools. However, due to the difficulty and cost of joint encoder installation, the estimation of joint positions derived from motor encoders is inaccurate because of cable effects. I developed AI-based data-driven calibration models that can further reduce 76% of error. The calibration only takes less than 21 minute and remains sub-mm/deg accuracy in 6 hour continuous operating.

![raven_cable](/assets/images/raven_cable.png)   
*Fig.2. Cable connection and coupling of the RAVEN-II*

![calibration_workflow](/assets/images/calibration_workflow.png)   
*Fig.3. Calibration Workflow*

## Feature Ablation Study on Learning-based Calibration

Although AI calibrations can significantly improve the control accuracy of the surgical robots, having all features in the robot states as the model inputs requires more training data and computational power. Aiming to improve the efficiency and explainability, I developed removal and inaccurate ablation studies on input features identify that raw joint positions and motor torques are the most important model inputs for calibration accuracy. Further specific ablations also give inspirations on how AI models utilize these input information. By excluding the unnecessary input features, lightweight models are developed and achieve better performance and efficiency simultaneously, reducing the training time on CPU to 2.5 minutes.

![raven_state](/assets/images/ravenstate.png)   
*Fig.4. The feature in the robot state and their relations*

## Active Learning Guided Generation of Synthetic Endoscopic Images

Supervised deep learning usually requires a large amount of labeled data to achieve accurate prediction, which poses a significant human workload, especially for medical images. To alleviate this workload, we developed an active learning framework to generate synthetic images for efficient neural network training. In each active learning iteration, a small number of informative unlabeled images are first queried by active learning and manually labeled. Next, synthetic images are generated based on these selected images to make the best use of them. This method leverages the advantage of both active learning and synthetic images. The effectiveness of the method is validated on two sinus surgery datasets and one intraabdominal surgery dataset. The results indicate a considerable performance improvement, especially when the size of the annotated dataset is small.

![calibration_workflow](/assets/images/fig2_workflow_n5.jpg)   
*Fig.5. Generation workflow of synthetic endoscopic images*

![calibration_workflow](/assets/images/fig5_example_syn.png)   
*Fig.6. Examples of generated images*