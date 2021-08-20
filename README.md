# Line Follower using ROS-Gazebo
 
This project aims to implement line follower robot using TurtleBot3 Waffle Bot on Gazebo using ROS.

## Dependencies

- ROS Noetic
- Gazebo Simulator
- TurtleBot3 ROS package
- Python==3.7
- OpenCv

## Approach

This is the implementaion of a line follower robot in ROS-Gazebo. This is a camera based line follower robot, in this the image is published on the topic *image_raw* by the gazebosim, 
which is then subscribed by the node created by us in our python script. The image is then passed through a opencv image pipeline which detects the centre point of the path in front of
the bot. Then is robot is rotated proportional to the difference between the center point of path and the image, after this linear velocity is published along with rotation on the *cmd_vel* 
topic which is then subscribed by gazebo.

## OpenCv Pipeline



## Results



## References


