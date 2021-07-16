# Turtlebot3-_SLAM_TASK2


**installing turtlebot3**

this is steps for ROS melodic:

$ sudo apt-get install ros-melodic-dynamixel-sdk
$ sudo apt-get install ros-melodic-turtlebot3-msgs
$ sudo apt-get install ros-melodic-turtlebot3




In case of TurtleBot3 Waffle Pi

$ echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc



**Gazebo simulation**

compile  in a catkin workspace:

$ cd ~/catkin_ws/src/
$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make


Launch  gazebo simulations for the turtlebot3 robot:


$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch






![533D301F-121F-473A-A12A-A0F61BE45F2E_1_105_c](https://user-images.githubusercontent.com/86611989/125991610-e3cb8b66-9e59-4d45-b927-153cfd3200eb.jpeg)






control the robot movement by typing in terminal shell:

$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch








**SLAM simulation**


Gmapping SLAM :

$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping



control the robot by :


$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch




When the map is created successfully, open a new terminal and save the map.

$ rosrun map_server map_saver -f ~/map
