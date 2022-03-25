Installation
============

.. todo: #Mario: ab V. 6.2?

Installieren Sie das Unzer Payment-Modul für OXID für den OXID eShop ab Version 6.3.

|prerequisites|

* Sie haben den OXID eShop 6.3 oder höher installiert.
* Sie haben Transportverschlüsselung (`https`) konfiguriert.

   a. Öffnen Sie im Verzeichnis `<Root-Verzeichnis des eShops>/source` die Datei `config.inc.php`.
   b. Stellen Sie sicher dass für die Basis-URL (Parameter `sShopURL`) https eingestellt ist.
   
      Beispiel:
   
      .. code::
   
         $this->sShopURL     = 'https://www.example.org';

|procedure|

1. Öffnen Sie eine Shell und wechseln Sie ins Root-Verzeichnis des Shops (in dem die Datei :file:`composer.json` liegt).
   Beispiel:

   .. code:: bash

      cd /var/www/oxideshop/


#. Führen Sie folgende Befehle aus:

   .. code:: bash

      composer config repositories.oscunzer composer https://unzer-module.packages.oxid-esales.com/
      composer require oxid-solution-catalysts/unzer ^1.0.0
      composer install
      ./vendor/bin/oe-console oe:module:install-configuration source/modules/osc/unzer
      ./vendor/bin/oe-console oe:module:apply-configuration

#. Optional: Um das Modul zu aktivieren, führen Sie folgenden Befehl aus.
   |br|
   Alternativ: Aktivieren Sie das Modul im Zuge der Konfiguration manuell (siehe :ref:`konfiguration:Unzer aktivieren`).

   .. code:: bash

      ./vendor/bin/oe-console oe:module:activate osc-unzer

#. Bestätigen Sie die Abfragen.



|result|

Sobald der Installationsprozess abgeschlossen ist, erscheint das Modul im Administrationsbereich unter :menuselection:`Erweiterungen --> Module`.


.. todo: #tbd Bild ergänzen

.. todo: Nächster Schritt Konfiguration






.. Intern: oxdaab, Status: