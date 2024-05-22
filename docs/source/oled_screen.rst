.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

OLED Screen
===================

After installation, the script will start automatically and the OLED screen will display the CPU, RAM and ROM Usage, CPU Temperature and IP Address of the Raspberry Pi.


In order to extend the life of OLED screen, OLED will turn off after 60 seconds by default, and will light up by pressing the power button shortly. You can enable/disable this feature with the following command.

* set to sleep mode:  "al" means to "always on". In sleep mode, short press the power button to wake up.



.. code-block:: shell

    pironman  -al off

* set to always on mode:



.. code-block:: shell

    pironman  -al on

* Set the duration in seconds, 



.. code-block:: shell

    pironman  -s 60

* The above are what we set for OLED screen, if you want to make OLED screen display other information and effects, you can open ``/opt/pironman/main.py`` to modify and run it.

    Open this python script and modify its contents.

    .. code-block:: shell

        sudo nano /opt/pironman/main.py


    Press ``Ctrl+X`` -> ``Y`` -> ``Enter`` to save and exit editing.

    Run it.

    .. code-block:: shell

        sudo python3 /opt/pironman/main.py