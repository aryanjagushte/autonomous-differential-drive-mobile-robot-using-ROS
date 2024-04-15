# autonomous-differential-drive-mobile-robot-using-ROS

## diff_drive_robot_description

This ROS package contains the description of a differential drive robot for simulation in Gazebo.
The robot's URDF model and associated files are provided to facilitate simulation and testing.

*Prerequisites*

Before using this package, ensure that you have the following installed:

  ROS Noetic: Installation instructions
  
  Navigation Stack: Install using
    sudo apt-get install ros-noetic-navigation
  
  Hector SLAM: Clone the repository using :
    git clone https://github.com/tu-darmstadt-ros-pkg/hector_slam.git

## Usage

# Launch Mapping

![slam](https://github.com/aryanjagushte/autonomous-differential-drive-mobile-robot-using-ROS/assets/90960915/0f974d86-a415-48fe-81f6-d5bbf47ac36a)

To launch the mapping process with Hector SLAM, follow these steps:

  *Launch the demo world for your robot:*

    roslaunch diff_drive_robot_description demo_world.launch

Launch the Hector SLAM tutorial:

    roslaunch hector_slam_launch tutorial.launch

**Once both launch files are running, you should see the mapping process begin in Gazebo.**

Load a Saved Map

To load a previously saved map, ensure you have the map_server package installed:

arduino

sudo apt-get install ros-noetic-map-server

Then, use the map_server to load the map:

rosrun map_server map_server <path_to_map_file>

Replace <path_to_map_file> with the path to your saved map file.


# Navigation

![navigation](https://github.com/aryanjagushte/autonomous-differential-drive-mobile-robot-using-ROS/assets/90960915/b711a94e-bcd7-4167-8bd5-81f097f605fa)


To enable navigation for your robot, follow these steps:

  *Launch the Gazebo world for your robot:*

roslaunch diff_drive_robot_description demo_world.launch

Launch the navigation stack:

    roslaunch diff_drive_robot_description navigation.launch
    

Once both launch files are running, your robot should be ready for navigation. You can use tools like RViz to send navigation goals and visualize the robot's path.

Notes

  For troubleshooting and further information on ROS navigation, refer to the official ROS documentation: http://wiki.ros.org/navigation

  
## Feel free to customize and expand upon this README file.
