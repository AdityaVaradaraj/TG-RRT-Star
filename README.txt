Group Members:

Aditya Varadaraj 117054859
Saurabh Palande 118133959

Requirements:

Python >= 3.8
cv2 (OpenCV 4.5.5)
numpy
math
random
matplotlib
rospy
actionlib
MoveBase
warnings


Normal CV2 Visualization Instructions:

1) Keep the tg_rrt_star.py and Utils folder in same directory.
2) Run as python3 tg_rrt_star.py
3) Give the start and goal (x,y,theta) coordinates when prompted.
4) Give step size as 5 for good visualization. Give no. of steps of 30 as 2, i.e., (-60, -30, 0, 30, 60) is actionset.
5) Choose the algorithm you want to run
6) Wait for algorithm to finish. (C-RRT* may take a while at times but rest should run quite fast).


ROS/Gazebo Instructions:

1) Please create a package called tgrrt_star in your catkin workspace and copy the contents of the provided package into the package created. Edit map.yaml in maps folder to provide absolute path to map.pgm file.

2) catkin_make or catkin build and source devel/setup.bash

3) You will need ros-noetic-navigation. (Installation by sudo apt-get install ros-noetic-navigation)

4) (150, 50, 0) --> (375, 225, 0)
export Turtlebot3 Burger
roslaunch tgrrt_star turtlebot.launch x_pos:=1.5 y_pos:=4.5 z_pos:=0
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/catkin_ws/src/tgrrt_star/map/map.yaml
In catkin_ws/src/tgrrt_star/scripts,  python3 tgrrt_star.py

5) (50, 50, 0) --> (375, 225, 0)
export Turtlebot3 Burger
roslaunch tgrrt_star turtlebot.launch x_pos:=1.5 y_pos:=1.5 z_pos:=0
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/catkin_ws/src/tgrrt_star/map/map.yaml
In catkin_ws/src/tgrrt_star/scripts,  python3 tgrrt_star.py

6) (50, 225, 0) --> (250, 50, 0)
export Turtlebot3 Burger
roslaunch tgrrt_star turtlebot.launch x_pos:=1.5 y_pos:=6.75 z_pos:=0
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/catkin_ws/src/tgrrt_star/map/map.yaml
In catkin_ws/src/tgrrt_star/scripts,  python3 tgrrt_star.py

7) Basically start x and start y multiplied by 3/100 should give you the coordinates x_pos and y_pos to be entered in the roslaunch tgrrt_star turtlebot.launch arguments.

Results:

https://drive.google.com/drive/folders/1PKRn7unqtmRtu8NBkBP461JPwqbGIMm4?usp=sharing
