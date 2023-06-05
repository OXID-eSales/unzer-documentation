Betrieb
=======

Überwachen Sie Ihre Bestellungen und die mit Unzer ausgeführten Zahlungsvorgänge.

Nehmen Sie beispielsweise Rückzahlungen vor oder beheben Sie die Ursachen von Zahlungsproblemen.

|procedure|

1. Wählen Sie :menuselection:`Bestellungen --> Bestellungen verwalten`.
#. Wählen Sie die Bestellung.
#. Zeigen Sie auf der Registerkarte :guilabel:`Unzer` die Daten der Transaktion an.
#. Prüfen Sie den Status des Zahlungsvorgangs:

   * :guilabel:`abgeschlossen`: Die Zahlung ist erfolgt. Sie können den Artikel versenden (:ref:`oxdamd01`).

     .. _oxdamd01:

     .. figure:: /media/screenshots/oxdamd01.png
        :alt: Unzer-Auftragsstatus: abgeschlossen

        Abb.: Unzer-Auftragsstatus: abgeschlossen

   * :guilabel:`Ausstehend`: Die Zahlung steht aus (:ref:`oxdamd02`).
     |br|
     Wie lange eine Zahlung ausstehend bleibt, hängt von der Zahlungsart ab. Eine Kreditkarten-Zahlung kann beispielsweise zwei Tage dauern.
     |br|
     In bestimmten Fällen ist es auch sinnvoll, dass Sie eine Zahlung so konfigurieren, dass sie erst durch die Auslieferung ausgelöst wird (siehe auch: :ref:`konfiguration:Optionen für Kreditkarten/PayPal`).

     .. _oxdamd02:

     .. figure:: /media/screenshots/oxdamd02.png
        :alt: Unzer-Auftragsstatus: ausstehend

        Abb.: Unzer-Auftragsstatus: ausstehend

   * :guilabel:`Fehler`: Ein Problem ist aufgetreten.

#. Wenn ein Problem aufgetreten ist, tun Sie Folgendes, um die Ursache zu beheben:

   a. Fragen Sie Ihren Kunden, warum die Zahlung nicht erfolgt ist.
   b. Wenn die Ursache nicht beim Kunden liegt, wenden Sie sich unter `support@unzer.com <support@unzer.com>`_ an den fachlichen Support von Unzer.
      |br|
      Halten Sie dabei die folgenden Informationen bereit (:ref:`oxdamd03`):

       * Unzer Short-ID: ID der Transaktion

         .. hint::

            Unter der Unzer Short-ID finden Sie die Transaktion auch in Unzer Insights (unter `insights.unzer.com <https://insights.unzer.com/>`_).

       * Unzer Kunden-ID

      .. _oxdamd03:

      .. figure:: /media/screenshots/oxdamd03.png
         :alt: Unzer Short-ID und Unzer Kunden-ID

         Abb.: Unzer Short-ID und Unzer Kunden-ID

   c. Wenn der fachliche Support von Unzer feststellt, dass es sich um ein technisches Problem handelt, halten Sie für den technischen Support zusätzlich die folgenden Informationen bereit (:ref:`oxdamd03`):

      * Unzer Trace-ID
      * Unzer Type-ID

      .. _oxdamd04:

      .. figure:: /media/screenshots/oxdamd04.png
         :alt: Unzer Trace-ID und Unzer Type-ID

         Abb.: Unzer Trace-ID und Unzer Type-ID


.. Intern: oxdamd, Status: