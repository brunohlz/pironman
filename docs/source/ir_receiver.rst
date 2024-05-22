.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

IR-Empfänger
================

.. note::
    Der IR-Empfänger ist an GPIO13 angeschlossen. Wenn Sie ihn an einen anderen Pin anschließen möchten, beziehen Sie sich bitte auf :ref:`change_config`.

Bevor Sie den IR-Empfänger verwenden können, müssen Sie seine Verbindung testen und das relevante Modul installieren.

#. Verwenden Sie den folgenden Befehl zum Testen. Wenn ein Anzeigegerät vorhanden ist, war die Konfiguration erfolgreich.

    .. code-block:: shell

        sudo ls /dev |grep lirc

#. Installieren Sie das ``lirc`` Modul.

    .. code-block:: shell

        sudo apt-get install lirc -y

#. Führen Sie den folgenden Befehl aus, und wenn Sie eine Taste auf der Fernbedienung drücken, wird der Code der entsprechenden Taste angezeigt.

    .. code-block:: shell

        mode2 -d /dev/lirc0

.. note::
    Wenn Sie Kodi auf dem Raspberry Pi verwenden möchten, beziehen Sie sich bitte auf: :ref:`kodi_osmc`.
