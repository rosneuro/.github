# ROS-Neuro: An Open-Source Platform for Neurorobotics

**ROS-Neuro** has been designed to represent the first open-source neurorobotic middleware that places human neural interfaces and robotic systems at the same conceptual and implementation level. **ROS-Neuro** is an extension of ROS that for many years is considered the standard platform for robotics. One of the strengths of ROS is its modularity and the possibility for different research groups to develop stand-alone components all relying on the same standard communication infrastructure. A similar requirement is a cornerstone for the workflow of any closed-loop neural interface where—for instance—acquisition, processing, and decoding methods should run in parallel in order to provide a continuous/discrete control signal to drive the robotic device. 

![alt text](https://raw.githubusercontent.com/rosneuro/.github/main/profile/rosneuro_schema.jpg)

---

## 1. Installation of ROS-Neuro

### 1.1 Setup your source list
Setup your computer to accept software from rosneuro.github.io.

```
sudo curl -s --compressed -o /etc/apt/sources.list.d/rosneuro.list "https://rosneuro.github.io/ppa/ubuntu/rosneuro.list"
```

### 1.2 Setup your keys
```
sudo apt install curl # if you haven't already installed curl
curl -s --compressed "https://rosneuro.github.io/ppa/ubuntu/rosneuro-key.gpg" | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/rosneuro-key.gpg >/dev/null
```

### 1.3 Installation
First, make sure your Debian package index is up-to-date:
```
sudo apt-get update
```
Then, install **rosneuro-full:**
```
sudo apt-get install ros-noetic-rosneuro-full
```

### 1.4 Update ```rosdep``` list
Add **ROS-Neuro** packages to the ```rosdep``` list:
```
sudo sh -c 'echo "yaml https://rosneuro.github.io/ppa/ubuntu/rosdep-rosneuro-packages.yaml" > /etc/ros/rosdep/sources.list.d/50-rosneuro-packages.list'
```
Update ```rosdep```:
```
rosdep update
```

### (1.5 Alternative installation) 
It is possible to checkout all **ROS-Neuro** packages in the same workspace and to use `catkin_make` and `catkin_make install` to build and install them in the system.


## 2. ROS-Neuro packages

Currently, **ROS-Neuro** provides the following packages:

- [**rosneuro_msgs**](https://github.com/rosneuro/rosneuro_msgs) Standard ROS messages in **ROS-Neuro** framework
- [**rosneuro/rosneuro_data**](https://github.com/rosneuro/rosneuro_data) Data structures in **ROS-Neuro** framework
- [**rosneuro/rosneuro_acquisition**](https://github.com/rosneuro/rosneuro_acquisition) Generic interface for acquiring data from different devices
- [**rosneuro/rosneuro_acquisition_eegdev**](https://github.com/rosneuro/rosneuro_acquisition_eegdev) Acquisition plugin for eegdev library
- [**rosneuro/rosneuro_acquisition_lsl**](https://github.com/rosneuro/rosneuro_acquisition_lsl) Acquisition plugin for LSL library
- [**rosneuro/rosneuro_recorder**](https://github.com/rosneuro/rosneuro_recorder) Generic interface for recording neuro data
- [**rosneuro/rosneuro_visualizer**](https://github.com/rosneuro/rosneuro_visualizer) Scope for EEG and EMG data
- [**rosneuro/rosneuro_buffers**](https://github.com/rosneuro/rosneuro_buffers) Generic buffers for neuro data
- [**rosneuro/rosneuro_buffers_ringbuffer**](https://github.com/rosneuro/rosneuro_buffers_ringbuffer) Buffer plugin for ringbuffer
- [**rosneuro/rosneuro_filters**](https://github.com/rosneuro/rosneuro_filters) Generic filters for neuro data
- [**rosneuro/rosneuro_filters_dc**](https://github.com/rosneuro/rosneuro_filters_dc) Filters plugin for DC filter
- [**rosneuro/rosneuro_filters_butterworth**](https://github.com/rosneuro/rosneuro_filters_butterworth) Filters plugin for Butterworth filter
- [**rosneuro/rosneuro_filters_car**](https://github.com/rosneuro/rosneuro_filters_car) Filters plugin for CAR filter
- [**rosneuro/rosneuro_filters_laplacian**](https://github.com/rosneuro/rosneuro_filters_laplacian) Filters plugin for Laplacian filter
- [**rosneuro/rosneuro_filters_blackman**](https://github.com/rosneuro/rosneuro_filters_blackman) Filters plugin for Blackman window
- [**rosneuro/rosneuro_filters_flattop**](https://github.com/rosneuro/rosneuro_filters_flattop) Filters plugin for Flattop window
- [**rosneuro/rosneuro_filters_hamming**](https://github.com/rosneuro/rosneuro_filters_hamming) Filters plugin for Hamming window
- [**rosneuro/rosneuro_filters_hann**](https://github.com/rosneuro/rosneuro_filters_hann) Filters plugin for Hann window

---

## References:
- Tonin L, Beraldo G, Tortora S, Menegatti E (2022) ROS-Neuro: An Open-Source Platform for Neurorobotics. Front. Neurorobot. 16:886050. doi: 10.3389/fnbot.2022.886050
- Tonin L, Beraldo G, Tortora S, Tagliapietra L, Millàn JdR et al. (2019). ROS-Neuro: A common middleware for BMI and robotics. The acquisition and recorder packages, in Proc of 2019 IEEE International Conference on Systems, Man and Cybernetics (SMC), 2767–2772
- Beraldo G, Tortora S, Menegatti E, Tonin L. (2020). ROS-Neuro: Implementation of a closed-loop BMI based on motor imagery, in Proc of 2020 IEEE International Conference on Systems, Man, and Cybernetics (SMC), 2031–2037
