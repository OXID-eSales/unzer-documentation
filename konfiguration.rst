Konfiguration
=============

Machen Sie das Unzer Payment-Modul für OXID betriebsbereit:

1. Aktivieren Sie das Modul.
2. Stellen Sie unter :guilabel:`Zugangsdaten` die Verbindung zu Ihrem Unzer-Händlerkonto her.
3. Optional: Konfigurieren Sie bei Bedarf unter :guilabel:`Zahlungsarten`, dass Zahlungen verzögert ausgelöst werden sollen (beispielsweise bei Geschäftskunden).
3. Prüfen Sie, Ob das Theme Ihres eShops jQuery nutzt. 
   Wenn das nicht der Fall ist, binden Sie jQuery unter :guilabel:`Sonstiges` über das Modul ein.
4. Verknüpfen Sie die von Unzer bereitgestellten Zahlungsarten mit Ihren Versadarten und Versandkostenregelen und führen Sie Testzahlungen in der Unzer-Sandbox aus.
   Hinweis: Die Betriebsart ``Sandbox`` ist nach dem Aktivieren standardmäßig eingestellt.
5. Wenn Sie Ihre Tests abgeschlossen haben, wechseln Sie unter :guilabel:`Umgebung` in die Betriebsart ``Livebetrieb``.


Unzer aktivieren
----------------

|procedure|

1. Wählen Sie :menuselection:`Erweiterungen --> Module`. 
2. Wählen Sie das Modul `Unzer Payment-Modul für OXID` und wählen Sie :menuselection:`Stamm --> Aktivieren`.
3. Optional: #tbd


|result|

.. todo:  Screenshot ergänzen


Zugangsdaten
------------

Registrieren Sie einen Webhook, um Ihren eShop mit Unter zu verbinden. 

Im ersten Durchgang testen Sie die mit Unzer bereitgestellten Zahlungsarten mit Test-Zugangsdaten in einer Sandbox. 

Erst wenn alles nch Ihren Vorstellungen funktioniert, nutzen Sie die Zugangsdaten für den Produktionsbetrieb.


|prerequisites|

* Sie haben bei ein Händlerkonto eingerichtet und folgende Daten erhalten:

   * Sandbox Public-Key
   * Sandbox Private-Key   
   * Sandbox Api-Key
   * Production Public-Key
   * Production Private-Key
   * Production Api-Key 
   
   Weitere Informationen zum Registrieren bei Unzer finden Sie unter #Mario: Unzer Link  https://www.unzer.com/de/direct/
   
|procedure|

1. Wählen Sie :menuselection:`Erweiterungen --> Module --> Unzer Payment-Modul für OXID`.
2. Geben Sie unter :menuselection:`Einstell. --> Zugangsdaten` die von Unzer bereitgestellten Keys in die entsprechenden Felder ein.
   #Mario: wozu ist der API-Key? 
   #Mario: Was ist ein Webhook?
3. Wählen Sie die Schaltfläche :guilabel:`Webhook für diesen Shop registrieren`.

|result|

Die URL Ihres registrierten Webhooks wird angezeigt. Ihr Shop ist mit Unzer verbunden. 

.. todo: Screenshot einfügen


Umgebung
--------

Legen Sie den Betriebsmodus fest.

Standardmäßig ist der Betriebsmodus :guilabel:`Sandbox` eingestellt.

Nachdem Sie die Funktionen des Moduls konfiguriert und getesten haben, schalten Sie auf :guilabel:`Livebetrieb` um. 

|procedure|

1. Wählen Sie unter :menuselection:`Einstell. --> Umgebung` den gewünschten Betriebsmodus.
   Um Testzahlungen auszuführen, stellen Sie sicher, dass :menuselection:`Einstell. --> Sandbox` gewählt ist. 
2. Optional: Um während des Testen Logs zu geneieren, markieren Sie das Kontrollkästchen :guilabel:`Debug-Modus aktivieren`.
   Die Log-Dateien finden Sie im Verzeichnis ``log/unzer``. #tbd: prüfen, ob das Verzeichnis angelegt wird, unter source oder modules ist es nicht 
3. Um unnötigen Speicherplatzverbrauch zu vermeiden, stellen Sie sicher, dass im Livebetrieb der Debug-Modus deaktiviert ist.

.. todo: #Mario: Was ist der Anwendungsfall für  "Webhook für diesen Shop löschen" wählen, um neue Keys einzugeben? 


Zahlungsarten
-------------

Legen Sie fest, ob für den eShop Zahlungen sofort eingezogen werden sollen, oder ob die Zahlungen nur reserviert werden sollen.

|example| 

Sie haben einen eShop für Geschäftskunden. Hier sind die Liefermengen und Zahlungsbeträge größer als bei Privatkunden.

Im Fall eines Fehler wäre das Retourenmanagement entsprechend schwieriger.

Deshalb wollen Sie sicherstellen, dass die Zahlung nur ausgelöst wird, wenn die Ware da oder auf dem Weg zum Versand ist. 

|procedure|

1. Wählen Sie :menuselection:`Einstell. --> Zahlungsarten`.
2. Sie haben folgende Möglichkeiten:
   a. Um Zahlungen direkt auszuösen, wählen Sie :guilabel:`direct Capture`.
   b. Um die Zahlung nur zu reservieren und später auszulösen, wählen Sie :guilabel:`Authorize & later Capture`.

.. todo: #Mario: Paypal/Kreditkarte: Mit einer der beiden Zahlungsformen ist der Kunde bei Unzer registriert, korrekt? Gibt es einen Anwendungsfall in dem ich unterschiedliche Zahlungsarten (derect/Authorize) konfigurieren?   
.. todo: #Mario: welches Ereignois löst bei Reservierung die tatsächliche Zahlung aus?   
   
3. Legen Sie den Zinssatz für Ratenzahlungen fest. 

.. todo: #Mario: Wie kriegt der Kunde den Ratenzahlungszinssatz mit, wie wird es abgerechnet/von Unzereingezogen?

.. todo: #Mario: das sieht hier nach einer globalen Einstellung aus: sinnvoll für B2B Sub-Shop, direct capturedagegen  bei B2C-Subshop? nach einer müsste damit zusammenspielen, wie ich Zahlungsarten konfigurieren; #tbd: Hintergrund/Zuammmenhang klären


Sonstiges
---------

Unzer nutzt für Formulareingaben jQuery.

Um Interferenzen mit anderen Modulen zu vermeiden, stellen Sie sicher, dass jQuery nicht doppelt aktiviert ist.

#Mario: was passiert, wenn mein Theme jQuery nicht hat und ich es nicht aktiviere? Wie können Interfereznen aussehen, wenn ich es aktiviere, obwohl es schon im Theme ist?

|procedure|

1. Wählen Sie :menuselection:`Einstell. --> Sonstiges`.

2. Tun Sie Folgendes:
   * Wenn Ihr Theme jQuery benutzt, stellen Sie sicher, das das Kontrollkästchen :guilabel:`Einbindung von jQuery über das Modul` deaktiviert ist.
   * Wenn Ihr Theme jQuery **nicht** benutzt, stellen Sie sicher, das das Kontrollkästchen :guilabel:`Einbindung von jQuery über das Modul` aktiviert ist.

















.. Intern: oxdaac, Status: