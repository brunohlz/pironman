.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

5. Pironman einrichten
===================================

.. note::
    * Dieser Pironman funktioniert wie ein PC und benötigt den Power-Button zum Ein-/Ausschalten.

.. _change_config:

Kompatible Systeme
-----------------------------------

Die kompatiblen Systeme für Pironman sind unten dargestellt.

.. image:: img/compitable_system.png

Sollten Ihre Systeme ``git``, ``python3`` und ``pip`` noch nicht vorinstalliert haben, müssen Sie diese zuerst installieren.

.. code-block:: shell

    sudo apt-get update
    sudo apt-get install git -y
    sudo apt-get install python3 python3-pip python3-setuptools -y


``pironman`` Modul installieren
----------------------------------

Verwenden Sie die folgenden Befehle, um das ``pironman`` Modul herunterzuladen und zu installieren.

.. code-block:: shell

    cd ~
    git clone https://github.com/sunfounder/pironman.git -b v2.0
    cd ~/pironman
    sudo python3 install.py

.. warning::  Die Angabe ``-b v2.0`` im Befehl ist notwendig.

Ein Neustart ist nach der Installation erforderlich. Eine Aufforderung zum Neustart wird irgendwann erscheinen, und Sie können ``y`` auswählen, um sofort oder später neu zu starten.

Hier sind die Grundkonfigurationen für Pironman.

   * Das OLED-Display zeigt die CPU-, RAM- und ROM-Auslastung, die CPU-Temperatur und die IP-Adresse des Raspberry Pi an.
   * Nach 60 Sekunden geht das OLED-Display in den Schlafmodus. Sie können es durch einen kurzen Druck auf den Power-Button wieder aufwecken.
   * Der Lüfter wird bei 50 Grad Celsius eingeschaltet.
   * Schalten Sie den WS2812 RGB-Streifen (standardmäßige Verbindung in IO10) ein, sodass er in der Farbe #0a1aff (blau) und im Atemmodus (Änderungsrate beträgt 50%) leuchtet.
   * Zu diesem Zeitpunkt können Sie 2 Sekunden lang drücken, um sicher herunterzufahren oder 10 Sekunden lang, um erzwungen herunterzufahren.


Konfiguration ändern
-----------------------------

Im ``pironman`` Modul haben wir einige Grundkonfigurationen für Pironman. Sie können diese mit dem folgenden Befehl überprüfen.

.. code-block:: shell

    pironman -c

Die aktuellen Konfigurationen sind unten aufgeführt.

   * Der Lüfter wird bei 50 Grad Celsius eingeschaltet.
   * Die Anzeigedauer des OLED-Displays beträgt 60s, danach wird es in den Schlafmodus versetzt.
   * Schalten Sie den WS2812 RGB-Streifen (Standardwert 10) ein, sodass er in der Farbe #0a1aff leuchtet und im Atemmodus (Änderungsrate beträgt 50%) angezeigt wird.

.. image:: img/pironman_c.jpg
    :align: center

Sie können diese Konfigurationen auch nach Ihren Bedürfnissen anpassen.

Verwenden Sie ``pironman``, ``pironman -h`` oder ``pironman --help``, um die Anweisungen anzuzeigen, wie folgt.

.. code-block:: shell

    Nutzung:
        pironman <OPTION> <Eingabe>

    Optionen:
        start            starte den pironman Service

        stop             stoppe den pironman Service

        restart          starte den pironman Service neu

        -h,--help        Hilfe, zeigt diese Hilfe an

        -c,--check       zeigt alle Konfigurationen an

        -a,--auto        [ an ], aktiviere das automatische Starten beim Booten
                         [ aus ], deaktiviere das automatische Starten beim Booten

        -u,--unit        [ C/F ], setzt die Temperatureinheit,
                             C oder F (Celsius/Fahrenheit)

        -f,--fan         [ Temperatur ], Temperatur, bei der der Lüfter eingeschaltet wird,
                         in Celsius (Standardwert 50), im Bereich (30 ~ 80)

        -al,--always_on  [an/aus], ob der Bildschirm immer eingeschaltet ist,
                         Standardwert ist False

        -s,--staty_time  [Zeit], Anzeigedauer des Bildschirms in Sekunden,
                         in Sekunden, Standardwert 30

        -rw,--rgb_sw     [an/aus], RGB-Streifenschalter

        -rs,--rgb_style  RGB-Streifenanzeigestil, Standard: Atem,
                         in [Atem / Sprung / Fluss / Erheben / Bunt]

        -rc,--rgb_color  [(HEX)Farbe], setze die Farbe des RGB-Streifens,
                         Standard: 0a1aff

        -rb,--rgb_speed  [Geschwindigkeit], RGB-Blinkgeschwindigkeit (0 ~ 100, Standard 50)

        -pwm,--rgb_pwm   [Frequenz], RGB-Signalfrequenz (400 ~ 1600, Standard 1000 kHz)

        -rp,--rgb_pin    [Pin], RGB-Signalkabel, könnte [10 / spi/ SPI / 12 / pwm/ PWM] oder
                         [21 / pcm / PCM], Standard 10 sein


Zum Beispiel, um die automatische Programmausführung beim Start zu deaktivieren.

.. code-block:: shell

    pironman -a aus

Oder setzen Sie die Farbe des WS2812 RGB-Streifens zurück.

.. code-block:: shell

    pironman -rc ff8a40


Diese Konfigurationen werden in ``/opt/pironman/config.txt`` gespeichert, und Sie können auch direkt in dieser Datei Änderungen vornehmen.

.. code-block:: shell

    sudo nano /opt/pironman/config.txt


.. image:: img/pironman_config.jpg
    :align: center

Drücken Sie ``Ctrl+X`` -> ``Y`` -> ``Enter``, um das Bearbeiten zu speichern und zu beenden.

.. note::
    Die Einführung und Konfiguration der Pironman-Komponenten finden Sie unter: :ref:`about_hardware`.

