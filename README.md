# Gazebo_Simulation_Tutorial_MindCloud
A repo contains the steps to simulate anything in Gazebo including ready-to-run models or your own models

## Sensor fusion 
- First Terminal :
  
``export TURTLEBOT3_MODEL=waffle``

``source ~/turtlebot3_ws/install/setup.bash ``

``ros2 run turtlebot3_teleop teleop_keyboard``

- Second Terminal :
  
``source ~/sensor_fusion_ws_tut/install/setup.bash ``

``ros2 launch sensor_fusion_pkg file.py``

- Third Terminal :
  
``export TURTLEBOT3_MODEL=waffle``

``source ~/turtlebot3_ws/install/setup.bash ``

``source ~/sensor_fusion_ws_tut/install/setup.bash``

``ros2 run sensor_fusion_pkg visual_odom_node``

- Fourth Terminal :
  
``source ~/sensor_fusion_ws_tut/install/setup.bash``

``ros2 topic echo /odometry/filtered --once``

- To visualize in rviz2 :

``source ~/turtlebot3_ws/install/setup.bash``

``export TURTLEBOT3_MODEL=waffle``

``rviz2``
