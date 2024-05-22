.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _ssd:

SATA M.2 SSD
=====================================

Warum nicht kompatibel mit NVME M.2 SSD?
------------------------------------------

.. note::
    Die M.2 SSD-Festplattenschnittstelle unterstützt nur das SATA-Protokoll, nicht NVME/PCIe.

Unsere aktuelle Schnittstelle wurde für SATA M.2 SSDs entwickelt, und wir möchten erklären, warum wir uns gegen eine Kompatibilität mit NVMe M.2 SSDs entschieden haben:

Der Hauptgrund ist, dass NVMe SSDs in Hochleistungs-Computing-Umgebungen glänzen, die Verarbeitungskapazität und Busbandbreite des Raspberry Pi 4 jedoch begrenzt sind. Das bedeutet, dass selbst wenn eine NVMe SSD angeschlossen wäre, Hardware-Beschränkungen deren Performancevorteile nicht voll ausnutzen könnten, was zu einer suboptimalen Ressourcennutzung führen würde.

Darüber hinaus hat die USB-Stromversorgung des Raspberry Pi 4 ihre Grenzen. Das Anschließen einer NVMe SSD könnte zu einer unzureichenden Stromversorgung führen, insbesondere bei hohen Arbeitslasten. NVMe SSDs benötigen oft höhere Ströme für eine stabile Leistung, aber die USB-Ports des Raspberry Pi 4 könnten diesen Anforderungen nicht gerecht werden, was zu einem instabilen Betrieb der SSD oder sogar zu Funktionsstörungen führen könnte.

Aus diesen Gründen würde das Anschließen einer NVMe SSD keine signifikanten Leistungsverbesserungen bringen. Daher haben wir uns entschieden, die NVMe SSD-Schnittstelle nicht zu unterstützen.

Wir danken Ihnen für Ihr Verständnis unserer Designüberlegungen. Unser Ziel ist es, Ihnen ein Produkt zu bieten, das Ihren Anforderungen gerecht wird und eine reibungslose Erfahrung bietet.

Über das Modell
---------------------------

M.2 SSD (M.2 Solid-State-Drive) gibt es in verschiedenen Modellen, abhängig von ihren Spezifikationen und Leistungsmerkmalen. Hier sind einige gängige M.2 SSD Modelle:

* **M.2 SATA SSDs**: Diese nutzen die SATA-Schnittstelle, ähnlich wie 2,5-Zoll-SATA-SSDs, aber im kleineren M.2-Formfaktor. Sie sind durch die maximalen Geschwindigkeiten von SATA III mit etwa 600 MB/s begrenzt. Diese SSDs sind kompatibel mit M.2-Steckplätzen, die für B- und M-Schlüssel ausgelegt sind.
* **M.2 NVMe SSDs**: Diese SSDs verwenden das NVMe-Protokoll über PCIe-Lanes und sind deutlich schneller als M.2 SATA SSDs. Sie eignen sich für Anwendungen, die hohe Lese-/Schreibgeschwindigkeiten erfordern, wie Gaming, Videobearbeitung und datenintensive Aufgaben. Diese SSDs benötigen in der Regel M-Keyed-Slots. Diese Laufwerke nutzen die PCIe-Schnittstelle (Peripheral Component Interconnect Express) mit verschiedenen Versionen wie 3.0, 4.0 und 5.0. Jede neue Version von PCIe verdoppelt effektiv die Datenübertragungsgeschwindigkeit ihres Vorgängers.


M.2 SSDs gibt es in drei Haupttypen: B-Key, M-Key und B+M-Key. Später wurde jedoch der B+M-Key eingeführt, der die Funktionen des B-Key und M-Key kombiniert. Als Ergebnis ersetzte er den eigenständigen B-Key. Bitte beachten Sie das untenstehende Bild.

.. image:: img/ssd_key.png

Allgemein gesagt sind M.2 SATA SSDs B+M-Key (passen in Sockel für B- und M-Key Module), während M.2 NVMe SSDs für PCIe 3.0 x4 Lane M-Key sind.

.. image:: img/ssd_model2.png

Über die Länge
-----------------------

M.2 Module gibt es in verschiedenen Größen und sie können auch für Wi-Fi, WWAN, Bluetooth, GPS und NFC verwendet werden.

Pironman unterstützt vier M.2 SATA SSD-Größen basierend auf ihren Bezeichnungen: 2230, 2242, 2260 und 2280. Die "22" steht für die Breite in Millimetern (mm), und die beiden folgenden Zahlen sind die Länge. Je länger das Laufwerk, desto mehr NAND-Flash-Chips können montiert werden; daher die größere Kapazität.

.. image:: img/m2_ssd_size.png
    :width: 600

Einbau der SSD
------------------------------

#. Nehmen Sie die Basisplatte des Pironman ab.

    .. image:: img/ssd1.jpg
        :width: 600

#. Entfernen Sie die Schraube für die M.2 SATA SSD.

    .. image:: img/ssd2.jpg

#. Stecken Sie Ihre M.2 SATA SSD ein.

    .. image:: img/ssd3.jpg

#. Schrauben Sie sie fest.

    .. image:: img/ssd4.jpg

#. Setzen Sie die Basisplatte wieder auf.

    .. image:: img/ssd5.jpg

#. Stecken Sie die SSD Bridge und die 5V/3V Stromversorgung ein.

    .. image:: img/ssd18.jpg


**Booten von SSD**
---------------------------
Nachdem Sie die SSD in Ihren Raspberry Pi eingebaut haben, wollen wir uns anschauen, wie Sie das Raspberry Pi Betriebssystem darauf installieren und den Raspberry Pi so konfigurieren, dass er von der SSD startet.

**1. Raspberry Pi OS auf SSD installieren**

Es gibt zwei Möglichkeiten, Raspberry Pi OS auf Ihrer SSD zu installieren:

* Die erste Methode besteht darin, es direkt über den **Raspberry Pi Imager** zu installieren. Dieser Vorgang ähnelt der Installation des OS auf einer Micro-SD-Karte. Wählen Sie einfach Ihre SSD aus, wenn Sie aufgefordert werden, ein Speichergerät zu wählen. Wenn Sie mit diesem Vorgang nicht vertraut sind, können Sie sich das Tutorial :ref:`install_os` ansehen.

* Die alternative Methode besteht darin, von Ihrer vorhandenen SD-Karte zu kopieren. Wenn Sie die Dateien und das System auf Ihrer SD-Karte beibehalten möchten, ist diese Methode ideal für Sie.

Gehen wir Schritt für Schritt durch, wie Sie den Inhalt Ihrer Micro-SD auf die SSD kopieren können:

#. Legen Sie die Micro-SD-Karte in den Pironman ein, schließen Sie die USB-Brücke an, um die SSD mit dem Raspberry Pi zu verbinden, und schalten Sie den Pironman ein.

    .. image:: img/ssd18.jpg

#. Greifen Sie auf den Raspberry Pi Desktop zu. Dies können Sie entweder direkt über einen Monitor tun oder über den Remote-Desktop. Siehe hierzu das Tutorial: :ref:`no_screen`.

#. Starten Sie den **SD Card Copier** aus dem **Accessories**-Bereich des **Start**-Menüs.

    .. image:: img/sd_card_copy.png

#. Wählen Sie das Quellgerät (Micro-SD-Karte) und das Zielgerät (SSD, ``/dev/sda/``) aus. Überprüfen Sie nochmals genau, ob Sie die richtigen Laufwerke ausgewählt haben, und klicken Sie dann auf **"Start"**, um den Kopiervorgang zu beginnen. Dies kann mehrere Minuten dauern.

    .. image:: img/sd_card_copy_select.png

#. Sobald **"Copy Complete"** angezeigt wird, fahren Sie den Raspberry Pi herunter und entfernen Sie die Micro-SD-Karte.

.. note::

    Wenn Ihre Micro-SD-Karte das **Raspberry Pi Lite** ist, müssen Sie Befehle verwenden, um den Kopiervorgang abzuschließen. Für detaillierte Anweisungen verweisen wir auf: :ref:`copy_lite`.

**2. Bootloader installieren**

Da das Raspberry Pi Betriebssystem nun auf der SSD ist, ist es an der Zeit, den Bootloader des Pi zurückzusetzen, um das Booten von USB zu priorisieren.

#. Laden Sie den |link_raspberry_pi_imager| von der Raspberry Pi Webseite herunter und installieren Sie ihn.

#. Legen Sie eine freie Micro-SD-Karte in Ihren Computer ein. Beachten Sie, dass der Inhalt dieser Karte gelöscht wird. Sichern Sie daher zuerst wichtige Daten.

#. Starten Sie den **Raspberry Pi Imager** und scrollen Sie im Bereich **“Operating System”** nach unten zu **“Misc Utility Images”**. Klicken Sie mit der linken Maustaste, um das folgende Menü zu öffnen.

    .. image:: img/ssd6.png
        :width: 600
        :align: center

#. Wählen Sie **Bootloader**.

    .. image:: img/ssd7.png
        :width: 600
        :align: center

#. Wählen Sie anschließend **USB Boot**. Dies bringt uns zurück zum Hauptmenü.

    .. image:: img/ssd8.png
        :width: 600
        :align: center

#. Unter **"Storage"** wählen Sie die Micro-SD-Karte aus. Überprüfen Sie nochmals genau, ob Sie das richtige Laufwerk gewählt haben, bevor Sie fortfahren.

    .. image:: img/ssd88.png
        :width: 600
        :align: center

#. Klicken Sie auf **“WRITE”**, um das Konfigurationsimage herunterzuladen und auf die Micro-SD-Karte zu schreiben.

    .. image:: img/ssd9.png
        :width: 600
        :align: center

#. Warten Sie auf eine erfolgreiche Schreibbestätigung, bevor Sie die Micro-SD-Karte aus Ihrem Computer entfernen.

#. Legen Sie die Micro-SD-Karte in den Pironman ein und schalten Sie ihn ein.

    .. image:: img/connect_power.jpg

#. Sobald das Update abgeschlossen ist, blinkt die grüne Aktivitäts-LED gleichmäßig. Wenn ein HDMI-Monitor angeschlossen ist, wird der Bildschirm nach Abschluss grün. Das Update kann 10 Sekunden oder sogar länger dauern. Stellen Sie daher sicher, dass Sie die Micro-SD-Karte während dieses Prozesses nicht entfernen.

    .. image:: img/ssd10.jpg

#. Schalten Sie den Strom des Raspberry Pi aus und entfernen Sie die Micro-SD-Karte.

**3. Vom SSD booten**

#. Stellen Sie zu diesem Zeitpunkt sicher, dass die Micro-SD-Karte entfernt ist. Verbinden Sie die USB-Brücke, um die SSD mit dem Raspberry Pi zu verbinden. Schalten Sie nun den Pironman ein.

    .. image:: img/login1.png
        :align: center




