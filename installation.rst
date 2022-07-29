Installation
============

Install Unzer Payment OXID for OXID eShop version 6.2 or higher.

|prerequisites|

* You have installed OXID eShop 6.2 or higher.
* You have configured transport encryption (`https`).

   a. In the `<root directory of the eShop>/source` directory, open the `config.inc.php` file.
   b. Make sure that https is set for the base URL (`shopURL` parameter).

      Example:

      .. code::

         $this->sShopURL = 'https://www.example.org';

|procedure|

1. Open a shell and change to the root directory of the store (where the :file:`composer.json` file is located).
   Example:

   .. code:: bash

      cd /var/www/oxideshop/


#. Execute the following commands:

   .. code:: bash

      composer config repositories.oscunzer composer https://unzer-module.packages.oxid-esales.com/
      composer require oxid-solution-catalysts/unzer ^1.0.0
      composer install


|result|

When the installation process is finished, the module appears in the administration area under :menuselection:`Extensions --> Modules` (:ref:`oxdamb01`).

.. _oxdamb01:

.. figure:: /media/screenshots/oxdamb01.png
   :alt: Unzer Payment for OXID installed

   Fig.: Unzer Payment for OXID installed



Next step: To configure :productname:`Unzer Payment`, choose :guilabel:`Next`.






.. Internal: oxdamb, status:

