Installation
============

Installieren Sie das Unzer Payment-Modul für OXID für den OXID eShop ab Version 6.2.

|prerequisites|

* Sie haben den OXID eShop 6.2 oder höher installiert.
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


|result|

Sobald der Installationsprozess abgeschlossen ist, erscheint das Modul im Administrationsbereich unter :menuselection:`Erweiterungen --> Module` (:ref:`oxdamb01`).


.. _oxdamb01:

.. figure:: /media/screenshots/oxdamb01.png
   :alt: Unzer Payment für OXID erfolgreich installiert

   Abb.: Unzer Payment für OXID erfolgreich installiert



Nächster Schritt: Um :productname:`Unzer Payment` zu konfigurieren, wählen Sie :guilabel:`Weiter`.






.. Intern: oxdamb, Status: