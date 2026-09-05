# Autonomous Prototype using Kobuki

This project explored a small-scale autonomous robotic tug concept using a TurtleBot2 / Kobuki mobile platform.

The work was carried out in 2020 as part of my role as an Associate AI Engineer at NextBridge, where I contributed to an autonomous robotics R&D effort involving ROS, mobile robot integration, mapping, navigation.

Experiments were conducted indoors using a small-scale setup attached to the mobile robot to represent the intended application.

> **Note:** This repository contains recovered material from the original project.
> Some development files are no longer available, so the documentation distinguishes
> between recovered/verified experiments and the intended final application.

## Project Goal

The prototype was used to investigate:

- LiDAR-based mapping and localization
- Autonomous navigation toward target positions
- Robot and sensor integration using ROS
- Autonomous positioning / parking behavior

## Experimental Setup

**Hardware**
- TurtleBot2 / Kobuki mobile base
- RPLIDAR
- NVIDIA Jetson TX2
- Development laptop
- Kinect sensor available on the TurtleBot platform

**Software / Robotics**
- ROS
- Gazebo
- RViz
- URDF
- SLAM / GMapping
- TurtleBot & Kobuki packages
- ROS Navigation
- SSH and ROS networking

LiDAR was used as the primary sensor for mapping and navigation experiments.

## Development & Integration

The project began with simulation and ROS system integration before testing with the physical prototype.

The work included:

- Configuring and modifying the robot model
- Integrating RPLIDAR with the ROS environment
- Configuring and testing SLAM
- Generating an indoor map
- Working with ROS TF coordinate frames
- Visualizing the robot, map, and sensor data in RViz
- Working with target poses and autonomous navigation
- Running ROS components across the Jetson TX2 and development laptop
- Configuring SSH, ROS networking, and remote visualization
- Investigating autonomous positioning / parking behavior

## Recovered Results

Recovered project artifacts include an indoor occupancy map generated at **0.05 m/pixel** and ROS TF diagrams showing the mapping/navigation frame structure:

`map -> odom -> base_footprint -> base_link`
