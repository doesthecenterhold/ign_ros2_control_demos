# ign_ros2_control_demos

Let me show you some magic.

Build this ROS2 package in your workspace. Run:

```
ros2 launch ign_ros2_control_demos arm_position.launch.py
```

In another terminal run:

```
ros2 topic pub --once /arm_controller/commands std_msgs/msg/Float64MultiArray "{data: [0., 0.25, 2.5, -1.0],layout: {dim:[], data_offset: 1"}}
```

The arm should move! First is base_joint, then shoulder_joint, then elbow_joint and then wrist_joint.