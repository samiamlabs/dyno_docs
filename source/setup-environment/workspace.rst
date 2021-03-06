
Setup workspace
====================

Catkin Tools
----------------------------

.. code:: bash

  sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu `lsb_release -sc` main" > /etc/apt/sources.list.d/ros-latest.list'
  wget http://packages.ros.org/ros.key -O - | sudo apt-key add -
  sudo apt-get update
  sudo apt-get install python-catkin-tools

Dyno shell tools
----------------------------

.. code:: bash

  mkdir ~/Code && cd ~/Code
  git clone git@github.com:ErikOrjehag/dyno-shell.git
  cd dyno-shell
  cp rosenv-templ.sh ~/.rosenv
  mkdir -p ~/catkin_ws/src
  cd ~/catkin_ws
  catkin build
  echo "source ~/.rosenv" >> ~/.bashrc
  source ~/.bashrc

ROS repositories
----------------------------------

.. code:: bash

  git clone git@github.com:samiamlabs/dyno.git
  git clone git@github.com:samiamlabs/omnibot_driver.git
  git clone git@github.com:samiamlabs/mecanum_controller.git
  type ddep
  ddep
  dmake

Documentation
-----------------------------

.. code:: bash

  cd ~/Code
  git clone git@github.com:samiamlabs/dyno_docs.git
  sudo pip install sphinx sphinx-autobuild sphinx-rtd-theme testresources
  cd dyno_docs
  make html
