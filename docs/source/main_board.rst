.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Hauptplatine
================

**Über die Anschlüsse**

.. image:: img/main_board_1.png

**Über die Pins**

.. note::
   Es werden zwei Kanäle für Lüfterpins bereitgestellt, sodass Sie gleichzeitig einen Lüfter sowohl vorne als auch hinten am Pironman anbringen können.

.. image:: img/main_board_2.png
    :width: 800

Auf der Hauptplatine befinden sich 5 Jumper-Kappen. Jede Jumper-Kappe entspricht einer Funktion. Wenn Sie die Funktion nicht benötigen und den Pin anderweitig verwenden möchten, können Sie die Jumper-Kappe abziehen. Im Folgenden wird die Funktion der fünf Jumper-Kappen detailliert erläutert.

* **Einschaltknopf aktivieren**: Wenn Sie diese Jumper-Kappe herausziehen, funktioniert der Einschaltknopf nicht. Außerdem wird der Einschaltknopf verwendet, um den OLED-Bildschirm im Schlafmodus zu wecken.

* **Herunterfahren Signal (IO26)**: Die Hauptplatine schaltet je nach Pegel des ``State``-Pins ein/aus; wenn ``State`` niedrig ist, schaltet sie ein, und wenn ``State`` hoch ist, schaltet sie aus.

    * Sie können die Hauptplatine nur ausschalten, indem Sie den Einschaltknopf 10 Sekunden lang gedrückt halten, wenn Sie GND und State mit einer Jumper-Kappe verbinden.
    * Wenn Sie ``State`` und IO26 mit einer Jumper-Kappe verbinden, kann der Raspberry Pi nach der Konfiguration den ``State``-Pin über IO26 steuern. Wenn der Raspberry Pi eingeschaltet ist, wird ``State`` auf niedrigem Pegel gesetzt, wenn der Raspberry Pi ausgeschaltet ist, wird ``State`` auf hohem Pegel gesetzt, sodass Hauptplatine und Raspberry Pi synchron ein-/ausschalten können.

* **WS2812 Pin Auswahl**: Der Raspberry Pi verfügt über drei Hochgeschwindigkeitssignalantriebsmodi, die zum Ansteuern des WS2812 RGB LED-Streifens verwendet werden können. Diese Modi haben jedoch andere Verwendungszwecke, und ihre Verwendung für den WS2812 RGB LED-Streifen deaktiviert ihre ursprünglichen Funktionen.

        * PCM (IO21) für digitalen Ton (HDMI-Audio).
        * SPI (IO10) wird für die SPI-Schnittstelle verwendet.
        * PWM (IO12) für analogen Ton (3,5mm Audiobuchse).

    Der SPI (IO10)-Antriebsmodus ist standardmäßig ausgewählt. Wenn Sie während des Montageprozesses zu einem anderen Pin wechseln (zum Beispiel IO21), müssen Sie auch die entsprechende Konfiguration ändern.

        .. code-block:: shell

            pironman -rp 21

* **Lüfter aktivieren**: Stecken Sie den Jumper ein, um die Lüftersteuerung zu aktivieren; ziehen Sie den Jumper heraus, um den Lüfter auszuschalten.


* **IR-Empfänger aktivieren**: Wenn Sie diese Jumper-Kappe herausziehen, funktioniert der IR-Empfänger nicht.

**Speicherung des Stromausfalls**

Wenn der Pironman plötzlich den Strom verliert, wird der Chip der Hauptplatine diesen Zustand speichern und beim nächsten Mal automatisch einschalten.
