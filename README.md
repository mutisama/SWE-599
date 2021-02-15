This repository containts the necessary codes and configurations for implementing slam with a Nvidia Jetbot robot.

There are two nodes, which are separated as `jetbot_node` and `remote_node`.

**Jetbot node**

`jetbot_node` includes all of the code that is run at JetBot which is the core ros node.

In order to start the ROS nodes that are necessary for slam, please follow the steps:

1- `roscore` (start ros core node)
2- `sudo chmod 666 /dev/ttyUSB0` (give necessary permissions to Lidar usb port)
3- `roslaunch jetbot_node sensors.launch` (this will start all of the necessary ros nodes)

**Remote node**

`remote_node` includes all of the code that is run at the remote computer which is connected to ROS network.

In order to start the ROS that are necessary for slam, please follow the steps:

1- Start jetbot_node first by following the required steps, if not, the slam won't work.

***For hector slam***

2- `roslaunch remote_node run_hector_slam.launch` (this will start all of the necessary ros nodes for hector slam)

***For cartographer slam***

3- `roslaunch remote_node run_cartographer.launch` (this will start all of the necessary ros nodes for cartographer slam)
