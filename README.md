# TurtleBot3

This repository contains all the necessary files and instructions to control and navigate a TurtleBot3 using ROS Noetic.

## Prerequisites

- ROS Noetic
- Ubuntu 20.04

## Setup

1. Install TurtleBot3 packages:
   ```bash
   sudo apt-get update
   sudo apt-get install ros-noetic-turtlebot3 ros-noetic-turtlebot3-simulations
   ```
2. Set TurtleBot3 model:
   ```bash
   echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
   source ~/.bashrc
   ```

## Usage

1. Launch TurtleBot3 simulation in Gazebo:
   ```bash
   roslaunch turtlebot3_gazebo turtlebot3_world.launch
   ```
2. Launch TurtleBot3 SLAM for map creation:
   ```bash
   roslaunch turtlebot3_slam turtlebot3_slam.launch
   ```
3. Save the map:
   ```bash
   rosrun map_server map_saver -f ~/map
   ```
4. Launch TurtleBot3 navigation with the saved map:
   ```bash
   roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
   ```
![Screenshot (71)](https://github.com/user-attachments/assets/79beb7d8-408f-480f-907f-2b57d2ee7fc2)
![Screenshot (70)](https://github.com/user-attachments/assets/776783c0-af93-432d-b8da-e890eb40ffac)
![Screenshot (69)](https://github.com/user-attachments/assets/2d394f3a-80ad-4197-8018-485247419cd2)
![Screenshot (68)](https://github.com/user-attachments/assets/bbefa86e-67a4-479b-86bc-7441f17866e9)
![Screenshot (67)](https://github.com/user-attachments/assets/b86918a4-c283-4150-8379-07682650e2a0)
![Screenshot (66)](https://github.com/user-attachments/assets/da90ccd1-4e45-4338-b61c-599da032c16a)


   
