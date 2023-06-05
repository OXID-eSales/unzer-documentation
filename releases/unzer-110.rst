Unzer Payment for OXID V. 1.1
=============================

Release date: 02-06-2023

New or changed functions
------------------------

* Use the Buy Now, Pay Later payment method :productname:`Unzer Invoice (Paylater)`.

  For more information, see `docs.unzer.com/payment-methods <https://docs.unzer.com/payment-methods/>`_.

  To use :productname:`Unzer Invoice (Paylater)`, do the following:

  1. Contact your Unzer representative and arrange the desired combination of currency and customer type.
     |br|
     You will receive the private and public keys for sandbox and live operation from Unzer.
  2. Configure :productname:`Unzer Purchase on Account (Paylater)` as described under :ref:configuration:Configurìng Unzer`.

* Note restrictions on the countries and currencies for which you can offer certain payment methods.

  * For the current valid countries, see :ref:`introduction:Which markets are covered?`.
  * For the current valid currencies, see :ref:`introduction:Which currencies are covered?`.

  For more information, see the `Changelog <https://github.com/OXID-eSales/unzer-module/blob/v1.1.0/CHANGELOG.md>`_.

Corrections
-----------

For the corrections, see the changelog (GitHub) under https://github.com/OXID-eSales/unzer-module/blob/v1.1.0/CHANGELOG.md.


Update
------

To use the features and fixes of :productname:`Unzer Payment for OXID` V. 1.1.0, make an update.

Requirements
^^^^^^^^^^^^

* You have OXID eShop V. 6.1.x to 6.5.x.
* You have Unzer Payment for OXID V. 1.0.x.

Procedure
^^^^^^^^^

Execute the following command.

.. code:: bash

   composer update

