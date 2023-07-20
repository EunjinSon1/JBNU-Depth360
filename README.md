# JBNU-Depth360

Accurate depth estimation is important in various scenarios, including both road driving and parking. 
This significance becomes pronounced within parking environments, which are characterized by the close proximity to adjacent vehicles and the presence of blind spots, such as the rear of the vehicle. However, the existing datasets for depth estimation are primarily concentrated on road driving scenarios. 
Therefore, it is not clear whether the models learned from these datasets perform well in parking environments. 

Hence, we propose a novel fisheye dataset for depth estimation, named JBNU-Depth360, designed for underground parking lot environments. 
For the data collection, we construct a mobile robot, utilizing AGX Xavier and Jackal UGV as the foundational components. 
Specifically, the mobile robot is equipped with four $183^{\circ}$ Fisheye M12 lenses, positioned in the front, rear, left, and right directions, respectively.
Additionally, a LiDAR sensor, Ouster GEN2 OS-0-32, is centrally located on the robot. Subsequently, to align the LiDAR point cloud with the RGB image, a calibration process is performed by utilizing a checkerboard to calibrate the front camera and the LiDAR system. 

The JBNU-Depth360 dataset is obtained within the underground parking lot located at Jeonbuk National University in Korea.
Specifically, the mobile robot collects data by starting its trajectory from the entrance of the parking lot, moving along the interior, and returning to the initial starting point. The dataset comprises 4,221 RGB images captured by a front camera, with a resolution of 1080x1920 pixels, and the corresponding LiDAR points. For the experiment, we obtain depth maps with the same resolution as the RGB images by projecting 3D LiDAR points onto a 2D plane.

You can download the JBNU-Depth360 data in [Google Drive]([link](https://drive.google.com/file/d/1Tpgy-Qk-vNhiHMza9vO8qH3xyn9B4n_O/view?usp=drive_link))



# Floder Structure
Our dataset is devided into 6 individual sequences, each corresponding to a continuous driving trajectory. 
The full dataset including RGB image, LiDAR point cloud as follows, where {seq:0>1} denotes the sequence ID using 1 digits and {frame:0>10} denotes the frame ID using 6 digits.

```bash
└── 230329
    └── test_{seq:0>1}
        ├── bin
        │   └── {frame:0>6}.bin
        └── image
            └── {frame:0>6}.png
```



# Sensor Locations
![robot_full2](https://github.com/EunjinSon1/JBNU-Depth360/assets/139856699/1e1a4baa-de43-4f83-b795-f44e4b544632){: width="300" height="300"){: .center}

