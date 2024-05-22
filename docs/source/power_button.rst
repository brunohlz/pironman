.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Ein/Aus-Taste
==================================

.. note::
    Die Ein/Aus-Taste ist an GPIO26 angeschlossen. Wenn Sie sie an einen anderen Pin anschließen möchten, beziehen Sie sich bitte auf :ref:`change_config`.

Die Ein/Aus-Taste kann verwendet werden, um den OLED-Bildschirm zu wecken oder den Pironman auszuschalten.

* Nach dem Einschalten wird der OLED-Bildschirm für 60 Sekunden angezeigt, bevor er in den Schlafmodus wechselt. Mit der Ein/Aus-Taste können Sie den OLED-Bildschirm später wieder aufwecken.

* Es gibt 2 Möglichkeiten, den Pironman herunterzufahren.

    #. Erzwungener Shutdown

        Wenn Sie die Ein/Aus-Taste 10 Sekunden lang gedrückt halten, wird die Stromversorgung des Pironman unterbrochen. Diese Methode kann jedoch Dateien des Raspberry Pi beschädigen oder einige Änderungen nicht speichern.

    #. Sicherer Shutdown

        Es gibt auch eine Möglichkeit, den Pironman sicher auszuschalten, indem Sie die Ein/Aus-Taste nach der Konfiguration 2 Sekunden lang gedrückt halten.

