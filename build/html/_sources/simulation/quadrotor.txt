Quadrotor
---------

.. figure:: /_static/simulation/quadrotor.png
   :width: 40%
   :align: left
   :figclass: align-left

::

  export DYNO_BASE=quadrotor
  export DYNO_USE_ROS_CONTROL_FOR_BASE="false"
  roslaunch dyno_gazebo bringup.launch

The quadrotor platform is not fully implemented. Mostly because of a
conflict in `Protocol Buffers` (`protobuf`) between Cartographer 1.0
and hector_quadrotor.
