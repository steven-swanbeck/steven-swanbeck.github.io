# Steven Swanbeck

#### Technical Skills: ROS, C++, Python, Machine Learning (Scikit-Learn, TensorFlow, PyTorch), MATLAB, CAD (SOLIDWORKS & similar, GD&T), OpenCV, Point Cloud Library, MoveIt

---
## Education
- M.S. Robotics, The University of Texas at Austin
- B.S. Mechanical Engineering, University of Nevada, Reno

## Relevant Work Experience
**Graduate Research Assistant @ Nuclear & Applied Robotics Group (_August 2022 - Present_)**
- Autonomous inspection, maintenance, and repair tasks for deployment into hazardous environments

**Undergraduate Research Assistant @ Smart Robotics Lab (_August 2021 - August 2022_)**
- Design, modeling, and control of novel soft-robotic grippers to improve safety of human-robot interaction

**Electro-Mechanical Engineering Intern @ Hamilton Company (_June 2021 - August 2021_)**

---
## Projects

### Augmented-Reality Integration for Aiding and Altering Robot Insepction and Maintenance Tasks
- By using augmented reality user interfaces, a human supervisor is able to accept, reject, or modify autonomous detections made by an independently operating robotic system.
- This is useful for making sure the robot does not incidentally coat sensitive material, such as gauges or valves, or spend time repairing material that was falsely identified and not actually in need of repair.
- The use of augmented reality allows the user to see exactly what the robot intends to repair and how it will do so _in situ_, and visualized markers help the user guide the robot into its calculated desired position to perform a repair.
{% include youtube.html id="rlCdHOC1ifg" %}

### Non-Contact Surface Coverage for Repair of Corroded Material
- Autonomous detection of corroded material within the environment using fused sensor measurements informs which surfaces are in need of repair.
- The geometries of these surfaces are reconstructed using the collected sensor data and used to develop a series of virtual fixtures offset from the surface at which a spray coating can be applied to coat the target surface, arresting the development of further decay.
- Using the perceived environment geometry and manipulability of the system, virtual fixtures are compliantly replanned until successful to enable surface coverage given these constraints.
- Predictions about which material to repair can be made autonomously using custom-trained detection models or made directly by a human supervisor using the [labelme](https://github.com/wkentaro/labelme) image labeling tool to create polygons around material to coat which are used in real time to generate plans to repair the marked material. Because labels are generated in the labelme format, this allows a training dataset to be constructed over time which can be used to train increasingly accurate ML models for autonomous detections.

### ML-Ops Pipeline for Rapidly Training and Deploying Models Using Point Cloud Data
- Using raw input LiDAR data, point clouds can be registered together and combined to create larger, unified maps of a space.
- This data can be colored using various strategies to aid visualization, and then labeled using the [labelCloud](https://github.com/ch-sa/labelCloud) point cloud labeling tool.
- Each cloud, with labels corresponding to different object and material types, are read in and the points associated with each label are extracted and combined accordingly into a labeled dataset.
- This generated dataset can be used to rapidly train machine learning models of various types, including logistic regression, state-vector machines, gradient-boosted trees, and arbitrarily complex ANN and RNN architectures.
- Trained models are saved and indexed for future use and a detailed printout describing the model type, architecture and features, characteristics of the data from which the model was trained, and its performance on the validation data split is generated.
- Saved models can be easily deployed to make predictions on and reconstruct new point cloud data, and can be queried as a ROS service for real-time predictions.

### Hardware-Agnostic 3D Dense Mapping Stack
- Using LiDAR and image data collected passively while navigating an environment, dense colored 3D maps can be generated that accurately reflect the geometries and appearances of the objects within them.
- Point clouds are colored with associated image data using projection strategies and are registered together for maximum fidelity.
- Generated maps can be traversed by a human user to assess the condition of material within the environment and assess the accuracy of autonomous predictions made by the robot during survey, if applicable.

### Robotic Calculator and Game-Player
- A calculator program written to perform basic arithmetic and perform mathematical order of operations is given an arm with which it can write the result of its calculations using a pen rather than simply printing the result to terminal.
- Similarly, the same arm given the ability to participate in a modified version of the classic "shell game" street scam, in which a participant is instructed to place money under one of three shells then mix them around and attempt to trick the robot into picking an incorrect shell under which there is no money. If the participant can fool the robot, they win the money, but if not, the game operator does.
- Using computer vision, the robot is able to search for a marker discretely placed on one of the shells to determine which shell has the money.

### Anthropomorphic Soft Robotic Gripper
- 

### Sublunar Exploration Quadruped


---
## Publications
1. R. Konda\*, D. Bombara\*, S. Swanbeck\*, and J. Zhang, "Anthropomorphic twisted string actuated soft robotic gripper with tendon-based stiffening," IEEE Transactions on Robotics, vol. 39, no. 2, pp. 1178-1195, 2023 (*equal contribution).
2. A. Baker, C. Foy, S. Swanbeck, R. Konda and J. Zhang, "STAR–2: A Soft Twisted-string-actuated Anthropomorphic Robotic Gripper: Design, Fabrication, and Preliminary Testing," 2023 IEEE/ASME International Conference on Advanced Intelligent Mechatronics (AIM), Seattle, WA, USA, 2023, pp. 643-648.
3. S. Swanbeck, R. Konda, and J. Zhang, "Kinematic Modeling of a Twisted-String Actuated Soft Robotic Finger as Part of an Anthropomorphic Gripper," 2023 Modeling, Estimation and Control Conference (MECC), Lake Tahoe, NV, USA, 2023.
