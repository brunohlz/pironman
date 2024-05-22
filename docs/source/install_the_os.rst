.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _install_os:

3. Betriebssystem installieren (Allgemein)
============================================

.. note::

    Wenn Sie Home Assistance nutzen möchten, folgen Sie bitte :ref:`install_hassos`.

.. note::

    * Wenn Ihr Raspberry Pi bereits eines der folgenden Pironman-kompatiblen Systeme installiert hat, können Sie dieses Kapitel überspringen.

        .. image:: img/compitable_system.png

**Schritt 1**

Raspberry Pi hat ein grafisches SD-Kartenschreibtool entwickelt, das
auf Mac OS, Ubuntu 18.04 und Windows funktioniert. Es ist für die meisten
Benutzer die einfachste Option, da es das Image herunterlädt und automatisch auf die
SD-Karte installiert.

Besuchen Sie die Download-Seite: https://www.raspberrypi.org/software/. Klicken Sie
auf den Link für den **Raspberry Pi Imager**, der zu Ihrem Betriebssystem passt.
Nachdem der Download abgeschlossen ist, starten Sie den Installer.

.. image:: img/image11.png
    :align: center


**Schritt 2**

Wenn Sie den Installer starten, versucht Ihr Betriebssystem möglicherweise, 
dessen Ausführung zu blockieren. Auf Windows erhalten Sie beispielsweise folgende 
Nachricht:

Sollte diese Meldung erscheinen, klicken Sie auf **More info** und dann auf **Run anyway**. 
Folgen Sie dann den Anweisungen zur Installation des Raspberry Pi Imagers.

.. image:: img/image12.png
    :align: center

**Schritt 3**

Stecken Sie Ihre SD-Karte in den SD-Kartensteckplatz Ihres Computers oder Laptops.

**Schritt 4**

Im Raspberry Pi Imager wählen Sie das Betriebssystem aus, das Sie installieren möchten, 
sowie die SD-Karte, auf die Sie es installieren möchten.

.. image:: img/image13.png
    :align: center

.. note:: 

    * Sie müssen beim ersten Mal mit dem Internet verbunden sein.
    * Das Betriebssystem wird dann für die zukünftige Offline-Nutzung gespeichert (``lastdownload.cache``, ``C:/Users/yourname/AppData/Local/Raspberry Pi/Imager/cache``). Wenn Sie die Software das nächste Mal öffnen, wird angezeigt: "Veröffentlicht: Datum, auf Ihrem Computer gespeichert".

.. Laden Sie das `raspios_armhf-2020-05-28 <https://downloads.raspberrypi.org/raspios_armhf/images/raspios_armhf-2021-05-28/2021-05-07-raspios-buster-armhf.zip>`_ Image herunter und wählen Sie es im Raspberry Pi Imager aus.

**Schritt 5**

Wählen Sie die von Ihnen verwendete SD-Karte aus.

.. image:: img/image14.png
    :align: center

**Schritt 6**

Drücken Sie **Ctrl+Shift+X** oder klicken Sie auf das **setting**-Symbol, um die Seite **Advanced options** zu öffnen, SSH zu aktivieren und Benutzernamen sowie Passwort festzulegen.

    .. note::
        * Da der Raspberry Pi kein Standardpasswort mehr hat, müssen Sie es selbst festlegen. Auch der Benutzername kann geändert werden.
        * Für den Fernzugriff müssen Sie SSH auch manuell aktivieren.

.. image:: img/image15.png
    :align: center

Scrollen Sie dann nach unten, um die WLAN-Konfiguration abzuschließen, und klicken Sie auf **SAVE**.

.. note::

    ``WLAN-Land`` sollte auf den zweibuchstabigen `ISO/IEC alpha2-Code <https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements>`_ des Landes eingestellt werden, in dem Sie Ihren Raspberry Pi verwenden.

.. image:: img/image16.png
    :align: center

**Schritt 7**

Klicken Sie auf den Button **WRITE**.

.. image:: img/image17.png
    :align: center

**Schritt 8**

Wenn auf Ihrer SD-Karte derzeit Dateien gespeichert sind, möchten Sie diese Dateien möglicherweise zuerst sichern, um ein dauerhaftes Verlieren zu vermeiden. Wenn es keine Datei zum Sichern gibt, klicken Sie auf **Yes**.

.. image:: img/image18.png
    :align: center

**Schritt 9**

Nach einer Wartezeit wird das folgende Fenster angezeigt, das das erfolgreiche Schreiben signalisiert.

.. image:: img/image19.png
    :align: center




