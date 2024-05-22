.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

.. _rgb_strip:

WS2812 RGB Strip
=======================

**Pin Selection**

#. Raspberry Pi has three high-speed signal driving mode that can be used to drive WS2812 RGB LED strip. But these modes have other uses, and using them for WS2812 RGB LED strip will disable their original functions.
 

    .. image:: img/strip_select.png


    * SPI (IO10) is used for SPI interface. 
    * PWM (IO12) for analog audio (3.5mm audio jack). 
    * PCM (IO21) for digital audio (HDMI audio). 

#. The SPI (IO10) drive mode is selected by default. If you switch to a different pin (let's say IO21) during the assembly process, you will also need to modify the corresponding configuration.

    .. code-block:: shell

        pironman -rp 21

**Other Configurations**

The WS1812 RGB Strip is a light strip with 8 RGB LEDs that can be used to display Pironman's status. You can use commands to make it turn on or off, or to modify its color (default is blue), display mode and change rate.

* Turn on the WS2812 RGB Strip.

.. code-block:: shell

    pironman  -rw on

* Turn it off.

.. code-block:: shell

    pironman  -rw off

* Change its color, using hexadecimal color values.

.. code-block:: shell

    pironman  -rc fe1a1a

* Changing the display mode, there are four modes to choose from: ``breath``, ``leap``, ``flow``, ``raise_up``.

.. code-block:: shell

    pironman  -rs leap

* Change the speed of change (0 ~ 100%).

.. code-block:: shell

    pironman  -rb 80

* Above are the effects we preset for WS2812 RGB Strip, if you want it to display other effects, you can open ``/opt/pironman/ws2812_RGB.py`` to modify and run it.

    Open this python script and modify its contents.

    .. code-block:: shell

        sudo nano /opt/pironman/ws2812_RGB.py

    Press ``Ctrl+X`` -> ``Y`` -> ``Enter`` to save and exit editing.

    Run it.

    .. code-block:: shell

        sudo python3 /opt/pironman/ws2812_RGB.py