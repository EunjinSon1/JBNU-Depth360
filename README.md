# JBNU-Depth360
<p align="center"><img src = "![JBNU_Depth360](https://github.com/EunjinSon1/JBNU-Depth360/assets/139856699/0ba8490a-5cb7-445e-b183-8aa52b7999b3)
" width="30%" height="30%"></p>


we propose a novel fisheye dataset for depth estimation, named JBNU-Depth360, designed for underground parking lot environments. 
For the data collection, we construct a mobile robot, utilizing AGX Xavier and Jackal UGV as the foundational components. 
Specifically, the mobile robot is equipped with four 183˚ Fisheye M12 lenses, positioned in the front, rear, left, and right directions, respectively.
Additionally, a LiDAR sensor, Ouster GEN2 OS-0-32, is centrally located on the robot. Subsequently, to align the LiDAR point cloud with the RGB image, a calibration process is performed by utilizing a checkerboard to calibrate the front camera and the LiDAR system. 

The JBNU-Depth360 dataset is obtained within the underground parking lot located at Jeonbuk National University in Korea.
Specifically, the mobile robot collects data by starting its trajectory from the entrance of the parking lot, moving along the interior, and returning to the initial starting point. The dataset comprises 4,221 RGB images captured by a front camera, with a resolution of 1080 × 1920 pixels, and the corresponding LiDAR points.

You can download the JBNU-Depth360 data in [[GoogleDrive](https://drive.google.com/file/d/1Tpgy-Qk-vNhiHMza9vO8qH3xyn9B4n_O/view?usp=drive_link)]



# Floder Structure
Our dataset is divided into 6 individual sequences, each corresponding to a continuous driving trajectory. 
The full dataset comprises RGB images and LiDAR point clouds, which are structured as follows: The sequence ID is denoted by {seq:0>1}, using a single digit, and the frame ID is denoted by {seq:0>6}, using 6 digits. 

```bash
└── 230329
    └── test_{seq:0>1}
        ├── bin
        │   └── {frame:0>6}.bin
        └── image
            └── {frame:0>6}.png
```


# Sensor Locations
<p align="center"><img src = "https://github.com/EunjinSon1/JBNU-Depth360/assets/139856699/0fcb94fe-d575-442f-82a6-f8eb24c5f7b1" width="30%" height="30%"></p>
