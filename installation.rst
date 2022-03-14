Installation
============

.. todo: #Mario: ab V. 6.2?

Installieren Sie das Unzer Payment-Modul für OXID für den OXID eShop ab Version 6.3.

|prerequisites|

* Sie haben den OXID eShop 6.3 oder höher installiert.
* Sie haben Transportverschlüsselung (`https`) konfiguriert.

   a. Öffnen Sie im Verzeichnis `<Root-Verzeichnis des eShops>/source` die Datei `config.inc.php`.
   b. Stellen Sie sicher dass für die eShop base URL (Parameter `sShopURL`) https eingestellt ist.
   
      Beispiel:
   
      .. code::
   
         $this->sShopURL     = 'https://192.168.123.20';

|procedure|

1. Öffnen Sie eine Shell und wechseln Sie ins Root-Verzeichnis des Shops (in dem die Datei :file:`composer.json` liegt).
   Beispiel:

   .. code:: bash

      cd /var/www/oxideshop/

2. Führen Sie folgenden Befehl aus: 

   .. code:: bash

      composer require oxid-solution-catalysts/unzer

.. todo: #Mario: Prüfen: ob anderes Repo als Quelle

3. Bestätigen Sie die Abfragen.

|result|

Sobald der Installationsprozess abgeschlossen ist, erscheint das Modul im Administrationsbereich unter :menuselection:`Erweiterungen --> Module`.


.. todo: #tbd Bild ergänzen

.. todo: Nächster Schritt Konfiguration






.. Intern: oxdaab, Status: