.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

Power Button
==================================

.. note::
    The power button is connected to GPIO26, if you want to change it to another pin, please refer to :ref:`change_config`.

The power button can be used to wake up the OLED screen or to turn the Pironman off.

* Upon power-up, the OLED screen displays for 60 seconds before going into sleep mode. Using the power button, you can wake up the OLED screen again later.

* You have 2 ways to get the Pironman to shut down.

    #. Force Shutdown

        Pressing and holding the power button for 10 seconds will let the Pironman power cut, but this method may damage the Raspberry Pi's files or leave some changes unsaved.

    #. Safe Shutdown

        There is also a way to safely turn off the Pironman by pressing and holding the power button for 2 seconds after configuring it.
