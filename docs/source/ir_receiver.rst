.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

IR Receiver
================

.. note::
    The IR receiver is connected to GPIO13, if you want to change it to another pin, please refer to :ref:`change_config`.

Before you can use IR receiver, you need to test its connection and install the relevant module.

#. Use the following command to test, if there is a display device then the configuration is successful.

    .. code-block:: shell

        sudo ls /dev |grep lirc

#. Install the ``lirc`` module.

    .. code-block:: shell

        sudo apt-get install lirc -y

#. Run the following command, and if you press a key on the remote controller, the code of the corresponding key will be printed.

    .. code-block:: shell

        mode2 -d /dev/lirc0

.. note::
    If you want to play Kodi on Raspberry Pi, please refer to: :ref:`kodi_osmc`.