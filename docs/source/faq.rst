.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

FAQ
============

Pironman's LED lights up but Raspberry Pi won't boot when power button is pressed?
-------------------------------------------------------------------------------------------

Please check the following conditions.

#. Is there a separate power supply for the Raspberry Pi?

    Please do not do this, for the following reasons.

    Since the Raspberry Pi itself has no on/off control, it can only be powered on by powering up the Raspberry Pi. 
    So Pironman will power off the Raspberry Pi after it is turned off, and power on the Raspberry Pi to start the Raspberry Pi. 
    If you power on both the Raspberry Pi and Pironman, after shutdown, the Pironman has no way to start the Raspberry Pi by powering on the Raspberry Pi because the Raspberry Pi is externally plugged in and always powered on.

#. Is the Micro SD card already inserted into the Pironman slot?
#. Are there any systems installed on Micro SD card?
#. The most important point to note is that the FFC cable of the GPIO Bridge is connected correctly?

    .. image:: img/gpio_bridge1.gif
    .. image:: img/gpio_bridge2.gif

.. _copy_lite:

How to copy Raspberry Pi OS Lite from Micro SD to SSD？
----------------------------------------------------------

#. Updating the Bootloader


    .. code-block:: shell

        sudo apt update
        sudo apt full-upgrade
        sudo rpi-update
        sudo rpi-eeprom-update -d -a

    After setting, reboot to take effect.


#. Use the following command to view the name of the storage device.


    .. code-block:: shell

        sudo fdisk -l

#. You will see a list of all the drives connected to your Raspberry Pi. In most cases, ``/dev/mmcxxx`` refers to your Micro SD card, and ``/dev/sda/`` refers to your SSD.

    .. image:: img/ssd16.png

#. Now, use the following command to clone the system from the Micro SD card to the SATA M.2 SSD.

    .. note::
        Replace ``/dev/mmcblk0`` with the name of your Micro SD card, and also modify ``/dev/sda`` to match the name of your SSD if it has a different name.


    .. code-block:: shell

        sudo dd if=/dev/mmcblk0 of=/dev/sda bs=4M

#. Pull out the Micro SD card, connect the M.2 SATA SSD and then power on the Pironman.