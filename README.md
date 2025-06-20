# Limo Pro Multimodal Locomotion

**Adaptive multimodal locomotion on AgileX Limo Pro via real-time terrain classification and automatic mode switching.** 

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Hardware & Software Requirements](#hardware--software-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)

## Overview
This project equips the AgileX Limo Pro robot with an embedded pipeline that fuses LiDAR and RGB-D data to classify terrain (hard, soft, obstacle) and automatically switch between differential, Ackermann, omni and tracked modes in ROS :contentReference[oaicite:1]{index=1}.

## Features
- Real-time terrain classification (<50 ms inference)  
- Automatic mechanical mode reconfiguration via ROS ActionLib  
- Support for four locomotion modes: differential, Ackermann, omni and tracks

## Hardware & Software Requirements
- **Robot**: AgileX Limo Pro with LiDAR & RGB-D camera  
- **Compute**: NVIDIA Jetson Orin Nano  
- **OS**: Ubuntu 20.04 with ROS Noetic (or ROS2 Foxy) :contentReference[oaicite:2]{index=2}  
- **Dependencies**: Python 3.8+, OpenCV, PCL, PyTorch/TensorRT

## Installation
```bash
git clone https://github.com/<your-org>/limo-pro-multimodal-locomotion.git
cd limo-pro-multimodal-locomotion
pip install -r requirements.txt
colcon build

