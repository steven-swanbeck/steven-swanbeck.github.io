# Steven Swanbeck
![headshot](/assets/img/headshot-modified.png)
#### [LinkedIn](https://www.linkedin.com/in/stevenswanbeck/)
#### [GitHub](https://github.com/steven-swanbeck)
#### Technical Skills: ROS, C++, Python, Machine Learning (Scikit-Learn, TensorFlow, PyTorch), MATLAB, CAD (SOLIDWORKS & similar, GD&T), OpenCV, Point Cloud Library, MoveIt
---
## About
I am a graduate student in the [Nuclear and Applied Robotics Group](https://robotics.me.utexas.edu/) (NRG) advised by [Dr. Mitch Pryor](https://www.me.utexas.edu/people/faculty-directory/pryor) at The University of Texas at Austin.

Prior to joining NRG, I completed my undergraduate studies in mechanical engineering at the University of Nevada, Reno and worked in the [Smart Robotics Lab](https://packpages.unr.edu/jun) under the guidance of [Dr. Jun Zhang](https://www.unr.edu/me/about/people/jun-zhang).

## Education
- M.S. Robotics, The University of Texas at Austin
- B.S. Mechanical Engineering, University of Nevada, Reno

## Selected Work Experience
**Graduate Research Assistant @ Nuclear & Applied Robotics Group (_August 2022 - Present_)**
- Autonomous inspection, maintenance, and repair tasks for deployment into hazardous environments

**Undergraduate Research Assistant @ Smart Robotics Lab (_August 2021 - August 2022_)**
- Design, modeling, and control of novel soft-robotic grippers to improve safety of human-robot interaction

**Electro-Mechanical Engineering Intern @ Hamilton Company (_June 2021 - August 2021_)**

---
## Selected Projects

### Augmented-Reality Integration for Aiding and Altering Robot Insepction and Maintenance Tasks (_July 2023 - Present_)
- By using augmented reality user interfaces, a human supervisor is able to accept, reject, or modify autonomous detections made by an independently operating robotic system.
- This is useful for making sure the robot does not incidentally coat sensitive material, such as gauges or valves, or spend time repairing material that was falsely identified and not actually in need of repair.
- The use of augmented reality allows the user to see exactly what the robot intends to repair and how it will do so _in situ_, and visualized markers help the user guide the robot into its calculated desired position to perform a repair.
{% include youtube.html id="rlCdHOC1ifg" %}

### Non-Contact Surface Coverage for Repair of Corroded Material (_May 2023 - Present_)
- Autonomous detection of corroded material within the environment using fused sensor measurements informs which surfaces are in need of repair.
- The geometries of these surfaces are reconstructed using the collected sensor data and used to develop a series of virtual fixtures offset from the surface at which a spray coating can be applied to coat the target surface, arresting the development of further decay.
- Using the perceived environment geometry and manipulability of the system, virtual fixtures are compliantly replanned until successful to enable surface coverage given these constraints.
- Predictions about which material to repair can be made autonomously using custom-trained detection models or made directly by a human supervisor using the [labelme](https://github.com/wkentaro/labelme) image labeling tool to create polygons around material to coat which are used in real time to generate plans to repair the marked material. Because labels are generated in the labelme format, this allows a training dataset to be constructed over time which can be used to train increasingly accurate ML models for autonomous detections.
![Survey](/assets/img/caught_in_the_act.png)
![Repair](/assets/img/caught_in_the_act_the_finale.png)
{% include youtube.html id="wLi5IyUC0lg" %}
{% include youtube.html id="H9DwXMYC1yQ" %}
{% include youtube.html id="hxRTpih4y6U" %}

### ML-Ops Pipeline for Rapidly Training and Deploying Models Using Point Cloud Data (_February 2023 - April 2023_)
- Using raw input LiDAR data, point clouds can be registered together and combined to create larger, unified maps of a space.
- This data can be colored using various strategies to aid visualization, and then labeled using the [labelCloud](https://github.com/ch-sa/labelCloud) point cloud labeling tool.
- Each cloud, with labels corresponding to different object and material types, are read in and the points associated with each label are extracted and combined accordingly into a labeled dataset.
- This generated dataset can be used to rapidly train machine learning models of various types, including logistic regression, state-vector machines, gradient-boosted trees, and arbitrarily complex ANN and RNN architectures.
- Trained models are saved and indexed for future use and a detailed printout describing the model type, architecture and features, characteristics of the data from which the model was trained, and its performance on the validation data split is generated.
- Saved models can be easily deployed to make predictions on and reconstruct new point cloud data, and can be queried as a ROS service for real-time predictions.
![pipeline example](/assets/img/labeling_pipeline_example.png)
![model printout](/assets/img/model_printout.png)

### Hardware-Agnostic 3D Dense Mapping Stack (_October 2022 - January 2023_)
- Using LiDAR and image data collected passively while navigating an environment, dense colored 3D maps can be generated that accurately reflect the geometries and appearances of the objects within them.
- Point clouds are colored with associated image data using projection strategies and are registered together for maximum fidelity.
- Generated maps can be traversed by a human user to assess the condition of material within the environment and assess the accuracy of autonomous predictions made by the robot during survey, if applicable.
![Facility Map](/assets/img/map2.png)
![facility map colored](/assets/img/map3.png)

### Robotic Calculator and Game-Player (_September 2022 - November 2022_)
- A calculator program written to perform basic arithmetic and perform mathematical order of operations is given an arm with which it can write the result of its calculations using a pen rather than simply printing the result to terminal.
- Similarly, the same arm given the ability to participate in a modified version of the classic "shell game" street scam, in which a participant is instructed to place money under one of three shells then mix them around and attempt to trick the robot into picking an incorrect shell under which there is no money. If the participant can fool the robot, they win the money, but if not, the game operator does.
- Using computer vision, the robot is able to search for a marker discretely placed on one of the shells to determine which shell has the money.
{% include youtube.html id="VsOunJDqvBQ" %}
{% include youtube.html id="34CjPUCyPaU" %}
{% include youtube.html id="NgUwk--LVM8" %}

### Anthropomorphic Soft Robotic Gripper (_August 2021 - June 2023_)
- Grippers designed to mimic the dexterity and grasping capabilities of the human hand using soft materials and novel actuation mechanisms.
- Twisted-string actuators (TSAs) used to generate high force, muscle-like linear actuation using tendons with low input power and motor torques.
- Original gripper system was able to execute almost all grasps within the human grasp taxonomy and could lift almost 13 times its own weight.
- Subsequent versions the gripper featured a higher number of actuators to improve dexterity and enable in-hand manipulations.
- The grippers were attached to a robotic manipulator and software packages written to coordinate their actions, enabling higher-level autonomous environmental manipulation tasks.
- The gripper was shared with NASA's Dexterous Robotics Team at Johnson Space Center in Houston and temporarily attached to their Valkyrie humanoid robot.
![SoftGripper](/assets/img/soft_gripper.jpg)
{% include youtube.html id="PzI-jFkVfLc" %}
{% include youtube.html id="ODOsu-wWiis" %}
![Valkyrie](/assets/img/gripperonValkyrie.jpg)

### Sublunar Exploration Quadruped (_March 2021 - January 2022_)
- NASA University Student Design Challenge to create an autonomous system capable of exploring evacuated subsurface lava tubes on the moon to assess their ability to sustain long-term human habitation.
- A custom quadrupedal system was designed that is capable of walking in any direction and collecting LiDAR data to construct 3D maps of its environments.
- The prototype features PID-based self-stabilization and adjustable gait parameters, plus a remote control setting to allow a user to walk it around.
![Quadruped](/assets/img/seq_standing.png)
{% include youtube.html id="LHgbjfePTno" %}
{% include youtube.html id="Oor5UM_UCEk" %}
{% include youtube.html id="YJJ4hOkALdQ" %}

---
## Publications
1. R. Konda\*, D. Bombara\*, S. Swanbeck\*, and J. Zhang, "Anthropomorphic twisted string actuated soft robotic gripper with tendon-based stiffening," IEEE Transactions on Robotics, vol. 39, no. 2, pp. 1178-1195, 2023 (*equal contribution).
2. A. Baker, C. Foy, S. Swanbeck, R. Konda and J. Zhang, "STAR–2: A Soft Twisted-string-actuated Anthropomorphic Robotic Gripper: Design, Fabrication, and Preliminary Testing," 2023 IEEE/ASME International Conference on Advanced Intelligent Mechatronics (AIM), Seattle, WA, USA, 2023, pp. 643-648.
3. S. Swanbeck, R. Konda, and J. Zhang, "Kinematic Modeling of a Twisted-String Actuated Soft Robotic Finger as Part of an Anthropomorphic Gripper," 2023 Modeling, Estimation and Control Conference (MECC), Lake Tahoe, NV, USA, 2023.
