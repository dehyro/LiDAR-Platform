# LiDAR-Platform
LiDAR platform for the extraction of morphological data from maize seedlings 


## Hardware requirements:

- LiDAR LMS4000
- MS Kinect v1
- Logitech Brio
- Arduino nano
- Step by step driver "EasyDriver V44 A3967"
- 12VDC stepper motor

## Software Requirements:

- Ubuntu 18.04
- Python 3.6
- Ros Melodic
- OpenCV
- Open3D
- PlantCV
- PyntCloud
- Arduino IDLE

## Required Folders, files and packages:

```bash
/root/user/                              # working path

|-- arduino/                             # Arduino folder
    |-- arduino.ino                      # arduino control code
|-- catkin_ws/                           # Workspace for Kinect v1
    |-- src/
        |-- freenect_stack/              # ros driver for Kinect v1
        |-- rgbd_launch/                 # ros driver for Kinect v1
|-- cvbridge_build_ws/                   # workspace for CVBridge library
    |-- bag_files/                       # folder to store .BAG files generated
    |-- calib.py                         # calibration code for platform
    |-- camera.py                        # image camera capture
    |-- clouds/                          # folder to store data: point clouds and images
        |-- Color_Img/                   # folder to store color calibration images
    |-- data.txt                         # store GUI variables
    |-- data_init.txt                    # store calibration data
    |-- initial.py                       # call for calib.py, create folders to store data and save calibration data in data_init.txt
    |-- scan/                            # folder to store calibration clouds
    |-- scanner.py                       # execute plant scanning, create point clouds (.TXT), images, and .BAG files 
|-- gui_ws/                              # workspace for GUI
    |-- src
        |-- tutorial_kivy                # package for running KivyMD GUI
            |-- gradient.png             # image for GUI background
            |-- gradient_2.png           # image for GUI background
            |-- omicas.png               # omicas project logo for GUI
            |-- ros_gui.kv               # kivy code to configure GUI
            |-- scripts/
                |-- simple_gui.py        # Launch of GUI with KivyMD for starting ROS nodes of platform and data collection
            |-- unibague_icon.png        # University of Ibagué logo for GUI
|-- kivy_venv/                           # Kivy virtual environment
|-- libfreenect/                         # official kinect package 
|-- s01_seedlings/                       # first sowing of seedlings
    |-- images/                          
    |-- img_results/
        |-- filters/
        |-- morph/
        |-- skel/
    |-- pcd_results/
        |-- ML/
    |-- point_clouds/
        |-- segmented/
    |-- s01_img_seg_part1.py             # first part of image segmentation for first sowing of seedlings
    |-- s01_img_seg_part2.py             # second part of image segmentation for first sowing of seedlings
    |-- s01_pcd_seg.py                   # point cloud segmentation for first sowing of seedlings
    |-- s01_ml_seg_part1.py              # first part of machine learning application on segmented point clouds
    |-- s01_ml_seg_part2.py              # second part of machine learning application on segmented point clouds
|-- s02_seedlings/                       # second sowing of seedlings
    |-- images/
    |-- img_results/
    |-- pcd_results/
        |-- mesh
    |-- point_clouds/
    |-- s02_img_seg.py                   # image segmentation for second sowing of seedlings
    |-- s02_pcd_seg.py                   # point cloud segmentation for second sowing of seedlings
    
```
## How to Use

