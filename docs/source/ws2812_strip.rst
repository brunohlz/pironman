.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _rgb_strip:

WS2812 RGB-Strip
=======================

**Pin-Auswahl**

#. Der Raspberry Pi verfügt über drei Hochgeschwindigkeitssignal-Treibmodi, mit denen der WS2812 RGB LED-Strip angetrieben werden kann. Diese Modi haben jedoch andere Funktionen und ihre Verwendung für den WS2812 RGB LED-Strip deaktiviert ihre ursprünglichen Funktionen.
 

    .. image:: img/strip_select.png


    * SPI (IO10) dient als SPI-Schnittstelle.
    * PWM (IO12) für analogen Audioausgang (3.5-mm-Audiobuchse).
    * PCM (IO21) für digitalen Audioausgang (HDMI-Audio).

#. Standardmäßig ist der SPI (IO10)-Treibermodus ausgewählt. Wenn Sie während des Montageprozesses auf einen anderen Pin (z.B. IO21) wechseln, müssen Sie auch die entsprechende Konfiguration ändern.

    .. code-block:: shell

        pironman -rp 21

**Weitere Konfigurationen**

Der WS1812 RGB-Strip ist ein Lichtstreifen mit 8 RGB-LEDs, der den Status des Pironman anzeigen kann. Sie können Befehle verwenden, um ihn ein- oder auszuschalten oder um seine Farbe (Standard ist blau), Anzeigemodus und Änderungsrate zu modifizieren.

* Den WS2812 RGB-Strip einschalten.

.. code-block:: shell

    pironman  -rw on

* Ausschalten.

.. code-block:: shell

    pironman  -rw off

* Farbänderung mit hexadezimalen Farbwerten.

.. code-block:: shell

    pironman  -rc fe1a1a

* Anzeigemodus ändern. Es gibt vier Modi zur Auswahl: ``breath``, ``leap``, ``flow``, ``raise_up``.

.. code-block:: shell

    pironman  -rs leap

* Änderungsgeschwindigkeit einstellen (0 ~ 100%).

.. code-block:: shell

    pironman  -rb 80

* Oben sind die von uns voreingestellten Effekte für den WS2812 RGB-Strip. Wenn Sie andere Effekte anzeigen möchten, können Sie ``/opt/pironman/ws2812_RGB.py`` öffnen, modifizieren und ausführen.

    Öffnen Sie dieses Python-Skript und ändern Sie den Inhalt.

    .. code-block:: shell

        sudo nano /opt/pironman/ws2812_RGB.py

    Drücken Sie ``Ctrl+X`` -> ``Y`` -> ``Enter``, um zu speichern und die Bearbeitung zu beenden.

    Führen Sie es aus.

    .. code-block:: shell

        sudo python3 /opt/pironman/ws2812_RGB.py
