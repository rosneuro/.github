# ROS-Neuro: An Open-Source Platform for Neurorobotics

**ROS-Neuro** has been designed to represent the first open-source neurorobotic middleware that places human neural interfaces and robotic systems at the same conceptual and implementation level. **ROS-Neuro** is an extension of ROS that for many years is considered the standard platform for robotics. One of the strengths of ROS is its modularity and the possibility for different research groups to develop stand-alone components all relying on the same standard communication infrastructure. A similar requirement is a cornerstone for the workflow of any closed-loop neural interface where—for instance—acquisition, processing, and decoding methods should run in parallel in order to provide a continuous/discrete control signal to drive the robotic device. 

![alt text](https://raw.githubusercontent.com/rosneuro/.github/main/profile/rosneuro_schema.jpg)

## ROS-Neuro packages

Currently, **ROS-Neuro** provides the following packages:

### rosneuro_msgs
Standard ROS messages in **ROS-Neuro** framework
- [rosneuro/rosneuro_msgs](https://github.com/rosneuro/rosneuro_msgs) 

### rosneuro_data
Data structures in **ROS-Neuro** framework
- [rosneuro/rosneuro_data](https://github.com/rosneuro/rosneuro_data) 

### rosneuro_acquisition
Generic interface for acquiring data from different devices
- [rosneuro/rosneuro_acquisition](https://github.com/rosneuro/rosneuro_acquisition) 

### rosneuro_acquisition_plugins
Official plugins for rosneuro_acquisition
- [rosneuro/rosneuro_acquisition_plugins](https://github.com/rosneuro/rosneuro_acquisition_plugins) 

### rosneuro_recorder
Generic interface for recording neuro data
- [rosneuro/rosneuro_recorder](https://github.com/rosneuro/rosneuro_recorder) 

### rosneuro_visualizer
Scope for EEG and EMG data
- [rosneuro/rosneuro_visualizer](https://github.com/rosneuro/rosneuro_visualizer) 

### rosneuro_buffers
Generic buffers for neuro data
- [rosneuro/rosneuro_buffers](https://github.com/rosneuro/rosneuro_buffers) 

### rosneuro_filters
Generic filters for neuro data
- [rosneuro/rosneuro_filters](https://github.com/rosneuro/rosneuro_filters) 

## Installation
The favorite method to install *ROS-Neuro* is from source by cloning all the available packages in the same workspace and by using `catkin_make install` to install them in the system. However, release 1.0.0 provides also the debian packages to install the different packages. The available debian packages are:
- [ros-noetic-rosneuro-msgs_1.0.0-0focal_amd64.deb](https://github.com/rosneuro/rosneuro_msgs/releases/download/v1.0.0/ros-noetic-rosneuro-msgs_1.0.0-0focal_amd64.deb)
- [ros-noetic-rosneuro-data_1.0.0-0focal_amd64.deb](https://github.com/rosneuro/rosneuro_data/releases/download/v1.0.0/ros-noetic-rosneuro-data_1.0.0-0focal_amd64.deb)
- [ros-noetic-rosneuro-acquisition_1.0.0-0focal_amd64.deb](https://github.com/rosneuro/rosneuro_acquisition/releases/download/v1.0.0/ros-noetic-rosneuro-acquisition_1.0.0-0focal_amd64.deb)
- [ros-noetic-rosneuro-acquisition-eegdev_1.0.0-0focal_amd64.deb](https://github.com/rosneuro/rosneuro_acquisition_plugins/releases/download/v1.0.0/ros-noetic-rosneuro-acquisition-eegdev_1.0.0-0focal_amd64.deb)
- [ros-noetic-rosneuro-recorder_1.0.0-0focal_amd64.deb](https://github.com/rosneuro/rosneuro_recorder/releases/download/v1.0.0/ros-noetic-rosneuro-recorder_1.0.0-0focal_amd64.deb)
- [ros-noetic-rosneuro-visualizer_1.0.0-0focal_amd64.deb](https://github.com/rosneuro/rosneuro_visualizer/releases/download/v1.0.0/ros-noetic-rosneuro-visualizer_1.0.0-0focal_amd64.deb)
- [ros-noetic-rosneuro-buffers_1.0.0-0focal_amd64.deb](https://github.com/rosneuro/rosneuro_buffers/releases/download/v1.0.0/ros-noetic-rosneuro-buffers_1.0.0-0focal_amd64.deb)
- [ros-noetic-rosneuro-filters_1.0.0-0focal_amd64.deb](https://github.com/rosneuro/rosneuro_filters/releases/download/v1.0.0/ros-noetic-rosneuro-filters_1.0.0-0focal_amd64.deb)

## References:
- Tonin L, Beraldo G, Tortora S, Menegatti E (2022) ROS-Neuro: An Open-Source Platform for Neurorobotics. Front. Neurorobot. 16:886050. doi: 10.3389/fnbot.2022.886050
- Tonin L, Beraldo G, Tortora S, Tagliapietra L, Millàn JdR et al. (2019). ROS-Neuro: A common middleware for BMI and robotics. The acquisition and recorder packages, in Proc of 2019 IEEE International Conference on Systems, Man and Cybernetics (SMC), 2767–2772
- Beraldo G, Tortora S, Menegatti E, Tonin L. (2020). ROS-Neuro: Implementation of a closed-loop BMI based on motor imagery, in Proc of 2020 IEEE International Conference on Systems, Man, and Cybernetics (SMC), 2031–2037
