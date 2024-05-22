.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Linux/Unix-Benutzer
==========================

#. Navigieren Sie zu **Applications** -> **Utilities**, finden Sie das **Terminal** und öffnen Sie es.

    .. image:: img/image21.png
        :align: center

#. Überprüfen Sie, ob sich Ihr Raspberry Pi im selben Netzwerk befindet, indem Sie ``ping <hostname>.local`` eingeben.

    .. code-block:: shell

        ping raspberrypi.local

    .. image:: img/mac-ping.png
        :width: 550
        :align: center

    * Wenn das Terminal ``ping: cannot resolve <hostname>.local`` anzeigt, könnte es sein, dass der Raspberry Pi keine Verbindung zum Netzwerk herstellen konnte. Bitte überprüfen Sie das Netzwerk.
    * Wenn Sie wirklich nicht ``<hostname>.local`` pingen können, versuchen Sie stattdessen, :ref:`get_ip` zu verwenden und ``ping <IP-Adresse>`` einzugeben (z.B. ``ping 192.168.6.116``).
    * Wenn mehrere Meldungen wie ``64 bytes from <IP-Adresse>: icmp_seq=0 ttl=64 time=0.464 ms`` erscheinen, bedeutet dies, dass Ihr Computer auf den Raspberry Pi zugreifen kann.

#. Geben Sie ``ssh <benutzername>@<hostname>.local`` (oder ``ssh <benutzername>@<IP-Adresse>``) ein.

    .. code-block:: shell

        ssh pi@raspberrypi.local

#. Die folgende Meldung könnte erscheinen:

    .. code-block::

        The authenticity of host 'raspberrypi.local (192.168.6.116)' can't be established.
        ECDSA key fingerprint is SHA256:7ggckKZ2EEgS76a557cddfxFNDOBBuzcJsgaqA/igz4.
        Are you sure you want to continue connecting (yes/no/[fingerprint])? 

    Geben Sie \"yes\" ein.

    .. image:: img/mac-ssh-login.png
        :width: 550
        :align: center

#. Geben Sie das zuvor festgelegte Passwort ein. (Meins ist ``raspberry``.)

#. Der Raspberry Pi ist nun verbunden, und wir können zum nächsten Schritt übergehen.

    .. image:: img/mac-ssh-terminal.png
        :width: 550
        :align: center
