.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

Cooling Fan
=====================

.. note::
    The Cooling Fan  is connected to GPIO6 (BCM).

The working status of the Cooling Fan is decided by the CPU temperature. When the CPU temperature reaches the set threshold, the fan spins, and if it is 2 degrees Celsius below the threshold, the fan is stopped.

* Set the temperature unit, ``C``: Celsius, ``F``: Fahrenheit.

.. code-block:: shell

    pironman  -u C


* Set the temperature at which the fan starts, for example, 40 degrees Celsius (the unit is set by you).

.. code-block:: shell

    pironman  -f 40