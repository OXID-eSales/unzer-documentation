Wofür/Wofür nicht?
==================

Nutzen Sie das Modul :productname:`Unzer Payment für OXID`, um Ihren nationalen und internationalen Kunden ein weites Spektrum beliebter Zahlungsarten bereitzustellen.

Gegenwärtig können Sie Ihren Kunden damit 18 der von Unzer abgedeckten weltweit wichtigsten Zahlungsarten anbieten.

.. image:: media/unzer-logo.png
    :alt: Unzer-Logo
    :class: no-shadow
    :height: 35
    :width: 150

Welche Märkte sind abgedeckt?
-----------------------------

Bieten Sie mit dem Modul :productname:`Unzer Payment für OXID` die in folgenden Märkten beliebten Zahlungsmethoden an.

.. todo: #EC: Welche Unzer-Zahlungsarten gibt es mit 1.1?:
    Hinzu kmomt: Unzer Kauf auf Rechnung (Paylater)
    "Unzer Kauf auf Rechnung" wird "Unzer Kauf auf Rechnung (alt)"? -- bleibt auf jeden Fall vorläufig drin.
    #EC: Das alte Unzer Kauf auf Rechnung erwähnen wir in den folgenden Tabellen nicht mehr, korrekt? Nur in Release Note

.. todo: #EC Gemäß https://docs.unzer.com/payment-methods/
         folgende deprecated, kommen aber gleichzeitig noch in Liste der Zahlungsarten vo:
            Ratenzahlung mit Unzer	(Unzer Installment) also weg aus Liste?
            [Deprecated] Unzer Invoice
            [Deprecated] Unzer Invoice Secured
        Wo kommt Unzer Kauf auf Rechnung (Paylater) in https://docs.unzer.com/payment-methods/ vor?

.. todo: #EC/#ML: Unzer Kauf auf Rechnung (Paylater) welche Märkte?
        - DE, AU, CH
        - Länder wie Kauf auf Rechnung plus Schweiz?
        Siehe https://github.com/OXID-eSales/unzer-module/blob/b-6.3.x/CHANGELOG.md:
        New country restrictions based on the Unzer documentation
        ALIPAY: DE, AT, BE, IT, ES, NL
        Installment: DE, AT, CH (payment method deprecated) (Ratenzahlung mit Unzer)
        Unzer Invoice (Paylater): DE, AT, CH, NL
        Prepayment: all Countries
        SEPA Direct Debit: DE, AT
        Sofort: DE, AT, BE, IT, ES, NL
        WeChat: AT, BE, DK, FI, FR, DE, ES, GB, GR, HU, IE, IS, IT, LI, LU, MT, NL, NO, PT, SE
        Australien	 : nein: Österreich       Sofort Überweisung (Klarna Pay now)

.. todo: Definitionseinschränkungen für Währungen ergänzen: verfügbar mit RC6

=================== ========================================================
Markt               Zahlungsmethode
=================== ========================================================
Weltweit	        Alipay
Weltweit	        Apple Pay
Weltweit	        Kartenzahlung
Weltweit	        PayPal
Weltweit	        WeChat
Australien	        Sofort Überweisung (Klarna Pay now)
Belgien	            Unzer Kauf auf Rechnung (Paylater)
Belgien	            Vorkasse
Belgien	            SEPA-Lastschrift
Belgien	            Sofort Überweisung (Klarna Pay now)
Belgien             Bancontact
Dänemark	        Sofort Überweisung (Klarna Pay now)
Deutschland	        Unzer Kauf auf Rechnung (Paylater)
Deutschland	        Vorkasse
Deutschland	        SEPA-Lastschrift
Deutschland	        Giropay
Deutschland	        Ratenzahlung mit Unzer
Deutschland	        Unzer Kauf auf Rechnung (Paylater)
Deutschland	        SEPA Lastschrift (abgesichert mit Unzer)
Deutschland	        Sofort Überweisung (Klarna Pay now)
Deutschland	        Unzer Bank Transfer (Überweisung)
Estland	            Unzer Kauf auf Rechnung (Paylater)
Estland	            Vorkasse
Estland	            SEPA-Lastschrift
Finnland	        Unzer Kauf auf Rechnung
Finnland	        Vorkasse
Finnland	        SEPA-Lastschrift
Finnland	        Sofort Überweisung (Klarna Pay now)
Frankreich	        Sofort Überweisung (Klarna Pay now)
Griechenland	    Unzer Kauf auf Rechnung (Paylater)
Griechenland	    Vorkasse
Griechenland	    SEPA-Lastschrift
Großbritannien	    Sofort Überweisung (Klarna Pay now)
Irland	            Unzer Kauf auf Rechnung (Paylater)
Irland	            Vorkasse
Irland	            SEPA-Lastschrift
Italien	            Unzer Kauf auf Rechnung (Paylater)
Italien	            Vorkasse
Italien	            SEPA-Lastschrift
Lettland	        Unzer Kauf auf Rechnung (Paylater)
Lettland	        Vorkasse
Lettland	        SEPA-Lastschrift
Litauen	            Unzer Kauf auf Rechnung (Paylater)
Litauen	            Vorkasse
Litauen	            SEPA-Lastschrift
Luxemburg	        Unzer Kauf auf Rechnung (Paylater)
Luxemburg	        Vorkasse
Luxemburg	        SEPA-Lastschrift
Malta	            Unzer Kauf auf Rechnung (Paylater)
Malta	            Vorkasse
Malta	            SEPA-Lastschrift
Niederlande	        iDEAL
Niederlande	        Unzer Kauf auf Rechnung (Paylater)
Niederlande	        Vorkasse
Niederlande	        SEPA-Lastschrift
Niederlande	        Sofort Überweisung (Klarna Pay now)
Norwegen	        Sofort Überweisung (Klarna Pay now)
Österreich	        eps Überweisung (Electronic Payment Standard)
Österreich	        Ratenzahlung mit Unzer
Österreich	        Unzer Kauf auf Rechnung (Paylater)
Österreich	        Vorkasse
Österreich	        SEPA-Lastschrift
Österreich	        Unzer Bank Transfer (Überweisung)
Polen	            Przelewy24
Polen	            Sofort Überweisung (Klarna Pay now)
Portugal	        Unzer Kauf auf Rechnung (Paylater)
Portugal	        Vorkasse
Portugal	        SEPA-Lastschrift
Portugal	        Sofort Überweisung (Klarna Pay now)
Schweden	        Sofort Überweisung (Klarna Pay now)
Schweiz     	    Sofort Überweisung (Klarna Pay now)
Slowakei	        Unzer Kauf auf Rechnung (Paylater)
Slowakei	        Vorkasse
Slowakei	        SEPA-Lastschrift
Slowakei	        Sofort Überweisung (Klarna Pay now)
Slowenien	        Unzer Kauf auf Rechnung (Paylater)
Slowenien	        Vorkasse
Slowenien	        SEPA-Lastschrift
Spanien	            Unzer Kauf auf Rechnung (Paylater)
Spanien	            Vorkasse
Spanien	            SEPA-Lastschrift
Spanien	            Sofort Überweisung (Klarna Pay now)
Italien	            Sofort Überweisung (Klarna Pay now)
Tschechien	        Sofort Überweisung (Klarna Pay now)
Ungarn	            Sofort Überweisung (Klarna Pay now)
Vereinigte Staaten	Sofort Überweisung (Klarna Pay now)
Zypern	            Unzer Kauf auf Rechnung (Paylater)
Zypern	            Vorkasse
Zypern	            SEPA-Lastschrift
=================== ========================================================

Welche Märkte sind abgedeckt (sortiert nach Zahlungsmethoden)?
--------------------------------------------------------------

=============================================== ================
Zahlungsmethode                                 Markt
=============================================== ================
Alipay	                                        Weltweit
Apple Pay                                       Weltweit
Bancontact	                                    Belgien
eps Überweisung (Electronic Payment Standard)	Österreich
Giropay	                                        Deutschland
iDEAL	                                        Niederlande
Kartenzahlung                                   Weltweit
PayPal	                                        Weltweit
Przelewy24	                                    Polen
Ratenzahlung mit Unzer	                        Deutschland
Ratenzahlung mit Unzer	                        Österreich
Unzer Kauf auf Rechnung (Paylater)              Belgien
Unzer Kauf auf Rechnung (Paylater)              Deutschland
Unzer Kauf auf Rechnung (Paylater)              Estland
Unzer Kauf auf Rechnung (Paylater)              Finnland
Unzer Kauf auf Rechnung (Paylater)              Griechenland
Unzer Kauf auf Rechnung (Paylater)              Irland
Unzer Kauf auf Rechnung (Paylater)              Italien
Unzer Kauf auf Rechnung (Paylater)              Lettland
Unzer Kauf auf Rechnung (Paylater)              Litauen
Unzer Kauf auf Rechnung (Paylater)              Luxemburg
Unzer Kauf auf Rechnung (Paylater)              Malta
Unzer Kauf auf Rechnung (Paylater)              Niederlande
Unzer Kauf auf Rechnung (Paylater)              Österreich
Unzer Kauf auf Rechnung (Paylater)              Portugal
Unzer Kauf auf Rechnung (Paylater)              Slowakei
Unzer Kauf auf Rechnung (Paylater)              Slowenien
Unzer Kauf auf Rechnung (Paylater)              Spanien
Unzer Kauf auf Rechnung (Paylater)              Zypern
SEPA-Lastschrift	                            Belgien
SEPA-Lastschrift	                            Deutschland
SEPA-Lastschrift	                            Estland
SEPA-Lastschrift	                            Finnland
SEPA-Lastschrift	                            Griechenland
SEPA-Lastschrift	                            Irland
SEPA-Lastschrift	                            Italien
SEPA-Lastschrift	                            Lettland
SEPA-Lastschrift	                            Litauen
SEPA-Lastschrift	                            Luxemburg
SEPA-Lastschrift	                            Malta
SEPA-Lastschrift	                            Niederlande
SEPA-Lastschrift	                            Österreich
SEPA-Lastschrift	                            Portugal
SEPA-Lastschrift	                            Slowakei
SEPA-Lastschrift	                            Slowenien
SEPA-Lastschrift	                            Spanien
SEPA-Lastschrift	                            Zypern
SEPA Lastschrift (abgesichert mit Unzer)	    Deutschland
Sofort Überweisung (Klarna Pay now)	            Australien
Sofort Überweisung (Klarna Pay now)	            Belgien
Sofort Überweisung (Klarna Pay now)	            Dänemark
Sofort Überweisung (Klarna Pay now)	            Deutschland
Sofort Überweisung (Klarna Pay now)	            Finnland
Sofort Überweisung (Klarna Pay now)	            Frankreich
Sofort Überweisung (Klarna Pay now)	            Großbritannien
Sofort Überweisung (Klarna Pay now)	            Niederlande
Sofort Überweisung (Klarna Pay now)	            Norwegen
Sofort Überweisung (Klarna Pay now)	            Polen
Sofort Überweisung (Klarna Pay now)	            Portugal
Sofort Überweisung (Klarna Pay now)	            Schweden
Sofort Überweisung (Klarna Pay now)	            Schweiz
Sofort Überweisung (Klarna Pay now)	            Slowakei
Sofort Überweisung (Klarna Pay now)	            Spanien
Sofort Überweisung (Klarna Pay now)	            Italien
Sofort Überweisung (Klarna Pay now)	            Tschechien
Sofort Überweisung (Klarna Pay now)	            Ungarn
Sofort Überweisung (Klarna Pay now)	            Vereinigte Staaten
Unzer Bank Transfer	(Überweisung)               Deutschland
Unzer Bank Transfer	(Überweisung)               Österreich
Vorkasse	                                    Belgien
Vorkasse	                                    Deutschland
Vorkasse	                                    Estland
Vorkasse	                                    Finnland
Vorkasse	                                    Griechenland
Vorkasse	                                    Irland
Vorkasse	                                    Italien
Vorkasse	                                    Lettland
Vorkasse	                                    Litauen
Vorkasse	                                    Luxemburg
Vorkasse	                                    Malta
Vorkasse	                                    Niederlande
Vorkasse	                                    Österreich
Vorkasse	                                    Portugal
Vorkasse	                                    Slowakei
Vorkasse	                                    Slowenien
Vorkasse	                                    Spanien
Vorkasse	                                    Zypern
WeChat	                                        Weltweit
=============================================== ================


Welche Währungen unterstützt Apple Pay?
---------------------------------------

Wenn Sie :productname:`Apple Pay` nutzen, dann berücksichtigen Sie folgende Einschränkung:

.. todo: #tbd: verify the following: "Wenn Sie in Ihrem OXID eShop Währungen anbieten, die :productname:`Apple Pay` nicht unterstützt, dann wird die :productname:`Apple Pay`-Schaltfläche nicht angezeigt." -- stimmt für alle Zahlungsarten
   " -- no restriction at the moment, verification would have to go in: ML provides feedback, text will then be true

Wenn Sie in Ihrem OXID eShop Währungen anbieten, die :productname:`Apple Pay` nicht unterstützt, dann wird die :productname:`Apple Pay`-Schaltfläche nicht angezeigt.

Stellen Sie deshalb beim Konfigurieren sicher, dass Ihr OXID eShop nur diejenigen Währungen anbietet, die :productname:`Apple Pay` unterstützt.

.. include:: /_static/reuse/apple-pay-currencies.rst


Weitere Informationen zum Konfigurieren der Währungen Ihres OXID eShops finden Sie unter :ref:`konfiguration:Optional: Korrekte Apple Pay-Währungseinstellungen sicherstellen`.

Wo finde ich weitere Informationen?
-----------------------------------

Zahlungsmethoden
^^^^^^^^^^^^^^^^

.. todo: #EC: Sind die URLs aktuell

Welche Zahlungsmethoden Sie zu welchen Konditionen nutzen wollen, vereinbaren Sie individuell mit Unzer.

Oft gestellte Fragen über die Zahlungsmethoden von Unzer finden Sie unter `www.unzer.com/de/zahlungsmethoden <https://www.unzer.com/de/zahlungsmethoden/>`_ .

Informationen über die Zahlungsmethoden, die :productname:`Unzer Payment für OXID` abdeckt, finden Sie unter `www.unzer.com/de/oxid-e-sales <https://www.unzer.com/de/oxid-e-sales/>`_.

Informationen über die Eigenschaften der verschiedenen Zahlungsmethoden finden Sie unter `docs.unzer.com/payment-methods/ <https://docs.unzer.com/payment-methods/>`_.


Konditionen
^^^^^^^^^^^

Von welchen Konditionen Sie bei der Zusammenarbeit mit Unzer profitieren, erfahren Sie unter `www.unzer.com/de/online-loesungen-preise <https://www.unzer.com/de/online-loesungen-preise/>`_.

Ebenfalls vereinbaren Sie mit Unzer beispielsweise,

* ob Sie Ihren Kunden Ratenzahlung anbieten wollen, und zu welchem Zinssatz
* ob es für Ihre Produkte eventuell sinnvoll ist, verzögerten Zahlung anzubieten
  |br|
  Verzögerte Zahlung kann beispielsweise sinnvoll sein bei individualisierten Produkten, die Sie erst auf Bestellung fertigen.

Wo kann ich mich registrieren?
------------------------------

Händlerkonto bei Unzer registrieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Um ein Händlerkonto bei Unzer anzulegen, lassen Sie Unzer ein individuelles Angebot für Sie machen.

Rufen Sie dazu das Kontaktformular unter `www.unzer.com/de/kontakt-vertrieb <https://www.unzer.com/de/kontakt-vertrieb/>`_ auf.

Sobald alle Fragen geklärt sind, sendet Ihnen Unzer die Anmeldeinformationen, die Sie zum Konfigurieren brauchen.

Händlerkonto bei Apple Pay registrieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wenn Sie mit Unzer vereinbaren, dass Sie :productname:`Apple Pay` nutzen, dann müssen Sie ein separates Apple-Entwickler-Konto anlegen und Zugangsdaten generieren.

Weitere Informationen finden Sie unter :ref:`konfiguration:Optionen für Apple Pay: Zugangsdaten eingeben`.


.. Intern: oxdama, Status:

