# ENPM809Y Final Project - Robot Navigation with ArUco Markers

[![Project Output Video](YOUR_GITHUB_VIDEO_LINK)](YOUR_GITHUB_VIDEO_LINK)

## Overview
This project is part of the ENPM809Y - Introductory Robot Programming course at the University of Maryland. The objective was to develop a ROS2-based solution for navigating a Turtlebot within a Gazebo simulation environment using ArUco markers and logical cameras.

## Project Objectives
- Create a ROS2 package for robot navigation.
- Detect an ArUco marker using an RGB camera and retrieve relevant parameters.
- Identify various colored batteries using static logical cameras.
- Plan and execute a path for the robot to navigate through predefined poses.

## Features Implemented
1. **ArUco Marker Detection**
   - Utilized OpenCV for detecting ArUco markers in the environment.
   - Extracted marker ID and retrieved corresponding navigation parameters.

2. **Logical Camera Integration**
   - Subscribed to multiple static camera topics to detect different parts in the environment.
   - Transformed object positions from camera frames to the map frame.

3. **Navigation Through Poses**
   - Implemented an action client to command the robot to sequentially visit part locations based on the detected ArUco marker ID.
   - Used ROS2's `/navigate_through_poses` action server to move through multiple waypoints.

4. **Setup and Installation**
   - Installed required ROS2 dependencies.
   - Configured workspace and package structure.
   - Ensured correct integration of logical cameras and navigation stack.

## Setup Instructions
1. Clone this repository into your ROS2 workspace:
   ```sh
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
   ```
2. Navigate to your workspace:
   ```sh
   cd ~/your_ros2_workspace
   ```
3. Install dependencies:
   ```sh
   rosdep install --from-paths src -y --ignore-src
   ```
4. Build the package:
   ```sh
   colcon build
   ```
5. Source the workspace:
   ```sh
   source install/setup.bash
   ```
6. Launch the simulation:
   ```sh
   ros2 launch final_project final_project.launch.py
   ```

## Code Documentation
- All implemented classes, functions, and nodes are documented using Doxygen-style comments.
- The navigation and detection logic is modularized for clarity and reusability.

## Challenges and Learnings
- **Frame Transformations:** Converting part positions from logical camera frames to the global map frame.
- **Efficient Topic Subscriptions:** Managing multiple topic subscriptions dynamically to optimize resource usage.
- **Action-Based Navigation:** Understanding and implementing ROS2 actions for multi-waypoint navigation.

## Future Improvements
- Extend functionality to incorporate dynamic obstacles.
- Implement SLAM to navigate without a preloaded map.
- Optimize computational performance by reducing redundant topic subscriptions.

## Acknowledgments
Special thanks to Professor Z. Kootbally and the ENPM809Y teaching staff for their guidance throughout the project.

---

Feel free to update the video link, repository URL, and any additional details as necessary!

