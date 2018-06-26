
ROS on Raspberry Pi
===================

The easiest way to setup ROS on Raspberry Pi is to install `Ubuntu Mate <https://ubuntu-mate.org/raspberry-pi/>`_.
Although it's possible to flash your SD using the terminal I would recommend to use a graphical tool to assist,
because it really sucks to destroy your main drive.
`Etcher <https://etcher.io/>`_ is available on Linux, MacOS and Windows to write the image to the SD card.

.. note:: Ubuntu Mate is not currently supported on Pi B3+, don't use the B3+ model for now!

The next step is to enable SSH. Hookup the Pi to a keyboard and monitor and execute the following.

.. code:: bash

  sudo systemctl enable ssh
  sudo systemctl start ssh

Then copy your ssh-key from your workstation to the Pi.

.. code:: bash

  ssh-copy-id -i ~/.ssh/id_rsa.pub pi@x.x.x.x

.. note:: The latest Firefox (version 55) is not supported on the Raspberry kernel, use ``sudo apt-get install chromium-browser`` instead.

Follow the same steps on :doc:`install` for Xenial to complete the installation on Mate.
