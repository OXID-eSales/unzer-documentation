Unzer Payment for OXID V. 1.2
=============================

Release date: 02-06-2023

New or changed functions
------------------------

Offer your customers the following extended payment options:

* New payment method Unzer installment (EUR, CHF) for the following countries:

  * Germany
  * Netherlands
  * Austria
  * Switzerland

* Extended country coverage for Unzer Direct Debit

  In addition to Germany and Austria, the following countries are now also covered:

  * Belgium
  * Estonia
  * Finland
  * France
  * Greece
  * Ireland
  * Italy
  * Latvia
  * Lithuania
  * Luxembourg
  * Malta
  * Netherlands
  * Portugal
  * Slovakia
  * Slovenia
  * Spain
  * Cyprus

For more information about the available payment methods, please see :ref:`introduction:For what?/Where not?`.


Corrections
-----------

* Sometimes orders are not completed correctly after payment, for example because customers do not return to the checkout.

  The system prevents this from happening by automatically creating orders after a time limit.

  If the problem still occurs, you can adjust the time limit value.

  For more information, see :ref:`configuration:Other: Adjusting the time limit for creating orders`

See also the changelog (GitHub) under https://github.com/OXID-eSales/unzer-module/blob/v1.2.0/CHANGELOG.md.


Update
------

To use the features and fixes of :productname:`Unzer Payment for OXID` V. 1.2.x, make an update.

Requirements
^^^^^^^^^^^^

* You have OXID eShop V. 6.3.x to 6.5.x.
* You have Unzer Payment for OXID V. 1.x.

Procedure
^^^^^^^^^

Execute the following command.

.. code:: bash

   composer update

