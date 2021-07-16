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


![8368DBE2-1CE6-4F7C-9DDA-25031FD9F46F_1_105_c](https://user-images.githubusercontent.com/86611989/125992091-3e8f3332-170d-43a1-b49e-a2e32f90522e.jpeg)





**SLAM simulation**


Gmapping SLAM :

$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping


![2C122AC1-5201-447C-BA56-798CB4780280_1_105_c](https://user-images.githubusercontent.com/86611989/125992331-d27bc82a-edb1-4a16-bdbd-cc02d57f6bb8.jpeg)




control the robot by :


$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch



![D4E7C44F-B9E3-4D75-AB66-EC560B5806E6_1_105_c](https://user-images.githubusercontent.com/86611989/125992467-95be18f1-392e-4c3d-997e-578de1001a41.jpeg)



When the map is created successfully, open a new terminal and save the map.

$ rosrun map_server map_saver -f ~/map
