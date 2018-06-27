
Setup workspace
====================

Catkin build tools
----------------------------

.. code:: bash

  mkdir ~/Code && cd ~/Code
  git clone git@github.com:ErikOrjehag/dyno-shell.git
  cd dyno-shell
  cp rosenv-templ.sh ~/.rosenv
  mkdir -p ~/catkin_ws/src
  cd ~/catkin_ws
  catkin_make
  echo "source ~/.rosenv" >> ~/.bashrc
  source ~/.bashrc
  echo $ROS_PACKAGE_PATH
  type dmake
  dmake

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
