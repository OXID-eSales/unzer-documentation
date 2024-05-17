Unzer Payment für OXID V. 1.2
=============================

.. todo: #DR: Datum bestimmen

Release-Datum: #tbd

Neue oder geänderte Funktionen
------------------------------

.. todo: #tbd EN: Unzer Installment

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

* Speichern von unterbrochenen Bestellungen

  .. todo: #ML: Feature oder Bugfix?: "If customers - for whatever reason - interrupt the order in the checkout, the order is still saved using a temporary order and Unzer's webhook"
        Was ist der Hintergrund?, Auswirkung? (https://github.com/OXID-eSales/unzer-module/blob/b-6.3.x/CHANGELOG.md#120---unreleased---2024--)
  .. todo: #ML: Müssen wir den Effekt illustrieren? = Loberon

* Behebung des Loberon-Bugs

  .. todo: #ML: Um welches Symptom geht es beim Loberon-Bug? -- Bugfix

  Weitere Informationen finden Sie unter :ref:`konfiguration:Sonstiges: Zeitgrenze für das Erstellen von Bestellungen anpassen`


.. todo: #tbd: URL Changelog verifizieren

Weitere Informationen finden Sie im Changelog (GitHub) unter https://github.com/OXID-eSales/unzer-module/blob/v1.2.0/CHANGELOG.md.

Update
------

Um die Funktionen und Korrekturen von :productname:`Unzer Payment für OXID` V. 1.2.0 und höher zu nutzen, machen Sie ein Update.

|prerequisites|

.. todo: #ML/#ES: Kann ich direkt von 1.0 updaten?

* Sie haben OXID eShop V. 6.3.x bis 6.5.x.
* Sie haben Unzer Payment für OXID V. 1.x.

|procedure|

1. Führen Sie den folgenden Befehl aus.

   .. code:: bash

      composer update

#. Um die neue Zahlungsart Unzer Ratenkauf zu nutzen, lassen Sie sie freischalten.

   Weitere Informationen finden Sie unter :ref:`einfuehrung:Wo finde ich weitere Informationen?`