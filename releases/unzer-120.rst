Unzer Payment für OXID V. 1.2
=============================

Release-Datum: 26.09.2024

Neue oder geänderte Funktionen
------------------------------

Bieten Sie Ihren Kunden folgende erweiterten Zahlungsmöglichkeiten:

* Neue Zahlungsmethode Unzer Ratenkauf (EUR, CHF) für folgende Länder:

  * Deutschland
  * Niederlande
  * Österreich
  * Schweiz

* Erweiterte Länderabdeckung für SEPA-Lastschrift

  Außer Deutschland und Österreich sind nun auch folgende Länder abgedeckt:

  * Belgien
  * Estland
  * Finnland
  * Frankreich
  * Griechenland
  * Irland
  * Italien
  * Lettland
  * Litauen
  * Luxemburg
  * Malta
  * Niederlande
  * Portugal
  * Slowakei
  * Slowenien
  * Spanien
  * Zypern

Weitere Informationen über die verfügbaren Zahlungsmethoden finden Sie unter :ref:`einfuehrung:Wofür/Wofür nicht?`

Korrekturen
-----------

* Manchmal werden Bestellungen nach dem Bezahlen nicht korrekt abgeschlossen, beispielsweise weil Kunden nicht ins Checkout zurückkehren.

  Das System verhindert diesen Fall durch das automatische Erstellen von Bestellungen nach einer Zeitgrenze.

  Sollte das Problem dennoch auftreten, können Sie den Wert der Zeitgrenze anpassen.

  Weitere Informationen finden Sie unter :ref:`konfiguration:Sonstiges: Zeitgrenze für das Erstellen von Bestellungen anpassen`

Siehe auch das Changelog (GitHub) unter https://github.com/OXID-eSales/unzer-module/blob/v1.2.0/CHANGELOG.md.

Update
------

Um die Funktionen und Korrekturen von :productname:`Unzer Payment für OXID` V. 1.2.0 und höher zu nutzen, machen Sie ein Update.

|prerequisites|

* Sie haben OXID eShop V. 6.3.x bis 6.5.x.
* YSie haben Unzer Payment für OXID V. 1.x.

|procedure|

1. Führen Sie den folgenden Befehl aus.

   .. code:: bash

      composer update

#. Um die neue Zahlungsart Unzer Ratenkauf zu nutzen, lassen Sie sie freischalten.

   Weitere Informationen finden Sie unter :ref:`einfuehrung:Wo finde ich weitere Informationen?`