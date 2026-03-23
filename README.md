## My Mobile Robot

```
ros2 launch my_mobile_robot launch_sim.launch.py world:=./src/my_mobile_robot/worlds/obstacles.world 
```

```
rviz2 --ros-args -p use_sim_time:=true
```

```
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -p stamped:=true -p use_sim_time:=true
```


```
ros2 launch slam_toolbox online_async_launch.py use_sim_time:=true params_file:=~/ros2_ws/src/my_mobile_robot/config/mapper_params_online_async.yaml
```

```
ros2 launch nav2_bringup navigation_launch.py params_file:=$HOME/ros2_ws/src/my_mobile_robot/config/nav2_params.yaml use_sim_time:=true
```