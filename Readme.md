**Author:Bismaya Sahoo**

**Email:bsahoo@uwaterloo.ca**


**DESCRIPTION**
--------------

* This package contains the gazebo description of the argo_world in Gazebo. 
* Although,all the experimental worlds are included here. The one recently tested is the argo_custom.launch. Have a look at the file to understand what is being launched.
* This is just the Gazebo World configuration which has to be launched in conjuction of other argo_descriptions. 
* Full interconnectivity will be updated in a while.

**UPDATE**
----------

1. The list of packages needed for simulation of the argo in Gazebo.
  * argo_gazebo
  * argo_viz
  * argo_description
  * argo_custom
  * argo_navigation
  * argo_base_control (for control via the joystick.)

2. Compile all these packages. Make sure Gazebo and RVIZ are installed. Ensure ROS navigation packages are installed.

3. Launch Sequence:
  * ```roslaunch argo_gazebo argo_custom.launch```
  * ```roslaunch argo_viz view_robot.launch```
  * ```roslaunch argo_navigation amcl_demo.launch``` 

   or
  * ```roslaunch argo_navigation gmapping_demo.launch```

   In order to move the robot, set 2D Nav Goal in Rviz. 

   If you wish to move the robot via keyboard:

  * ```rosrun teleop_twist_keyboard teleop_twist_keyboard.py```

   Alternatively, to move it via joystick.

  * ```roslaunch argo_base_control argo_joy_gazebo.launch```
  
  
**FUTURE MODIFICATIONS**
------------------------

1. Models to Scale in Solidworks
2. Models to be more descriptive. 
  * Seat color
  * Logo
  * Inertia and Mass
  * Sensor Models
3. Brake Models to be skid steer configurations as in ARGO. Currently, differential drive.


