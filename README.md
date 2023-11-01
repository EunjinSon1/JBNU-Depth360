# JBNU-Depth360

<p align="center"><img src = "https://github.com/EunjinSon1/JBNU-Depth360/assets/139856699/9c19ff6b-532e-4b3f-bd18-bd138c65b0c4" width="40%" height="40%"></p>

We propose a novel fisheye dataset for depth estimation, named JBNU-Depth360, designed for underground parking lot environments. The JBNU-Depth360 dataset was acquired from underground parking lot environments located in Jeonbuk National University, South Korea. The dataset comprises 4,221 RGB images captured by a front camera, each with a resolution of 1080 × 1920 pixels, and their corresponding LiDAR points. To protect privacy, the RGB images anonymized.

You can download the JBNU-Depth360 data in [[GoogleDrive](https://drive.google.com/file/d/1jrqScsIgzD7-e0BHgZKsgJDrVQ1IzFSW/view?usp=drive_link)]


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


# Sensor configuration
<p align="center"><img src = "https://github.com/EunjinSon1/JBNU-Depth360/assets/139856699/55e65384-9f0e-4c02-8257-f519a01a76d9" width="70%" height="70%"></p>

The sensor configuration (left, middle) and top-view image (right) of the mobile robot used to collect the JBNU-Depth dataset. The robot is equipped with AGX Xavier on a Jackal UGV. Additionally, the LiDAR sensor, Ouster GEN2 OS-0-32, is located atop the center of the robot (as denoted by the red circle in the top-view image), and four NileCAM21 cameras with a 183-degree Fisheye M12 lens are positioned in the front, rear, left, and right directions of the robot (as denoted by the blue circle in the top-view image).



