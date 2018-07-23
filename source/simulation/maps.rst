Guide: Loading and saving maps
==============================

.. _web_interface: http:/io.dynorobotics.se

Open a terinal and run `roslaunch dyno_gazebo bringup.launch`

Open `web_interface`_ in a browser. Make sure that hostname set to your computer.

Start making a new map toggling the *cartographer load new 2d* switch in the
*Capabilies* section of the web interface.

.. figure:: /_static/simulation/new_map.gif
   :width: 50%
   :align: center
   :figclass: align-centered

Enable navigation with move_base by toggling navigation.

.. figure:: /_static/simulation/new_map2.gif
   :width: 50%
   :align: center
   :figclass: align-centered

Move around in the environment by sending navigation goals in rviz.

.. figure:: /_static/simulation/new_map3.gif
   :width: 50%
   :align: center
   :figclass: align-centered

You also drive around manually by using a joystick or keyboard. See :doc:`/simulation/teleop` for more details.


Alternativly you can use the *Exploration* Rapp to make the robot explore the environment autonomously. See :doc:`/simulation/exploration`.

.. figure:: /_static/simulation/new_map4.gif
   :width: 50%
   :align: center
   :figclass: align-centered

When you have finished mapping, first click the *Finish Trajectory 0* button and then
the *Save State* button in the *Cartographer*.

.. figure:: /_static/simulation/new_map5.gif
   :width: 50%
   :align: center
   :figclass: align-centered

The *Finish Trajectory 0* button freezes the trajectory and runs some optimizations,
so you will not be able to coninue mapping after pressing is. (Saving the sate without finishing trajectory first also works)

Turn off mapping.

.. figure:: /_static/simulation/new_map6.gif
   :width: 50%
   :align: center
   :figclass: align-centered

Toggle the *cartographer load state 2d* switch to load the saved map.

.. figure:: /_static/simulation/new_map7.gif
   :width: 50%
   :align: center
   :figclass: align-centered

The robot will start on a new trajectory (green) and continue mapping from where it left off.

.. figure:: /_static/simulation/new_map8.gif
   :width: 50%
   :align: center
   :figclass: align-centered
