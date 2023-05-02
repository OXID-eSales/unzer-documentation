Unzer Payment für OXID V. 1.1
=============================

.. todo: #DP: wann ist Release?

Release-Datum: 30.05.2023

Neue oder geänderte Funktionen
------------------------------

* Nutzen Sie die Buy Now, Pay Later-Zahlungsart :productname:`Unzer upaylater`.

  Zusätzlich zum bisherigen Zahlen auf Rechnung ermöglichen Sie Ihren Kunden damit auch Ratenkauf und Bezahlen per Lastschrift.

  Weitere Informationen finden Sie unter `Buy Now, Pay Later <https://www.unzer.com/de/press/articles/unzer-launches-buy-now-pay-later/>`_.

  Um :productname:`Unzer upaylater` zu nutzen, tun Sie Folgendes:

  1. Kontaktieren Sie Ihren Ansprechpartner bei Unzer und vereinbaren Sie die gewünschten Kombination von Währung und Kundentyp.
     |br|
     Sie erhalten von Unzer die privaten und öffentlichen Schlüssel für den Sandbox- und Livebetrieb.
  2.

.. todo: #tbd: Für 2.0: Wie ist es bei Neukunden:

.. todo: #EC: Das bisherige "Unzer Kauf auf Rechnung" so lassen oder umbenennen, z.B. "Unzer Kauf auf Rechnung (alt)": In welchem Anwendungsfall verwende ich das alte und das neue PayLater?: mit Unzer klären; vermutlich keine neuen Abschlüsse mit der alten Zahlungsart

.. todo: #EC: Das bisherige SEPA Lastschrift und SEPA Lastschrift (abgesichert mit Unzer) abgedeckt durch upaylater?

.. todo: #EC: Muss der Shopbetreiber an dieser Stelle etwas wissen über die unterschiedliche Rsikobewerrtung von B2C und B2B-Kunden? Wirkt es sich auf die Konditionen aus oder trägt Unzer das Risiko?



Korrekturen
-----------

.. todo: #ML: Gibt es bug fixes in 1.1?

Korrekturen finden Sie im Changelog (GitHub) unter https://github.com/OXID-eSales/unzer/blob/v1.1.0/CHANGELOG.md.


Update
------

Um die Funktionen und Korrekturen von :productname:`Unzer Payment für OXID` V. 1.1.0 zu nutzen, machen Sie ein Update.

Voraussetzungen
^^^^^^^^^^^^^^^

* Sie haben OXID eShop V. 6.1.x bis 6.5.x.

Vorgehen
^^^^^^^^

.. todo: #ML/tbd: verifizieren

Führen Sie den folgenden Befehl aus.

.. code:: bash

   composer update
