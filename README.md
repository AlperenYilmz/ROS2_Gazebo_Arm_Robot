# ROS2_Gazebo_Arm_Robot
- colcon build, for ROS2 Humble
- Create new package, put the files in the package folder, change the name in package.xml and CMakeLists.txt
- There's 2 launch files in the project:
	- **arm_robot_gazebo.launch.xml** launches the gazebo sim (no joint controller)
	- **arm_robot_rviz.launch.xml** launches RViz2 sim
- **Don't forget to edit launch files for paths**
- Dependent packages: RViz2, Gazebo and all relevant packages that come with ros2 humble.

## DESCRIPTION:
- It is a simple robot that incorporates 2 plugins (camera and differential drive) for functionality. **arm_robot.urdf.xacro** contains all the links, joints and plugin implementations
- There are 2 more xacro files inside urdf folder:
	- **link_creator.xacro**, responsible for creating predefined shaped links with creating collisions and inertial tags
	- **inertia_calculator.xacro**, nested in **link_creator.xacro**, is responsible for calculating inertials for links **(does not support meshes!)**
	- **camlink.xacro** is the camera part of the actual robot but kept out of the urdf for better readability of the code.

