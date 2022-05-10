Apple Pay-Zugangsdaten erstellen
================================

Wenn Sie :productname:`Apple Pay` nutzen, generieren Sie in Ihrem Apple-Entwickler-Konto die nötigen Daten, um sie in Ihrem OXID eShop zu Unzer hochladen zu können.

Die Daten benötigen Sie unter :menuselection:`Erweiterungen --> Module --> Einstell. --> zusätzliche Optionen für Apple Pay`.

Sie benutzen dieselben Zertifikate und Schlüssel für den Sandbox- wie für den Live-Betrieb.

Weitere Informationen finden Sie unter

* :ref:`konfiguration:Optionen für Apple Pay: Zugangsdaten eingeben`
* :ref:`konfiguration:Betriebsmodus: eShop testen und Live-Betrieb aktivieren`.

|prerequisites|

Sie haben Zugriff auf die Unzer-Dokumentation zum Erzeugen der :productname:`Apple Pay`-Zertifikate unter `docs.unzer.com/payment-methods/applepay/applepay-prerequisites <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites>`_.

Händler-ID anlegen
------------------

Generieren Sie die die Händler-ID, die Sie im Feld :guilabel:`Shopbetreiber Identifikation` eingeben müssen.



|procedure|

1. Um ein Apple-Entwickler-Konto anzulegen, legen Sie unter `appleid.apple.com <https://appleid.apple.com/>`_ eine Apple-ID an.
#. Melden Sie sich in Ihrem Apple-Entwickler-Konto an.
#. Wählen Sie :guilabel:`Certificates, Identifiers & Profiles`.
#. Wählen Sie im Menü den Eintrag :guilabel:`Identifiers` und dann das :guilabel:` Add Identifiers`-Symbol (+)`.
#. Unter :guilabel:`Register a new Identifier` wählen Sie :guilabel:`Merchant IDs` und bestätigen mit :guilabel:`Continue`.
#. Unter :guilabel:`Edit or Configure Merchant ID` geben Sie Folgendes ein:
#. Unter :guilabel:`Register a Merchant ID` geben Sie Folgendes ein:

   * :guilabel:`Description`: Beschreibung der Anwendung
     |br|
     Beispiele:

     * Wenn Sie ein dediziertes Testsystem zum Prüfen der Apple Pay-Funktionen benutzen, beispielsweise :technicalname:`Apple Pay Test`.
     * Um im Produktionsbetrieb den besser den Überblick zu behalten, geben Sie beispielsweise den Namen des betreffenden Subshops ein.
   * :guilabel:`Identifier`: Empfohlen: Geben Sie eine Zeichenfolge nah dem Schema :technicalname:`merchant.<Domänenname>.<Applikationsname>` ein.
     |br|
     Beispiel: :technicalname:`merchant.meinoxidshop.applepaytest`

#. Wählen Sie :guilabel:`Continue`.
#. Um Ihre Eingaben zu bestätigen, wählen Sie :guilabel:`Register`.

|result|

Ihre Händler-ID erscheint unter :guilabel:`Identifiers` in der Spalte :guilabel:`Identifier`.

Zahlungs-Zertifikat erzeugen
----------------------------

Generieren Sie das Zahlungs-Zertifikat und den dazugehörigen Schlüssel, die Sie in den Feldern :guilabel:`Zertifikat zur Zahlungsabwicklung` und :guilabel:`Privater Schlüssel zur Zahlungsabwicklung` eingeben müssen.

Lassen Sie das Zertifikat von Apple signieren.

|prerequisites|

* Sie haben eine Apple-Händler-ID angelegt (siehe :ref:`applepay/applepay-zertifikate:Händler-ID anlegen`).


|procedure|

1. Folgen Sie Schritt 1 der Anleitung unter `Generate the Payment Processing Certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#generate-the-payment-processing-certificate>`_.
   |br|
   Resultat: Sie haben folgende Dateien:

   * ECC-Schlüssel, in unserem Beispiel :file:`ecckey.key`
   * CSR, in unserem Beispiel :file:`ecccertreq.csr`

#. Wählen Sie Sie in Ihrem Apple-Entwickler-Konto unter :menuselection:`Certificates, Identifiers & Profiles --> Identifiers` die Händler-ID, die Sie unter :ref:`applepay/applepay-zertifikate:Händler-ID anlegen` für Ihren OXID eShop erzeugt haben, in unserem Beispiel :technicalname:`Apple Pay Test`.
#. Um die Datei :file:`ecccertreq.csr` zu Apple hochzuladen, wählen Sie unter :guilabel:`Apple Pay Payment Processing Certificates` die Schaltfläche :guilabel:`Create Certificate` (siehe `Step 2: Upload the Payment Processing Certificate CSR to Apple <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-2-upload-the-payment-processing-certificate-csr-to-apple>`_).
   |br|
   Name, Typ und Ablaufdatum des Zertifikats werden angezeigt.
#. Um das von Apple signierte Zertifikat herunterzuladen und zu speichern, wählen Sie unter :guilabel:`Apple Pay Payment Processing Certificates` die Schaltfläche :guilabel:`Download` (siehe `Step 3: Download the Apple-signed Payment Processing Certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-3-download-the-apple-signed-payment-processing-certificate>`_).
   |br|
   Sie haben das von Apple heruntergeladene :file:`csr`-Zertifikat :file:`ecccertreq.csr` gespeichert.
#. Konvertieren Sie das :file:`csr`-Zertifikat in eine :file:`pem`-Datei (siehe `Step 4: Convert the certificate to a text file <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-4-convert-the-certificate-to-a-text-file>`_).
   |br|
   Sie haben in unserem Beispiel die Datei :file:`apple_pay.pem`.
#. Konvertieren Sie den ECC-Schlüssel (in unserem Beispiel :file:`ecckey.key`), den Sie in Schritt 1 generiert haben, in einen nicht-verschlüsselten privaten Schlüssel im Format PKCS#8 (siehe `Step 5: Convert your ECC private key to a non-encrypted PKCS #8 private key <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-5-convert-your-ecc-private-key-to-a-non-encrypted-pkcs-8-private-key>`_).
   |br|
   Sie haben in unserem Beispiel die Datei :file:`privatekey.key`.

|result|

Sie haben folgende Dateien gespeichert:

* das Zertifikat zur Zahlungsabwicklung, in unserem Beispiel die Datei :file:`apple_pay.pem`
* den dazugehörigen privaten Schlüssel zur Zahlungsabwicklung im Format PKCS#8, in unserem Beispiel die Datei :file:`privatekey.key`


Händler-Zertifikat erzeugen
---------------------------

Generieren Sie das Händler-Zertifikat und den zugehörigen Schlüssel, die Sie in den Feldern :guilabel:`Shopbetreiber Zertifikat` und :guilabel:`Shopbetreiber Zertifikat Privater Schlüssel` eingeben müssen.

Lassen Sie das Zertifikat von Apple signieren.

|prerequisites|

* Sie haben eine Apple-Händler-ID angelegt (siehe :ref:`applepay/applepay-zertifikate:Händler-ID anlegen`).


|procedure|

1. Folgen Sie Schritt 1 der Anleitung unter `Generate a Merchant Identity Certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#generate-a-merchant-identity-certificate>`_.
   |br|
   Resultat: Sie haben folgende Dateien:

   * RSA-Schlüssel, in unserem Beispiel :file:`encrypted_merchant_id.key`
   * CSR, in unserem Beispiel :file:`merchant_id.csr`

#. Wählen Sie Sie in Ihrem Apple-Entwickler-Konto unter :menuselection:`Certificates, Identifiers & Profiles --> Identifiers` die Händler-ID, die Sie unter :ref:`applepay/applepay-zertifikate:Händler-ID anlegen` für Ihren OXID eShop erzeugt haben, in unserem Beispiel :technicalname:`Apple Pay Test`.
#. Um die Datei :file:`merchant_id` zu Apple hochzuladen, wählen Sie unter :guilabel:`Apple Pay Merchant ID Certificate` die Schaltfläche :guilabel:`Create Certificate` (siehe `Step 2: Upload the Merchant Identification Certificate CSR to Apple <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-2-upload-the-merchant-identification-certificate-csr-to-apple>`_).
   |br|
   Name, Typ und Ablaufdatum des Zertifikats werden angezeigt.
#. Um das von Apple signierte Zertifikat herunterzuladen und zu speichern, wählen Sie unter :guilabel:`Apple Pay Merchant ID Certificate` die Schaltfläche :guilabel:`Download` (siehe `Step 3: Download the Apple-signed Merchant Identification Certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#step-3-download-the-apple-signed-merchant-identification-certificate>`_).
   |br|
   Sie haben das von Apple heruntergeladene :file:`csr`-Zertifikat :file:`merchant_id.cer` gespeichert.
#. Konvertieren Sie das :file:`csr`-Zertifikat in eine :file:`pem`-Datei (siehe `Step 4a: Convert the certificate <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#convert-the-certificate>`_).
   |br|
   Sie haben in unserem Beispiel die Datei :file:`merchant_id.pem`.
#. Konvertieren Sie den RSA-Schlüssel (in unserem Beispiel :file:`encrypted_merchant_id.key`), den Sie in Schritt 1 generiert haben, in einen nicht-verschlüsselten privaten Schlüssel im Format PKCS#8 (siehe `Step 4b: Convert your RSA private key <https://docs.unzer.com/payment-methods/applepay/applepay-prerequisites/#convert-your-rsa-private-key>`_).
   |br|
   Sie haben in unserem Beispiel die Datei :file:`merchant_id.key`.

|result|

Sie haben folgende Dateien gespeichert:

* das Händler-ertifikat, in unserem Beispiel die Datei :file:`merchant_id.pem`
* den dazugehörigen privaten Schlüssel zum Händler-Zertifikat im Format PKCS#8, in unserem Beispiel die Datei :file:`merchant_id.key`


