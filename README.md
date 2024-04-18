# ign_ros2_control_demos

Let me show you some magic.

Build this ROS2 package in your workspace. Run:

```
ros2 launch ign_ros2_control_demos arm_position.launch.py
```

In another terminal run:

```
ros2 topic pub --once /arm_controller/commands std_msgs/msg/Float64MultiArray "data:
- 0.35"
```

With this command you can move the cylinder to any position between 0.0 and 0.35.

Now, for the magic. Open the file `test_simple_arm.xacro.urdf`. Then change the line `<joint name="joint_base" type="prismatic">` to `<joint name="joint_base" type="revolute">`. Now run the simulation again. Surprise! Nothing works. Why? Because ros2 control hates you.