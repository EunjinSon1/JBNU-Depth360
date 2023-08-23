# JBNU-Depth360

<p align="center"><img src = "https://github.com/EunjinSon1/JBNU-Depth360/assets/139856699/9c19ff6b-532e-4b3f-bd18-bd138c65b0c4" width="40%" height="40%"></p>

We propose a novel fisheye dataset for depth estimation, named JBNU-Depth360, designed for underground parking lot environments. 
For the data collection, we construct a mobile robot, utilizing AGX Xavier and Jackal UGV as the foundational components. 
Specifically, the mobile robot is equipped with four NileCAM21 cameras, each of which is outfitted with a 183˚ Fisheye M12 lens. These cameras are strategically placed to capture views in the front, rear, left, and right directions, respectively. Additionally, a LiDAR sensor, the Ouster GEN2 OS-0-32, is centrally positioned on the robot. Subsequently, a calibration process is executed to achieve alignment between the LiDAR point cloud and the RGB image. This calibration procedure involves utilizing a checkerboard pattern to calibrate both the front camera and the LiDAR system, ensuring accurate spatial correspondence between the captured RGB images and the corresponding LiDAR data.

The JBNU-Depth360 dataset is obtained within the underground parking lot located at Jeonbuk National University in Korea.
Specifically, the mobile robot collects data by starting its trajectory from the entrance of the parking lot, moving along the interior, and returning to the initial starting point. The dataset comprises 4,221 RGB images captured by a front camera, each with a resolution of 1080 × 1920 pixels, and their corresponding LiDAR points. To protect privacy, the RGB images anonymized.

You can download the JBNU-Depth360 data in [[GoogleDrive](https://drive.google.com/drive/u/3/my-drive)]


# Folder Structure
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
<p align="center"><img src = "https://github.com/EunjinSon1/JBNU-Depth360/assets/139856699/99a2cf29-f66b-4b9f-be49-e7fe1c729754" width="30%" height="30%"></p>
