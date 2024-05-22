.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

4. Raspberry Pi einrichten
============================

Wenn Sie einen Bildschirm haben
---------------------------------

Wenn Sie über einen Bildschirm verfügen, wird es Ihnen leichtfallen, den Raspberry Pi zu bedienen.

**Benötigte Komponenten**

* Ein Raspberry Pi   
* 1 * Netzteil
* 1 * Micro-SD-Karte
* 1 * Bildschirm-Netzteil
* 1 * HDMI-Kabel
* 1 * Bildschirm
* 1 * Maus
* 1 * Tastatur

#. Legen Sie die mit dem Raspberry Pi OS vorbereitete SD-Karte in den Micro-SD-Kartensteckplatz auf der Unterseite Ihres Raspberry Pi ein.

#. Schließen Sie die Maus und die Tastatur an.

#. Verbinden Sie den Bildschirm über den HDMI-Anschluss des Raspberry Pi und stellen Sie sicher, dass Ihr Bildschirm an eine Steckdose angeschlossen und eingeschaltet ist.

    .. note::

        Wenn Sie einen Raspberry Pi 4 verwenden, müssen Sie den Bildschirm an den HDMI0-Anschluss anschließen (am nächsten zum Stromanschluss).

#. Verwenden Sie das Netzteil, um den Raspberry Pi mit Strom zu versorgen. Nach einigen Sekunden wird der Raspberry Pi OS-Desktop angezeigt.

    .. image:: img/login1.png
        :align: center

.. _no_screen:

Wenn Sie keinen Bildschirm haben
-----------------------------------

Wenn Sie keinen Monitor haben, können Sie sich aus der Ferne in Ihren Raspberry Pi einloggen.

Sie können den SSH-Befehl verwenden, um die Bash-Shell des Raspberry Pi zu öffnen. Bash ist die standardmäßige Shell für Linux. Die Shell selbst ist ein Befehl (Anweisung), wenn der Benutzer Unix/Linux verwendet. Die meisten Aufgaben können über die Shell erledigt werden.

Wenn Sie nicht nur über das Befehlsfenster auf Ihren Raspberry Pi zugreifen möchten, können Sie auch die Funktion des Remote-Desktops verwenden, um Dateien auf Ihrem Raspberry Pi über eine grafische Benutzeroberfläche zu verwalten.

Unten finden Sie ausführliche Anleitungen für jedes System.


.. toctree::

    remote_macosx
    remote_windows
    remote_linux

