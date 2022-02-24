Installation
============



Installation durchführen
------------------------

Installieren Sie das Unzer Payment-Modul für OXID für den OXID eShop ab Version 6.3.

|prerequisites|

* Sie haben den OXID eSHOP 6.3 oder höher installiert.`
* Sie haben Transportverschlüsselung (`https`) konfiguriert.

   a. Öffnen Sie im Verzeichnis `<Rootverzeichnis des eShops>/source` die Datei `config.inc.php`.
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

      composer require oxid-solution-catalysts/unzer:dev-b-6.3.x

.. todo: #Johannes#Mario: Wenn produktiv, dann composer require oxid-solution-catalysts/unzer ?

3. Bestätigen Sie die Abfragen.

|result|

Sobald der Installationsprozess abgeschlossen ist, erscheint das Modul im Administrationsbereich unter :menuselection:`Erweiterungen --> Zahlungsarten`.


.. todo: #tbd Bild ergänzen

.. todo: Nächster Schritt Konfiguration


Installation abschließen
------------------------

.. todo: #Mario/#Johannes: Schritt sinnvoll/überflüssig?

Löschen Sie temporäre Dateien.
|br|
Löschen Sie dazu alle Dateien und Ordner außer :file:`.htaccess` aus dem Verzeichnis :file:`/tmp` des Shops.




.. Intern: oxdaab, Status: