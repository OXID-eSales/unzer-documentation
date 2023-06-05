Unzer Payment für OXID V. 1.1
=============================

Release-Datum: 02.06.2023

Neue oder geänderte Funktionen
------------------------------

* Nutzen Sie die Buy Now, Pay Later-Zahlungsart :productname:`Unzer Kauf auf Rechnung (Paylater)`.

  .. todo: #EC: Stimmt die folgende Aussage? Was ist aus Altkundensicht der Unterschied zu Unzer Kauf auf Rechnung (Paylater), welche Vorteile habe ich durch einen Umstieg?
        Zusätzlich zum bisherigen Zahlen auf Rechnung ermöglichen Sie Ihren Kunden damit auch Ratenkauf und Bezahlen per Lastschrift.

  .. todo: #EC/#ML: Als Altkunde: Kann ich Unzer Kauf auf Rechnung und Unzer Kauf auf Rechnung (Paylater) parallel nutzen, oder muss ich ich entscheiden und dann entsprechend neu konfigurieren?

  .. todo: #EC: Ist das die offizielle URL/Infoquelle zu Unzer Kauf auf Rechnung (Paylater)?: https://docs.unzer.com/payment-methods/ ?

  Weitere Informationen finden Sie unter `docs.unzer.com/payment-methods <https://docs.unzer.com/payment-methods/>`_.

  Um :productname:`Unzer Kauf auf Rechnung (Paylater)` zu nutzen, tun Sie Folgendes:

  1. Kontaktieren Sie Ihren Ansprechpartner bei Unzer und vereinbaren Sie die gewünschten Kombination von Währung und Kundentyp.
     |br|
     Sie erhalten von Unzer die privaten und öffentlichen Schlüssel für den Sandbox- und Livebetrieb.
  2. Konfigurieren Sie :productname:`Unzer Kauf auf Rechnung (Paylater)` wie beschrieben unter :ref:konfiguration:Unzer konfigurieren`.

.. todo: Info: Das bisherige SEPA Lastschrift und SEPA Lastschrift (abgesichert mit Unzer) bleibt: wird später geändert.

.. todo: #EC: Muss der Shopbetreiber an dieser Stelle etwas wissen über die unterschiedliche Risikobewerrtung von B2C und B2B-Kunden? Wirkt es sich auf die Konditionen aus oder trägt Unzer das Risiko?  -- muss mit Customer Center besprochen werden; sollte auf docs page beschrieben sein: EC prüft.
        #EC: Was ist die URL der docs page? -- https://docs.unzer.com/payment-methods/ ?

* Beachten Sie Einschränkungen bei den Ländern und Währungen, für die Sie bestimmte Zahlungsarten anbieten können.

  * Die aktuelle gültigen Länder finden Sie unter :ref:`einfuehrung:Welche Märkte sind abgedeckt?`.
  * Die aktuelle gültigen Währungen finden Sie unter :ref:`einfuehrung:Welche Währungen sind abgedeckt?`.

  Weitere Informationen finden Sie im `Changelog <https://github.com/OXID-eSales/unzer-module/blob/v1.1.0/CHANGELOG.md>`_.

Korrekturen
-----------

Korrekturen finden Sie im Changelog (GitHub) unter https://github.com/OXID-eSales/unzer-module/blob/v1.1.0/CHANGELOG.md.


Update
------

Um die Funktionen und Korrekturen von :productname:`Unzer Payment für OXID` V. 1.1.0 zu nutzen, machen Sie ein Update.

Voraussetzungen
^^^^^^^^^^^^^^^

* Sie haben OXID eShop V. 6.1.x bis 6.5.x.
* Sie haben Unzer Payment für OXID V. 1.0.x.

Vorgehen
^^^^^^^^

Führen Sie den folgenden Befehl aus.

.. code:: bash

   composer update
