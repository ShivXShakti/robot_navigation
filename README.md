# robot_navigation
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_gazebo turtlebot3_stage_4.launch

##### mapping
roslaunch turtlebot3_slam turtlebot3_gmapping.launch 
rosrun rviz rviz
or if you have rviz file
roslaunch navigation rviz_file.launch
rosrun map_server map_saver -f navigation_map
rosrun map_server map_server navigation_map.yaml     #with location

##### localization
rosrun rviz rviz
roslaunch navigation rviz_navigation.launch
rosrun map_server map_server navigation_map.yaml
roslaunch turtlebot3_navigation amcl.launch
