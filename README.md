# ros2 run
ros2 run <package_name> <executable_name>
```
ros2 run turtlesim turtlesim_node
ros2 run turtlesim turtle_teleop_key
```
```
ros2 run turtlesim turtlesim_node --ros-args --remap __node:=my_turtle
```
ros2 run <package_name> <executable_name> --ros-args --params-file <file_name>

```
ros2 run turtlesim turtlesim_node --ros-args --params-file ./turtlesim.yaml
```
