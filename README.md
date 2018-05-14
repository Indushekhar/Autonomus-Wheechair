# Autonomus-Wheechair
Autonomous Wheelchair project : Project 5 for the course ENPM 661 Planning of Autonomus Robot
# workspace for project 5 : Autonomus wheechair
# Ashwin Goyal
# Ashish Patel
# Indushekhar Singh

ROS Verison : Kinetic





In Terminal 1, launch the Gazebo world

roslaunch mybot_gazebo mybot_world.launch

In Terminal 2, start map building

roslaunch mybot_navigation gmapping_demo.launch


In Terminal 3, launch rviz and set the following parameters:

roslaunch mybot_description mybot_rviz_gmapping.launch


In Terminal 4,  Send a base controller command and ensure that the robot moves in both Gazebo and rviz : 

rostopic pub /cmd_vel geometry_msgs/Twist "linear:
  x: 0.2
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.1"

In Terminal 5, save the map to some file path

rosrun map_server map_saver -f ~/mybot_ws/src/mybot_navigation/maps/test_map
