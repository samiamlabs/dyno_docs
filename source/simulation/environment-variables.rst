Environment Variables
=====================

Descriptions
------------

DYNO_BASE
^^^^^^^^^

What robot base shoud be used. This applies both to simulation and real robots.

------------------------------------

DYNO_DEFAULT_RAPP
^^^^^^^^^^^^^^^^^

.. _Robot App: http://wiki.ros.org/rocon/indigo/Guide#rocon_app_platform.Rapps
.. _Concert Client: http://wiki.ros.org/rocon/indigo/Guide#rocon_concert.The_Concert

What `Robot App`_ (Rapp) shoud start automaticly when you bring up a `Concert Client`_.

| Simulation: ``roslaunch dyno_gazebo bringup.launch``
| Real Robot: ``roslaunch dyno_bringup bringup.launch``

------------------------------------

DYNO_USE_ROS_CONTROL_FOR_BASE
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. _mecanum_controller: https://github.com/samiamlabs/mecanum_controller
.. _diff_drive_controller: http://wiki.ros.org/diff_drive_controller
.. _four_wheel_steering_controller: https://github.com/ros-controls/ros_controllers/tree/melodic-devel/four_wheel_steering_controller
.. _ros_control: http://wiki.ros.org/ros_control

Changes whether the robot base subscribes to */mobile_base_controller/cmd_vel* or
uses `ros_control`_ to control the joints directly.

If set to true, a controller that translates */mobile_base_controller/cmd_vel*
to joint velocities is started.

Diffrent controllers are started depending on what base is used.
The controllers currently used are: `mecanum_controller`_, `diff_drive_controller`_, `four_wheel_steering_controller`_.

Defalut Gazebo physics with `ros_control`_ doesn't currently work for the
holonomic/omni plattform, so this variable sould be set to false when simulating theese platforms.

------------------------------------

DYNO_JOY_TYPE
^^^^^^^^^^^^^

Type of joystick.

------------------------------------

JOY_SERIAL_PORT
^^^^^^^^^^^^^^^

Serial port to use for joystick.

------------------------------------

Values
------

==============================  =====================================  ===================================================
Name                            Defalut Value                          Optional Values
==============================  =====================================  ===================================================
DYNO_BASE                       turtlebot3                             omnibot, magni, holonomic, diff-drive, quadrotor
DYNO_DEFAULT_RAPP               dyno_common_rapps/exploration          dyno_common_rapps/waypoint_navigation
DYNO_USE_ROS_CONTROL_FOR_BASE   false                                  true
DYNO_JOY_TYPE                   gamepad                                xbox360, playstation
JOY_SERIAL_PORT                 /dev/input/js0                         --
==============================  =====================================  ===================================================
