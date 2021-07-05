Use-Turtlebot3-with-SLAM 
# 
**Install Dependent ROS 1 Packages**

`````````
$ sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy 

$ sudo ros-melodic-teleop-twist-keyboard ros-melodic-laser-proc 

$ sudo ros-melodic-rgbd-launch ros-melodic-depthimage-to-laserscan 

$ sudo ros-melodic-rosserial-arduino ros-melodic-rosserial-python 

$ sudo ros-melodic-rosserial-server ros-melodic-rosserial-client 

$ sudo ros-melodic-rosserial-msgs ros-melodic-amcl ros-melodic-map-server 

$ sudo ros-melodic-move-base ros-melodic-urdf ros-melodic-xacro 

$ sudo ros-melodic-compressed-image-transport ros-melodic-rqt* 

$ sudo ros-melodic-gmapping ros-melodic-navigation ros-melodic-interactive-markers
`````````
# 

**Install TurtleBot3**

```
$ sudo apt-get install ros-melodic-dynamixel-sdk

$ sudo apt-get install ros-melodic-turtlebot3-msgs

$ sudo apt-get install ros-melodic-turtlebot3
```
# 
**TurtleBot3 Waffle Pi**

`$ echo "export TURTLEBOT3_MODEL=waffle_pi" `
# 
**Install Simulation Package**


`$ export TURTLEBOT3_MODEL=waffle_pi`

`$ roslaunch turtlebot3_gazebo turtlebot3_world.launch`

# 
**Run SLAM Node**

`$ export TURTLEBOT3_MODEL=waffle_pi`

`$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping`

# 
**control the robot and ceaite the map**

`$ export TURTLEBOT3_MODEL=waffle_pi`

`$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch`
# 
**save the map**

`$ rosrun map_server map_saver -f ~/map`
