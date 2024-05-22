.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

Main Board
================

**About the Ports**

.. image:: img/main_board_1.png


**About the Pins**

.. note::
   Two channels of fan pins are provided, allowing you to assemble a fan in both the front and back of the Pironman at the same time.

.. image:: img/main_board_2.png
    :width: 800

There are 5 jumper caps on the Main Board, each jumper cap corresponds to a function, if you do not need the function and want to use the pin elsewhere, you can unplug the jumper cap. The following is a detailed explanation of the functions of the five jumper caps.


* **Enable Power Button**: If you pull out this jumper cap, the power button will not work. Besides, the power button is also used to wake up the OLED screen in Sleep Mode.

* **Shutdown Signal (IO26)**: The Main board powers on/off depending on the level of the ``State`` pin; when ``State`` is low, it powers on, and when ``State`` is high, it powers off.

    * You can only turn off the main board by pressing and holding the power button for 10 seconds if you connect GND and state with a jumper cap. 
    * If you connect ``State`` and IO26 with a jumper cap, after configuration, the Raspberry Pi can control the ``State`` pin through IO26. When Raspberry Pi is on, ``State`` will be set to low level, when Raspberry Pi is off, ``State`` will be set to high level, so the motherboard and Raspberry Pi can power on/off synchronously.

* **WS2812 Pin Select**: Raspberry Pi has three high-speed signal driving mode that can be used to drive WS2812 RGB LED strip. But these modes have other uses, and using them for WS2812 RGB LED strip will disable their original functions.

        * PCM (IO21) for digital audio (HDMI audio). 
        * SPI (IO10) is used for SPI interface. 
        * PWM (IO12) for analog audio (3.5mm audio jack). 

    The SPI (IO10) drive mode is selected by default. If you switch to a different pin (let's say IO21) during the assembly process, you will also need to modify the corresponding configuration.

        .. code-block:: shell

            pironman -rp 21


* **Enable Fan**: Insert the jumper to enable fan control; remove the jumper to turn off the fan.


* **Enable IR Receiver**: If you pull out this jumper cap, the IR Receiver will not work.


**Power Cut Memory**

When the Pironman suddenly loses power, the chip of the Main Board will record this state and will automatically power on the next time.