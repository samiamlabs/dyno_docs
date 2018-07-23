Guide: Route Scheduler
======================

.. _web_interface: http:/io.dynorobotics.se

Open a terinal and run::

   roslaunch dyno_gazebo bringup.launch

Open `web_interface`_ in a browser. Make sure that hostname set to your computer.

Start the Route scheduler app by clicking on *Route Scheduler* in the *Robot Apps*
section.

.. figure:: /_static/simulation/route_scheduler.gif
   :width: 30%
   :align: center
   :figclass: align-centered

Previously saved locations will be automaticly loaded when you start the app.
To add additional locations, move the robot to where you want it and press
the *Add Current Location* button in the *World State* section of the web interface.

.. figure:: /_static/simulation/route_scheduler2.gif
   :width: 80%
   :align: center
   :figclass: align-centered

.. figure:: /_static/simulation/route_scheduler3.png
   :width: 80%
   :align: center
   :figclass: align-centered

Add a waypoint/location to the queue by selecting it in the dropdown list and
clicking the *+* button.

.. figure:: /_static/simulation/route_scheduler4.gif
   :width: 50%
   :align: center
   :figclass: align-centered

Click the *Start* button to start moving the robot.

.. figure:: /_static/simulation/route_scheduler5.gif
   :width: 100%
   :align: center
   :figclass: align-centered

To get an idea of what is happening behind the scenes, run this in a new terminal::

  rosrun rqt_py_trees rqt_py_trees

.. figure:: /_static/simulation/route_scheduler6.gif
   :width: 100%
   :align: center
   :figclass: align-centered
