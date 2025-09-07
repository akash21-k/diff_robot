# diff_robot
# built in ros2 humble in ubuntu 22.04

# setup 
$ mkdir -p ros2_ws/src
$ cd ros2_ws/src
$ git clone 

# for gazebo simulation and control of robot through keyboard
$ source ros2_ws/install/setup.bash
$ ros2 launch diff_robot gazebo.launch.py
$ ros2 run teleop_twist_keyboard teleop_twist_keyboard

# for mapping and SLAM
$ source ros2_ws/install/setup.bash
$ ros2 launch diff_robot turtlebot3_world.launch.py
$ ros2 run teleop_twist_keyboard teleop_twist_keyboard

# after the mapping in order to save the map:
$ ros2 run nav2_map_server map_saver_cli -f ~/my_map
after the saving the close all the tab

# for autonomous navigation 
$ source ros2_ws/install/setup.bash
$ ros2 launch diff_robot turtlebot3_navigation.launch.py

using the 2d nav goal option in rviz2, give the position to move the robot.
