:orphan:
Creating Apple Pay access data
==============================

If you use :productname:`Apple Pay`, generate the necessary data in your Apple developer account to upload it to Unzer in your OXID eShop.

You will need the data under :menuselection:`Extensions --> Modules --> Unzer Payment for OXID --> Settings --> additional options for Apple Pay`.

You use the same certificates and keys for sandbox operation as for live operation.

For more information, see

* :ref:`configuration:Options for Apple Pay: Entering your credentials`.
* :ref:`configuration:Operation mode: Testing the eShop and activating live operation`.

|prerequisites|

You have access to the Unzer documentation for generating the :productname:`Apple Pay` certificates at `docs.unzer.com/payment-methods/applepay/applepay-prerequisites <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites>`_.


Creating an Apple Pay merchant ID
---------------------------------

Generate the merchant ID that you need to enter in the :guilabel:`Merchant Identifier` field.



|procedure|

1. To create an Apple developer account, create an Apple ID at `appleid.apple.com <https://appleid.apple.com/>`_.
#. Log in to your Apple developer account.
#. Choose :guilabel:`Certificates, Identifiers & Profiles`.
#. Choose :guilabel:`Identifiers` from the menu and then choose the :guilabel:`Add Identifiers` icon (+).
#. Under :guilabel:`Register a new Identifier`, choose :guilabel:`Merchant IDs` and confirm with :guilabel:`Continue`.
#. Under :guilabel:`Register a Merchant ID`, enter the following:

   * :guilabel:`Description`: description of the application.
     |br|
     Examples:

     * If you are using a dedicated test system to test Apple Pay features, enter :technicalname:`Apple Pay Test`, for example.
     * To better keep track of this in production operations, enter the name of the subshop in question, for example.
   * :guilabel:`Identifier`: Recommended: Enter a string close to the scheme :technicalname:`merchant.<domain name>.<application name>`.
     |br|
     Example: :technicalname:`merchant.myoxidshop.applepaytest`.

#. Choose :guilabel:`Continue`.
#. To confirm your input, choose :guilabel:`Register`.

|result|

Your merchant ID appears in the :guilabel:`Identifier` column under :guilabel:`Identifiers`.


Generating a payment certificate
--------------------------------

Generate the payment certificate and the corresponding key that you will need to enter in the :guilabel:`Payment Processing Certificate` and :guilabel:`Private key for payment processing` fields.

Get the certificate signed by Apple.

|prerequisites|

* You have created an Apple merchant ID (see :ref:`applepay/applepay-certificates:Creating an Apple Pay merchant ID`).


|procedure|

1. Follow step 1 of the instructions under `Generate the Payment Processing Certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#generate-the-payment-processing-certificate>`_.
   |br|
   Result: You have the following files:

   * ECC key, in our example :file:`ecckey.key`.
   * CSR, in our example :file:`ecccertreq.csr`.

#. In your Apple developer account, under :menuselection:`Certificates, Identifiers & Profiles --> Identifiers`, choose the merchant ID you created for your OXID eShop under :ref:`applepay/applepay-certificates:Creating an Apple Pay merchant ID`, in our example :technicalname:`Apple Pay Test`.
#. To upload the :file:`ecccertreq.csr` to Apple, under :guilabel:`Apple Pay Payment Processing Certificates` choose :guilabel:`Create Certificate` (see `Step 2: Upload the Payment Processing Certificate CSR to Apple <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-2-upload-the-payment-processing-certificate-csr-to-apple>`_).
   |br|
   The name, type and expiration date of the certificate are displayed.
#. To download and save the Apple-signed certificate, under :guilabel:`Apple Pay Payment Processing Certificates`, choose :guilabel:`Download` (see `Step 3: Download the Apple-signed Payment Processing Certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-3-download-the-apple-signed-payment-processing-certificate>`_).
   |br|
   You have saved the :file:`csr` certificate downloaded from Apple :file:`ecccertreq.csr`.
#. Convert the :file:`csr` certificate to a :file:`pem` file (see `Step 4: Convert the certificate to a text file <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-4-convert-the-certificate-to-a-text-file>`_).
   |br|
   In our example, you have :file:`apple_pay.pem`.
#. Convert the ECC key you generated in step 1 (in our example :file:`ecckey.key`) to a non-encrypted PKCS#8 private key (see `Step 5: Convert your ECC private key to a non-encrypted PKCS #8 private key <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-5-convert-your-ecc-private-key-to-a-non-encrypted-pkcs-8-private-key>`_).
   |br|
   In our example you have the file :file:`privatekey.key`.

|result|

You have saved the following files:

* the payment processing certificate, in our example the file :file:`apple_pay.pem`.
* the corresponding private key for payment processing in PKCS#8 format, in our example the file :file:`privatekey.key`.


Generating a merchant certificate
---------------------------------

Generate the merchant certificate and the associated key that you will need to enter in the :guilabel:`Merchant Certificate` and :guilabel:`Merchant Certificate Private Key` fields.

Get the certificate signed by Apple.

|prerequisites|

* You have created an Apple merchant ID (see :ref:`applepay/applepay-certificates:Creating an Apple Pay merchant ID`).

|procedure|

1. Follow step 1 of the instructions in `Generate a Merchant Identity Certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#generate-a-merchant-identity-certificate>`_.
   |br|
   Result: You have the following files:

   * RSA key, in our example :file:`encrypted_merchant_id.key`.
   * CSR, in our example :file:`merchant_id.csr`.

#. In your Apple developer account, under :menuselection:`Certificates, Identifiers & Profiles --> Identifiers`, choose the merchant ID you created for your OXID eShop under :ref:`applepay/applepay-certificates:Creating an Apple Pay merchant ID`, in our example :technicalname:`Apple Pay Test` #.
#. To upload the :file:`merchant_id` file to Apple, under :guilabel:`Apple Pay Merchant ID Certificate` choose :guilabel:`Create Certificate` (see `Step 2: Upload the Merchant Identification Certificate CSR to Apple <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-2-upload-the-merchant-identification-certificate-csr-to-apple>`_).
   |br|
   The name, type and expiration date of the certificate are displayed.
#. To download and save the Apple-signed certificate, under :guilabel:`Apple Pay Merchant ID Certificate` choose :guilabel:`Download` (see `Step 3: Download the Apple-signed Merchant Identification Certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-3-download-the-apple-signed-merchant-identification-certificate>`_).
   |br|
   You have saved the :file:`csr` certificate downloaded from Apple :file:`merchant_id.cer`.
#. Convert the :file:`csr` certificate to a :file:`pem` file (see `Step 4a: Convert the certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#convert-the-certificate>`_).
   |br|
   In our example, you have the :file:`merchant_id.pem` file.
#. Convert the RSA key you generated in step 1 (in our example :file:`encrypted_merchant_id.key`) to a non-encrypted private key in PKCS#8 format (see `Step 4b: Convert your RSA private key <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#convert-your-rsa-private-key>`_).
   |br|
   In our example, you have :file:`merchant_id.key`.

|result|

You have saved the following files:

* the merchant certificate, in our example the file :file:`merchant_id.pem`.
* the private key corresponding to the merchant certificate, in PKCS#8 format, in our example the file :file:`merchant_id.key`.


