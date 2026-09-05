# Autonomous Aircraft Tug Prototype using Kobuki

This project explored a small-scale autonomous robotic tug concept for parking
and positioning aircraft inside a T-hangar.

The prototype platform was based on a TurtleBot2 / Kobuki mobile base and was
intended to validate autonomous navigation, mapping, localization, and parking
behavior before moving toward a custom-built robotic platform.

## Project Goal

The main objective was to develop a small-scale autonomous system capable of:

- Mapping its environment
- Localizing itself using LiDAR
- Navigating toward a defined target position
- Performing autonomous parking / positioning
- Supporting future development of an autonomous aircraft tug platform

## Hardware

The prototype setup included:

- TurtleBot2 / Kobuki mobile base
- RPLIDAR
- NVIDIA Jetson TX2
- Laptop for development and visualization
- Kinect sensor available on the TurtleBot2 platform

LiDAR was selected as the primary sensor for mapping and navigation.

## Software and Robotics Stack

The project involved:

- ROS
- Gazebo
- RViz
- URDF robot modeling
- Hector SLAM
- TurtleBot packages
- Kobuki base integration
- Navigation and pose-based motion concepts
- SSH and remote visualization
- ROS network configuration

## Development Approach

The project initially focused on simulation and system integration before
testing the approach on the physical TurtleBot2 platform.

A key part of the work involved adapting components commonly used with
TurtleBot3 to work with the Kobuki base, Jetson TX2, and RPLIDAR setup.

The navigation pipeline included:

1. Building and modifying the robot URDF model
2. Integrating the LiDAR
3. Creating a map using SLAM
4. Visualizing the robot and environment in RViz
5. Defining target poses for autonomous movement
6. Investigating autonomous parking behavior

## Mapping and Localization

Hector SLAM was investigated for LiDAR-based mapping because the platform
could operate using LiDAR without relying heavily on additional sensors.

Other mapping approaches such as GMapping and Google Cartographer were also
considered during the research phase.

## System Integration Challenges

Several practical engineering issues were investigated during development:

- Running ROS processes across the Jetson TX2 and a laptop
- Remote visualization using SSH
- ROS network configuration
- Wireless communication between development machines
- USB bandwidth limitations when using multiple high-bandwidth sensors
- RPLIDAR connectivity through USB hubs
- Modifying the URDF model for the custom hardware configuration
- Running RViz and navigation tools remotely

## Project Context

This work was part of an autonomous robotics development effort exploring how
a mobile robotic platform could be used as a small-scale prototype for an
aircraft tug / parking system.
