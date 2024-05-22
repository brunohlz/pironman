.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

OLED-Bildschirm
===================

Nach der Installation wird das Skript automatisch gestartet und der OLED-Bildschirm zeigt die CPU-, RAM- und ROM-Auslastung, die CPU-Temperatur und die IP-Adresse des Raspberry Pi an.

Um die Lebensdauer des OLED-Bildschirms zu verlängern, schaltet sich der OLED-Bildschirm standardmäßig nach 60 Sekunden aus und wird durch kurzes Drücken des Einschaltknopfes wieder aktiviert. Sie können diese Funktion mit dem folgenden Befehl aktivieren/deaktivieren.

* Schlafmodus einstellen: „al“ bedeutet „immer an“. Im Schlafmodus den Einschaltknopf kurz drücken, um aufzuwachen.

.. code-block:: shell

    pironman  -al off

* Immer-an-Modus einstellen:

.. code-block:: shell

    pironman  -al on

* Dauer in Sekunden festlegen:

.. code-block:: shell

    pironman  -s 60

* Das oben Genannte sind unsere Einstellungen für den OLED-Bildschirm. Wenn Sie möchten, dass der OLED-Bildschirm andere Informationen und Effekte anzeigt, können Sie ``/opt/pironman/main.py`` öffnen, ändern und ausführen.

    Öffnen Sie dieses Python-Skript und ändern Sie den Inhalt.

    .. code-block:: shell

        sudo nano /opt/pironman/main.py

    Drücken Sie ``Ctrl+X`` -> ``Y`` -> ``Enter``, um zu speichern und die Bearbeitung zu beenden.

    Führen Sie es aus.

    .. code-block:: shell

        sudo python3 /opt/pironman/main.py
