# Line Follower using ROS-Gazebo
 
This project aims to implement line follower robot using TurtleBot3 Waffle Bot on Gazebo using ROS.


## Dependencies

- ROS Noetic
- Gazebo Simulator
- TurtleBot3 ROS package
- Python==3.7
- OpenCv


## Approach

This is the implementaion of a line follower robot in ROS-Gazebo. This is a camera based line follower robot, in this the image is published on the topic *image_raw* by the gazebosim, which is then subscribed by the node created by us in our python script. The image is then passed through a opencv image pipeline which detects the centre point of the path in front of the bot. Then is robot is rotated proportional to the difference between the center point of path and the image, after this linear velocity is published along with rotation on the *cmd_vel* topic which is then subscribed by gazebo.

## OpenCv Pipeline

- Image obtained from the topic *image_raw* is converted to HSV image. 

## Results

![Hnet com-image](https://user-images.githubusercontent.com/64823050/130450615-f4f6c4f6-5411-48ed-952e-375e8dfd2e81.gif)


## References

[Programming Robots with ROS, by Quigley, Morgan and Gerkey, Brian and Smart, William D., 2015](https://github.com/osrf/rosbook/tree/master/followbot)
