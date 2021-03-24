Reference: https://docs.ros.org/en/foxy/Tutorials.html

# ROS2 RUN
### ros2 run <package_name> <executable_name>
```
ros2 run turtlesim turtlesim_node
ros2 run turtlesim turtle_teleop_key
```
```
ros2 run turtlesim turtlesim_node --ros-args --remap __node:=my_turtle
```
### ros2 run <package_name> <executable_name> --ros-args --params-file <file_name>
```
ros2 run turtlesim turtlesim_node --ros-args --params-file ./turtlesim.yaml
```

# ROS2 NODE
```
ros2 node list
```
### ros2 node info <node_name>
```
ros2 node info /my_turtle
```

# RQT
```
rqt
rqt_graph
ros2 run rqt_console rqt_console
```

# ROS2 TOPIC
```
ros2 topic list
ros2 topic list -t
```
### ros2 topic echo <topic_name>
```
ros2 topic echo /turtle1/cmd_vel
```
### ros2 topic info <topic_name>
```
ros2 topic info /turtle1/cmd_vel
```
### ros2 interface show <type_name>.msg
```
ros2 interface show geometry_msgs/msg/Twist
```

### ros2 topic pub <topic_name> <msg_type> "args"
```
ros2 topic pub --once /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0, y: 0.0, z: 0.0}, angular: {x: 0.0, y: 0.0, z: 1.8}}"
ros2 topic pub --rate 1 /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0, y: 0.0, z: 0.0}, angular: {x: 0.0, y: 0.0, z: 1.8}}"
```
### ros2 topic hz <topic_name>
```
ros2 topic hz /turtle1/pose
```

# ROS2 SERVICE
```
ros2 service list
ros2 service list -t
```
### ros2 service type <service_name>
```
ros2 service type /clear
```
```
ros2 service find std_srvs/srv/Empty
```
### ros2 interface show <type_name>.srv
```
ros2 interface show std_srvs/srv/Empty.srv
```
### ros2 service call <service_name> <service_type> "args"
```
ros2 service call /clear std_srvs/srv/Empty
ros2 service call /spawn turtlesim/srv/Spawn "{x: 2, y: 2, theta: 0.2, name: ''}"
```

# ROS2 PARAM
### ros2 param get <node_name> <parameter_name>
```
ros2 param get /teleop_turtle scale_angular
ros2 param get /turtlesim background_g
```
### ros2 param set <node_name> <parameter_name> "value"
```
ros2 param set /turtlesim background_r 150
```
### ros2 param dump <node_name>
```
ros2 param dump /turtlesim
```

# ROS2 ACTION
```
ros2 action list
ros2 action list -t
```
```
ros2 action info /turtle1/rotate_absolute
```
```
ros2 interface show turtlesim/action/RotateAbsolute.action
```
### ros2 action send_goal <action_name> <action_type> "values"
```
ros2 action send_goal /turtle1/rotate_absolute turtlesim/action/RotateAbsolute "{theta: 1.57}"
ros2 action send_goal /turtle1/rotate_absolute turtlesim/action/RotateAbsolute "{theta: -1.57}" --feedback
```

# ROS2 Launch
### ros2 launch <launch_file_name>
```
ros2 launch turtlesim_mimic_launch.py
```
### ros2 launch <package_name> <launch_file_name>
