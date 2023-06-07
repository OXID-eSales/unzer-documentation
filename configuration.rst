Configuration
=============

Make :productname:`Unzer Payment for OXID` ready to use.


Basic procedure
---------------

Configure and test Unzer. Then switch on live operation.

|prerequisites|

* You have agreed on the conditions with Unzer, opened a merchant account and received the access data from Unzer.

|procedure|

1. Activate the module.
#. Under :guilabel:`Access Data`, create the connection to your Unzer merchant account.
#. If you use :productname:`Apple Pay`, do the following:

   a. Generate the necessary certificates locally.
   b. Sign the certificates in your Apple developer account.
   c. To make your :productname:`Apple Pay` credentials known to Unzer, under :guilabel:`Options for Apple Pay`, enter the signed certificates  and upload them to Unzer.
#. Optional: if required, under :guilabel:`Additional options ...` configure  that payments should be triggered with a delay (for example, for business customers).
#. Check if your eShop theme uses jQuery.
   |br|
   If it does not, under :guilabel:`Other`, include jQuery.
#. Link the payment methods provided by Unzer to your shipping methods and shipping rules and run test payments in the Unzer sandbox.
   |br|
   The :technicalname:`Sandbox` mode is set by default after activation.
#. Test Unzer in the Unzer sandbox and adjust the configuration until all payment processes work as you want.
#. When you have finished your tests, under :guilabel:`Operation mode` switch to :technicalname:`Production`.
#. If you have run the tests on a dedicated test system and then move your eShop to the production system, regenerate the webhooks for the production system URL.

Activating Unzer
----------------

Activate Unzer in each subshop where you want to use the module.

|procedure|

1. Choose :menuselection:`Extensions --> Modules`.
2. Choose the module :guilabel:`Unzer Payment Module for OXID` and choose :menuselection:`Overview --> Activate`.


|result|

Under :menuselection:`Shop Settings --> Payment Methods`, the payment method covered by the :productname:`Unzer Payment for OXID` module are marked as active.

Active are automatically those payment method that match the countries you marked as active in :menuselection:`Master Settings --> Countries` (:ref:`oxdamc01`).



|example|

You have marked the Netherlands as active. This makes the payment method :productname:`iDEAL` available.


.. _oxdamc01:

.. figure:: /media/screenshots/oxdamc01.png
   :alt: Automatically activated payment methods

   Fig.: Automatically activated payment methods



Configuring Unzer
-----------------

Start the configuration.

|procedure|

1. Choose :menuselection:`Extensions --> Modules`.
#. Choose the :guilabel:`Unzer Payment Module for OXID` module and choose :guilabel:`Settings`.

Access Data: Generating a webhook
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Register a webhook to connect your eShop with Unzer.

|prerequisites|

* You have the following data ready, which Unzer provided you with when you set up your merchant account:

   * Sandbox Public-Key
   * Sandbox Private-Key
   * Production Public-Key
   * Production Private-Key

For more information about authenticating with Unzer, see `docs.unzer.com/server-side-integration/api-basics/authentication <https://docs.unzer.com/server-side-integration/api-basics/authentication/>`_.


|procedure|

1. Under :menuselection:`Setting --> Access Data`, enter the keys provided by Unzer into the corresponding fields (:ref:`oxdamc02`, item 1).
#. Choose the :guilabel:`Register webhook for this shop` button (:ref:`oxdamc02`, item 2).

.. _oxdamc02:

.. figure:: /media/screenshots/oxdamc02.png
   :alt: Registering a webhook

   Fig.: Registering a webhook


|result|

The URL of your registered webhook is displayed (:ref:`oxdamc03`). Your store is connected to Unzer.

.. _oxdamc03:

.. figure:: /media/screenshots/oxdamc03.png
   :alt: Registered webhook

   Fig.: Registered Webhook


Credit card/PayPal options
^^^^^^^^^^^^^^^^^^^^^^^^^^

Specify whether payments are to be collected immediately for the eShop, or whether payments are only to be reserved.

----------------------------------------------------------------------

|example|

Typically, the money is collected immediately.

In certain cases, it makes sense that the payment is only triggered by the delivery:

* You sell certain individualized products that you do not manufacture, commission, or order until the order is received.
* You have an eShop for business customers. Here the delivery quantities and payment amounts are larger than for private customers.
  |br|
  So, in case of an error returns management would be more difficult.
  |br|
  Therefore, you want to make sure that the payment is only triggered when the goods are there or on their way to be shipped.

----------------------------------------------------------------------

|procedure|

1. Choose :menuselection:`Settings --> additional options for credit cards`.
#. You have the following options:

   * To trigger payments directly, choose :guilabel:`direct Capture`.
   * To reserve the payment only and trigger it later, choose :guilabel:`Authorize & later Capture`.
#. Repeat step 2 under :menuselection:`Settings --> additional options for PayPal`.
#. Save your settings.
#. Make sure that you have assigned only the appropriately configured :guilabel:`PayPal` or :guilabel:`Cards` payment method to the customized products in your eShop.
   |br|
   Delayed payment for payment by :productname:`PayPal` or :productname:`Cards` takes effect for all items in your eShop to which you have assigned these payment methods.


|result|


The order has the status :guilabel:`pending` (see :ref:`oxdamd02` in chapter :ref:`operation:Operation`).

If you have chosen :guilabel:`Authorize` for payment by PayPal or card payment, the delayed payment will be triggered,

* as soon as you set the ordered item to the status `Delivered` in your eShop
* when you request the payment using Unzer Insights (at `insights.unzer.com <https://insights.unzer.com/>`_)

For all other payment methods supported by Unzer, the payment is triggered immediately with the order.

Options for Apple Pay: Entering your credentials
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you use :productname:`Apple Pay`, connect to Apple separately.

To do this, generate the following :productname:`Apple Pay` credentials, have them signed in your Apple developer account, and upload them to Unzer:

  * Merchant ID
  * Payment processing certificate
  * Payment processing certificate private key
  * Merchant certificate
  * Merchant certificate private key

|prerequisites|

* You have connected your OXID eShop to Unzer (see :ref:`configuration:Access Data: Generating a webhook`).


|procedure|

1. Create an :productname:`Apple Pay` merchant ID (see :ref:`applepay/applepay-certificates:Creating an Apple Pay merchant ID`).
#. Create an Apple signed payment processing certificate and associated payment processing private key in PKCS#8 format (see: :ref:`applepay/applepay-certificates:Generating a payment certificate`).
#. Choose :menuselection:`Settings --> additional options for Apple Pay`.
#. In the appropriate input fields, enter payment certificate and key.
   |br|
   Make sure to include the prefix and suffix (``-----BEGIN PRIVATE KEY-----``, for example).

   * Open the :file:`pem` file with the payment processing certificate (in our example :file:`apple_pay.pem`) and copy the content into the :guilabel:`payment processing certificate` field.
   * Open the text file with the private key for payment processing (in our example :file:`privatekey.key`) and copy the content into the :guilabel:`Private key for payment processing` field.

#. Choose the :guilabel:`Transfer payment certificates` button.
#. Generate an Apple-signed merchant certificate and the corresponding private key in PKCS#8 format (see: :ref:`applepay/applepay-certificates:Creating an Apple Pay merchant ID`).
#. Choose :menuselection:`Settings --> additional options for Apple Pay`.
#. In the :guilabel:`Merchant Identifier` field, enter the merchant ID you created in your Apple developer account (see :ref:`applepay/applepay-certificates:Creating an Apple Pay merchant ID`).
#. Enter the merchant certificate and key in the appropriate input fields (including prefix and suffix):

   * Open the :file:`pem` file containing the merchant certificate (in our example :file:`merchant_id.pem`) and copy the contents into the :guilabel:`Payment Processing Certificate` field.
   * Open the text file with the private key to the merchant certificate (in our example :file:`merchant_id.key`) and copy the content into the :guilabel:`Private key for payment processing` field.
#. In the :guilabel:`Company` field, enter your company name.
#. Under :guilabel:`Supported credit cards`, activate the credit card company whose credit card is associated with your Apple Pay account.

   .. attention::

      **Conversion at risk**

      Which credit card companies you can choose as supported depends on your agreement with Unzer.

      If you mark credit card companies that differ from your agreement with Unzer, no checkout is possible, and your customer will probably reject your shop.

      Test all payment methods extensively in the sandbox.

#. Optional: Under :guilabel:`Supported payment types`, choose the card type you want to allow :

   * Checkbox :guilabel:`Credit Card`: Allow :emphasis:`credit` card payments.
   * Check box :guilabel:`Debit Card`: Allow :emphasis:`debit` card payments.

   By default, both card types are active. :emphasis:`Both` card types are active even if you check :emphasis:`neither` of the two checkboxes.
   |br|
   Debit card payments are used less frequently than credit card payments. For example, if you consider credit cards more reliable, choose this card type as the only one allowed.
#. Save your settings.

Entering access data for Unzer purchase on account (Paylater)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you want to use the :productname:`Unzer Invoice (Paylater)` payment method, enter the public and private keys provided by Unzer.

|prerequisites|

* Depending on the combination of currency and customer type you have agreed on with Unzer, you have the following data ready, which Unzer has provided you with when you set up your merchant account:

   * Sandbox Public-Key
   * Sandbox Private-Key
   * Production Public-Key
   * Production Private-Key

|procedure|

1. Under :menuselection:`Settings --> Additional Options for Unzer Invoice (Paylater)`, in the appropriate fields, enter the keys provided by Unzer.

   Make sure that you enter the key pair for both currencies (EUR and CHF) (:ref:`oxdamc04`, item 1 and 2) for each customer type (in our example only B2C).

#. Save your settings.

.. note::

   **Match currencies and credentials**.

   The payment method Unzer Invoice (Paylater) will only be offered in the checkout if you have

   * configured the currency that matches the key pair (EUR or CHF)
   * entered the key pairs tat match the configured currencies

   Under :menuselection:`Master Settings --> Core Settings --> Settings --> Other settings`, make sure that you have configured the desired currencies.

.. _oxdamc04:

.. figure:: /media/screenshots/oxdamc04.png
   :alt: Entering key pairs for Unzer Invoice (Paylater)
   :width: 650
   :class: with-shadow

   Figure: Entering key pairs for Unzer Invoice (Paylater)

|result|

In the checkout, an additional query for the date of birth (:ref:`oxdamc05`, item 1) appears automatically for private customers (B2C).

Business customers (B2B) are automatically recognized by the system by an entry in the :guilabel:`company name` input field. In addition to the date of birth, a business customer must specify the legal form of his company.

From the information about the customer, Unzer calculates a credit rating of the customer.

.. _oxdamc05:

.. figure:: /media/screenshots/oxdamc05.png
   :alt: Specifying the date of birth and company form
   :width: 650
   :class: with-shadow

   Figure: Specifying the date of birth and company form


Recommended: Ensuring correct currency settings
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Make sure that the currencies that your OXID eShop supports match the currencies that a payment method supports.

However, nothing can go wrong: For currencies that a payment method does not support, only the respective button for the payment method is not displayed in the checkout.

.. include:: /_static/reuse/apple-pay-currencies.rst

|procedure|

1. Check the currencies that your store supports:

   a. Choose :menuselection:`Master Settings --> Core Settings`.
   #. On the :guilabel:`Settings` tab, expand the :guilabel:`Other Settings` section.
   #. In the input field for currencies, check whether you want to add or remove currencies.
#. To ensure a clean configuration, do the following:

   a. Under :menuselection:`Shop Settings --> Payment Methods`, for the respective payment type, choose the :guilabel:`Country` tab.
   #. Make sure that only those countries are assigned whose currency is supported by the payment type.

Other: Ensuring optimum performance
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Unzer uses jQuery for validating form inputs.

However, to avoid affecting the performance of your OXID eShop, make sure that jQuery is not installed twice.

|example|

You use one of the two OXID themes :productname:`Wave` or :productname:`Fluid`.

Both OXID themes have jQuery already integrated.

To avoid interference, make sure that jQuery is not included again separately for :productname:`Unzer Payment for OXID`.

|procedure|

1. Verify if the theme of your OXID eShop uses jQuery:

   * Ask your web front-end developer.
   * Alternatively: Inspect the HTML code of your eShop's front page.
#. Choose :menuselection:`Settings --> Other`.
#. Do the following:

   * If your theme uses jQuery, make sure the :guilabel:`Include jQuery via the module` checkbox is deactivated.
   * If your theme **does not** use jQuery, make sure the :guilabel:`Include jQuery via the module` checkbox is activated.


Operation mode: Testing the eShop and activating live operation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Test :productname:`Unzer Payment for OXID` in the Unzer sandbox and adjust the configuration until all payment processes work as you want them to.

To do this, run test payments in the Unzer sandbox.

The operating mode :guilabel:`Sandbox` is set by default.

Recommendation: Use a dedicated test system for testing. In this case, follow the instructions in :ref:`configuration:Switching from a test system to the production system`.

|prerequisites|

* To start live operation, you have created an Unzer Insights account (https://insights.unzer.com/signin).

  For more information, see the `Go-live checklist <https://docs.unzer.com/online-payments/go-live-checklist/>`_.

|procedure|

1. Optional: To generate logs during testing, activate the checkbox under :menuselection:`Settings --> Operation mode` activate :guilabel:`Enable debug mode`.
   |br|
   Typically, you turn on logging only on request: When the Unzer support asks you to debug a problem.
   |br|
   You find the log files in the directory :file:`source/log/unzer`.

#. Configure the payment methods provided by :productname:`Unzer Payment for OXID` as payment methods in your eShop:

   * Enable the countries you want to cover.
   * Link the payment methods to your shipping methods and shipping rules.
   * Avoid duplication of payment methods.
     |br|
     Background: :productname:`Unzer Direct Debit (SEPA Direct Debit)` can be offered in European countries including Germany, :productname:`Unzer Direct Debit (SEPA Direct Debit) (secured with Unzer)` however only in Germany.
     |br|
     Configure these invoice types so that :productname:`Unzer Direct Debit (SEPA Direct Debit) (secured with Unzer)` is assigned to German user groups only and :productname:`Unzer Direct Debit (SEPA Direct Debit)` is assigned to non-German user groups only.
#. After you have configured and tested the functions of the module, under :menuselection:`Settings --> Access Data` make sure that you have entered the following data that you received from Unzer:

   * In the :guilabel:`Live public key` field is the :technicalname:`Production public key`.
   * In the :guilabel:`Live private key` field is the :technicalname:`Production Private-Key`.
#. Under :guilabel:`Operation mode`, choose :guilabel:`Production` and choose :guilabel:`Save`.
#. If you use :productname:`Apple Pay`, do the following:

   a. Under :guilabel:`additional options for Apple Pay`, re-enter key and certificates.
      |br|
      You have created the certificates and keys in your Apple developer account and saved them locally (see :ref:`applepay/applepay-certificates:Creating Apple Pay access data`).

      * Payment processing certificate (file :file:`apple_pay.pem`).
      * Private key for payment processing (file :file:`privatekey.key`).
      * Shop operator certificate (file :file:`merchant_id.pem`)
      * Private key to store operator certificate (file :file:`merchant_id.key`)

   b. Choose :guilabel:`Transfer payment certificates (Production)`.

#. To avoid unnecessary memory consumption, under :guilabel:`Operating mode` make sure that the debug mode is disabled in live mode.
#. Save your settings.


Switching from a test system to the production system
-----------------------------------------------------

If you have installed Unzer on a dedicated :emphasis:`test` system first, regenerate the webhook for the :emphasis:`production` system URL.

Otherwise, you will not receive any status messages on your production system, and you will not be able to process your customers' orders.

Also, make sure that you delete the webhook on your test system.

In this way, you maximize the performance of your Unzer connection.

Delete and regenerate a webhook also in case you have changed the URL of your OXID eShop for other reasons.

|background|

If the webhook is still active on your test system even when you are not using the test system, the status messages that Unzer sends to their production system will also be sent to your test system.

This creates an unnecessary system load on the Unzer system that is connected to your webhook. This can decrease the performance of your Unzer connection.

|procedure|

1. On your dedicated test system, do the following:

   a. Choose :menuselection:`Extensions --> Modules --> Unzer Payment Module for OXID --> Settings`.
   b. Under :guilabel:`Access Data`, choose :guilabel:`Delete Webhook` (see :ref:`oxdamc03`).
#. Repeat step 1 on your production system.
#. Under :guilabel:`Access Data`, re-enter your Unzer access data (:ref:`oxdamc02`, item 1).
#. Choose the :guilabel:`Register Webhook` button (:ref:`oxdamc02`, item 2).
#. Verify the URL that is displayed as part of the registered webhook (see :ref:`oxdamc03`).
#. If you use :productname:`Apple Pay`, under :menuselection:`Settings --> additional options for Apple Pay` enter the certificates and keys you created in your Apple developer account and stored locally (see :ref:`applepay/applepay-certificates:Creating Apple Pay access data`).


|result|

Your production system receives status reports from Unzer about your customers' payment transactions.
|br|
You can view the transaction data. For more information, see :ref:`operation:Operation`.

.. Intern: oxdamc, Status: