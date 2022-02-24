Konfiguration
=============

Machen Sie das Unzer Payment-Modul für OXID betriebsbereit.

Grundsätzliches Vorgehen
------------------------

Konfigurieren und testen Sie Unzer. Schalten Sie anschließend den Live-Betrieb ein.

|prerequisites|

* Sie haben gemeinsam mit Unzer die Konditionen vereinbart, ein Händlerkonto eröffnet und von Unzer die Zugangsdaten erhalten.

|procedure|

1. Aktivieren Sie das Modul.
#. Stellen Sie unter :guilabel:`Zugangsdaten` die Verbindung zu Ihrem Unzer-Händlerkonto her.
#. Optional: Konfigurieren Sie bei Bedarf unter :guilabel:`Zahlungsarten`, dass Zahlungen verzögert ausgelöst werden sollen (beispielsweise bei Geschäftskunden).
#. Prüfen Sie, Ob das Theme Ihres eShops jQuery nutzt.
   |br|
   Wenn das nicht der Fall ist, binden Sie jQuery unter :guilabel:`Sonstiges` über das Modul ein.
#. Verknüpfen Sie die von Unzer bereitgestellten Zahlungsarten mit Ihren Versandarten und Versandkostenregeln und führen Sie Testzahlungen in der Unzer-Sandbox aus.
   |br|
   Die Betriebsart ``Sandbox`` ist nach dem Aktivieren standardmäßig eingestellt.
#. Testen Sie Unzer in der Unzer-Sandbox und passen Sie die Konfiguration an, bis alle Zahlungsprozess nach Ihren Vorstellungen funktionieren.
#. Wenn Sie Ihre Tests abgeschlossen haben, wechseln Sie unter :guilabel:`Umgebung` in die Betriebsart ``Livebetrieb``.
#. Wenn Sie die Tests auf einem dedizierten Testsystem durchgeführt haben und Ihren eShop dann in das Produktionssystem umziehen, generieren Sie die Webhooks für die URL des Produktionssystems neu.

Unzer aktivieren
----------------

|procedure|

1. Wählen Sie :menuselection:`Erweiterungen --> Module`. 
2. Wählen Sie das Modul `Unzer Payment-Modul für OXID` und wählen Sie :menuselection:`Stamm --> Aktivieren`.


|result|

Unter :menuselection:`Shopeinstellungen --> Zahlungsarten` sind alle Zahlungsarten, die das Modul :guilabel:`Unzer Payment-Modul für OXID` abdeckt, als aktiv gekennzeichnet.

.. todo: #Bild ergänzen; #Mario: ist das das erwartete Ergebnis?
    .. image:: media/screenshots/oxdaac01.png
    :alt: Unzer Zahlungsarten
    :class: with-shadow
    :height: 344
    :width: 650

Unzer konfigurieren
-------------------

Starten Sie das Konfigurieren.

|procedure|

1. Wählen Sie :menuselection:`Erweiterungen --> Module`.
#. Wählen Sie das Modul :guilabel:`Unzer Payment-Modul für OXID` und wählen Sie :guilabel:`Einstell.`.

Zugangsdaten: Webhook generieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Registrieren Sie einen Webhook, um Ihren eShop mit Unzer zu verbinden.

|prerequisites|

* Sie haben folgende Daten bereitliegen, die Ihnen Unzer mit Einrichtung Ihres Händlerkontos bereitgestellt hat:

   * Sandbox Public-Key
   * Sandbox Private-Key
   * Production Public-Key
   * Production Private-Key

Weitere Informationen zum Registrieren bei Unzer finden Sie unter https://www.unzer.com/de/direct/

.. todo: #Mario verifiziert: Unzer Link  https://www.unzer.com/de/direct/


|procedure|

1. Geben Sie unter :menuselection:`Einstell. --> Zugangsdaten` die von Unzer bereitgestellten Keys in die entsprechenden Felder ein.
#. Wählen Sie die Schaltfläche :guilabel:`Webhook für diesen Shop registrieren`.

.. todo: #Mario: wozu ist der API-Key? -- klären

|result|

Die URL Ihres registrierten Webhooks wird angezeigt. Ihr Shop ist mit Unzer verbunden. 

.. todo: Screenshot einfügen


Zahlungsarten: Reservierung und Ratenzahlungszins festlegen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Legen Sie fest, ob für den eShop Zahlungen sofort eingezogen werden sollen, oder ob die Zahlungen nur reserviert werden sollen.

Geben Sie außerdem den Zinssatz für Ratenzahlungen ein, den Sie mit Unzer vereinbart haben.

|example|

Typischerweise wird das Geld sofort eingezogen.

In bestimmten Fällen ist es sinnvoll, dass die Zahlung erst durch die Auslieferung ausgelöst wird:

* Sie vertreiben bestimmte individualisierte Produkte, die Sie erst nach Eingang der Bestellung herstellen, in Auftrag geben oder bestellen.
* Sie haben einen eShop für Geschäftskunden. Hier sind die Liefermengen und Zahlungsbeträge größer als bei Privatkunden.
  |br|
  Im Fall eines Fehler wäre das Retourenmanagement entsprechend schwieriger.
  |br|
  Deshalb wollen Sie sicherstellen, dass die Zahlung nur ausgelöst wird, wenn die Ware da oder auf dem Weg zum Versand ist.

|procedure|

1. Wählen Sie :menuselection:`Einstell. --> Zahlungsarten`.
#. Sie haben folgende Möglichkeiten:
   a. Um Zahlungen direkt auszulösen, wählen Sie :guilabel:`direct Capture`.
   b. Um die Zahlung nur zu reservieren und später auszulösen, wählen Sie :guilabel:`Authorize & later Capture`.
#. Stellen Sie sicher, dass Sie die den individualisierten Produkten in Ihrem eShop nur die Zahlungsarten :guilabel:`PayPal` oder :guilabel:`Kreditkarte` zugeordnet haben.
   |br|
   Die verzögerte Zahlung für Zahlung per PayPal oder Kreditkarte greift für alle Artikel in Ihrem eShop, denen Sie diese Zahlungsarten zugeordnet haben.
#. Tragen Sie den Zinssatz für Ratenzahlungen ein, den Sie mit Unzer vereinbart haben.

|result|

Wenn Sie für Zahlung per PayPal oder Kreditkarte :guilabel:`Authorize & later Capture` gewählt haben, wird die Zahlung ausgelöst,

* sobald Sie in Ihrem eShop den bestellten Artikel auf den Status `Geliefert` gesetzt haben.
* wenn Sie auf der Unzer-Seite  #tbd

Bei allen anderen von Unzer unterstützten Zahlungsarten wird die Zahlung sofort mit der Bestellung ausgelöst.

.. todo: #Mario: Was passiert, wenn ich einen zu hohen oder zu niedrigen Wert eintrage?
.. todo: #Mario: Welchen Wert trage ich ein, wenn ich keine Ratenzahlung vereinbart habe?
.. todo: #tbd: Prüfen: wie sieht Ratenzahlungsangebt aus Kundensicht aus?

Sonstiges: Optimale Performance sicherstellen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Unzer nutzt für das Validieren von Formulareingaben jQuery.

Um die Performance Ihres OXID eShops nicht zu beeinträchtigen, stellen Sie jedoch sicher, dass jQuery nicht doppelt installiert ist.

|example|

Sie benutzen eines der beiden OXID-Themes `Wave` oder `Fluid`.

Beide OXID-Themes haben jQuery bereits integriert.

Um Interferenzen zu verhindern, stellen Sie sicher, dass jQuery nicht für das Unzer Payment-Modul separat noch einmal eingebunden wird.

|procedure|

1. Prüfen Sie, ob das Theme Ihres OXID eShops jQuery nutzt:

   * Fragen Sie Ihren Web-Frontend-Entwickler.
   * Alternativ: Inspizieren Sie den HTML-Code der Startseite Ihres eShops.
#. Wählen Sie :menuselection:`Einstell. --> Sonstiges`.
#. Tun Sie Folgendes:

   * Wenn Ihr Theme jQuery benutzt, stellen Sie sicher, das das Kontrollkästchen :guilabel:`Einbindung von jQuery über das Modul` deaktiviert ist.
   * Wenn Ihr Theme jQuery **nicht** benutzt, stellen Sie sicher, das das Kontrollkästchen :guilabel:`Einbindung von jQuery über das Modul` aktiviert ist.


Umgebung: eShop testen und Live-Betrieb aktivieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Testen Sie Unzer in der Unzer-Sandbox und passen Sie die Konfiguration an, bis alle Zahlungsprozesse nach Ihren Vorstellungen funktionieren.

Führen Sie dazu Testzahlungen in der Unzer-Sandbox aus.

Der Betriebsmodus :guilabel:`Sandbox` ist standardmäßig eingestellt.

Empfehlung: Nutzen Sie zum Testen ein dediziertes Testsystem. Beachten Sie in diesem Fall die Anweisungen unter :ref:`Webhook löschen und neu anlegen <webhook-loeschen-und-neu-anlegen>`.


|procedure|

1. Optional: Um während des Testen Logs zu generieren, markieren Sie unter :menuselection:`Einstell. --> Umgebung` das Kontrollkästchen :guilabel:`Debug-Modus aktivieren`.
   |br|
   Die Log-Dateien finden Sie im Verzeichnis ``log/unzer``.
#. Nachdem Sie die Funktionen des Moduls konfiguriert und getestet haben, schalten Sie auf :guilabel:`Livebetrieb` um.
#. Um unnötigen Speicherplatzverbrauch zu vermeiden, stellen Sie sicher, dass im Livebetrieb der Debug-Modus deaktiviert ist.

.. todo: #tbd: prüfen, ob das Verzeichnis ``log/unzer`` angelegt wird, unter source oder modules ist es nicht

.. _webhook-loeschen-und-neu-anlegen:

Webhook löschen und neu anlegen
-------------------------------

Wenn Sie Unzer zuerst auf einem Testsystem installiert haben, generieren Sie den Webhook für die URL des Produktionssystems neu.

Sie erhalten sonst auf Ihrem Produktionssystem keine Statusmeldungen, und Sie können die Bestellungen Ihrer Kunden nicht abwickeln.

Stellen Sie außerdem sicher, dass Sie den Webhook auf Ihrem Testsystem löschen.

Auf diese Weise maximieren Sie die Performance Ihrer Unzer-Anbindung.

Löschen und generieren Sie einen Webhook neu auch in dem Fall, dass Sie aus anderen Gründen die URL Ihres OXID eShops geändert haben.

|background|

.. todo: #Mario: Folgendes verifizieren:

Wenn der Webhook auf Ihrem Testsystem auch dann noch aktiv ist, wenn Sie das Testsystem nicht nutzen, werden die Statusmeldungen, die Unzer an ihr Produktionssystem sendet, auch an Ihr Testsystem gesendet.

Dies erzeugt bei Unzer eine unnötige Systemlast auf dem System, das mit Ihrem Webhook verbunden ist. Das kann die Performance Ihrer Unzer-Anbindung vermindern.

|procedure|

1. Tun Sie auf Ihrem dedizierten Testsystem Folgendes:

   a. Wählen Sie :menuselection:`Erweiterungen --> Module --> Unzer Payment-Modul für OXID --> Einstell.`.
   b. Wählen Sie unter :guilabel:`Zugangsdaten` die Schaltfläche :guilabel:`Webhook für diesen Shop löschen`.
#. Wiederholen Sie Schritt 1 auf Ihrem Produktionssystem.
#. Geben Sie unter :guilabel:`Zugangsdaten` Ihre Unzer-Zugangsdaten neu ein.
#. Wählen Sie die Schaltfläche :guilabel:`Webhook für diesen Shop registrieren`.
#. Verifizieren Sie die URL, die als Teil des registrierten Webhooks angezeigt wird.

|result|

Ihr Produktionssystem erhält von Unzer die Statusmeldungen über die Zahlungsvorgänge Ihrer Kunden.
















.. Intern: oxdaac, Status: