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
### ros2 interface show <type>.msg
```
ros2 interface show geometry_msgs/msg/Twist
```
