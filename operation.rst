Operation
=========

Monitor your orders and the payment transactions executed with Unzer.

For example, make refunds or resolve the causes of payment problems.

|procedure|

1. Choose :menuselection:`Orders --> Administer Orders`.
#. Choose the purchase order.
#. On the :guilabel:`Unzer` tab, display the transaction data.
#. Verify the status of the payment transaction:

   * :guilabel:`completed`: the payment has been made. You can ship the item (:ref:`oxdamd01`).

     .. _oxdamd01:

     .. figure:: /media/screenshots/oxdamd01.png
        :alt: Unzer order state: completed

        Fig.: Unzer order state: completed

   * :guilabel:`pending`: Payment pending (:ref:`oxdamd02`).
     |br|
     How long a payment remains outstanding depends on the payment method. For example, a credit card payment may take two days.
     |br|
     In certain cases, you may also want to configure a payment so that it is not triggered until it is delivered (see also: :ref:`configuration:Credit card/PayPal options`).

     .. _oxdamd02:

     .. figure:: /media/screenshots/oxdamd02.png
        :alt: Unzer order state: pending

        Fig.: Unzer order state: pending

   * :guilabel:`Error`: A problem has occurred.

#. If a problem has occurred, do the following to fix the cause:

   a. Ask your customer why the payment was not made.
   b. If the cause is not with the customer, contact Unzer's technical support at `support@unzer.com <support@unzer.com>`_.
      |br|
      When doing so, have the following information ready (:ref:`oxdamd03`):

       * Unzer Short-ID: ID of the transaction

         .. hint::

            Under the Unzer Short ID, you can also find the transaction in Unzer Insights (at `insights.unzer.com <https://insights.unzer.com/>`_).

       * Unzer Customer ID

      .. _oxdamd03:

      .. figure:: /media/screenshots/oxdamd03.png
         :alt: Unzer Short-ID and Unzer Customer-ID

         Fig.: Unzer Short-ID and Unzer Customer-ID

   c. If Unzer technical support finds that this is a technical issue, have the following additional information available for technical support (:ref:`oxdamd03`):

      * Unzer Trace ID
      * Unzer Type-ID

      .. _oxdamd04:

      .. figure:: /media/screenshots/oxdamd04.png
         :alt: Unzer Trace-ID and Unzer Type-ID

         Fig.: Unzer Trace-ID and Unzer Type-ID


.. Intern: oxdamd, Status: