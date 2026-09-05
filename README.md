# Autonomous Aircraft Tug Prototype using Kobuki

This project explored a small-scale autonomous robotic tug concept for parking
and positioning aircraft.

The experimental platform was based on a TurtleBot2 / Kobuki mobile base. Tests
were conducted in an indoor environment, where a small-scale aircraft setup was
attached to the mobile robot to represent the intended aircraft-parking use case.

The prototype was used to investigate autonomous navigation, mapping,
localization, and positioning before moving toward a custom-built robotic
platform.

> **Note:** This repository contains recovered material from an experimental
> R&D project developed in 2020. Some of the original development files are no
> longer available, so the documentation distinguishes between implemented
> experiments and the intended final aircraft-parking application.

## Project Goal

The main objective was to investigate a small-scale autonomous system capable of:

- Mapping its environment
- Localizing the mobile platform
- Navigating toward defined target positions
- Investigating autonomous parking / positioning behavior
- Supporting future development of an autonomous aircraft tug platform

## Experimental Setup

Experiments were conducted indoors using a mobile robot as the prototype
platform. A small-scale aircraft setup was attached to the robot to represent
the aircraft-parking application.

The hardware environment included:

- TurtleBot2 / Kobuki mobile base
- RPLIDAR
- NVIDIA Jetson TX2
- Laptop for development and visualization
- Kinect sensor available on the TurtleBot2 platform

LiDAR was used as the primary sensor for mapping and navigation experiments.

## Software and Robotics Stack

The project involved:

- ROS
- Gazebo
- RViz
- URDF robot modeling
- SLAM
- TurtleBot packages
- Kobuki base integration
- Navigation and pose-based motion
- SSH and remote visualization
- ROS network configuration

## Development Approach

The project initially focused on simulation and ROS system integration before
testing the approach with the physical prototype.

The work included adapting and configuring existing ROS/TurtleBot components
for the experimental Kobuki, Jetson TX2, and RPLIDAR setup.

The development workflow included:

1. Configuring and modifying the robot model
2. Integrating LiDAR into the ROS environment
3. Configuring and testing SLAM
4. Generating an indoor occupancy map
5. Visualizing the robot, coordinate frames, sensor information, and map in RViz
6. Working with target poses and autonomous navigation
7. Investigating autonomous positioning / parking behavior

## Mapping and SLAM

LiDAR-based SLAM approaches were investigated for mapping the indoor
environment.

Recovered project artifacts include a generated occupancy map with a resolution
of 0.05 m/pixel.

Recovered ROS TF data also shows the mapping/navigation transform chain,
including frames such as:

`map -> odom -> base_footprint -> base_link`

along with wheel, IMU, and laser-related frames.

The recovered workspace contains experiments involving GMapping as well as
configuration related to other SLAM approaches investigated during development.

## System Integration Challenges

A significant part of the project involved practical ROS and hardware
integration, including:

- Running ROS components across the Jetson TX2 and a development laptop
- Remote visualization using SSH
- ROS network configuration
- Wireless communication between development machines
- RPLIDAR integration
- USB connectivity and bandwidth considerations
- Modifying robot descriptions for the experimental hardware configuration
- Working with ROS TF coordinate frames
- Running RViz, SLAM, and navigation tools
- Integrating existing TurtleBot/Kobuki ROS components into the prototype

## Recovered Project Artifacts

The original 2020 development workspace was only partially recovered.

This repository preserves selected outputs from the experiments, including:

- Generated occupancy map
- ROS map configuration
- TF frame diagrams
- Documentation of the experimental architecture and development process

Standard ROS, TurtleBot, and Kobuki packages used by the project are not
republished here as original work.

## Project Status

This was an experimental R&D prototype rather than a production aircraft tug.

The recovered artifacts confirm work on ROS integration, robot modeling,
mapping/SLAM, TF configuration, simulation, and navigation experimentation.

The broader project investigated autonomous aircraft positioning and parking
using a small-scale aircraft setup attached to the mobile robot. Because the
complete original workspace and documentation are no longer available, this
repository does not claim that the complete autonomous aircraft-parking
workflow reached its intended final implementation.

## Attribution

The project was built using existing open-source ROS, TurtleBot, Kobuki,
Gazebo, SLAM, and navigation components.

These underlying packages and drivers were not developed by me. This repository
documents the project-level system integration, configuration, experimentation,
and recovered outputs from the prototype.
