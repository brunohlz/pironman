.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Kühlventilator
=====================

.. note::
    Der Kühlventilator ist an GPIO6 (BCM) angeschlossen.

Der Betriebsstatus des Kühlventilators wird durch die CPU-Temperatur bestimmt. Wenn die CPU-Temperatur den eingestellten Schwellenwert erreicht, beginnt der Ventilator zu laufen. Liegt sie 2 Grad Celsius unter dem Schwellenwert, wird der Ventilator gestoppt.

* Temperatureinheit festlegen, ``C``: Celsius, ``F``: Fahrenheit.

.. code-block:: shell

    pironman  -u C


* Die Temperatur festlegen, bei der der Ventilator startet, z.B. 40 Grad Celsius (die Einheit wird von Ihnen bestimmt).

.. code-block:: shell

    pironman  -f 40