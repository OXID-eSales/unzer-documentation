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

.. todo: Siehe https://github.com/OXID-eSales/unzer-module/blob/b-6.3.x/CHANGELOG.md:
        New country restrictions based on the Unzer documentation:
        done DE+EN: ALIPAY: DE, AT, BE, IT, ES, NL
        done DE+EN: Entf. Installment: DE, AT, CH (payment method deprecated) (Ratenzahlung mit Unzer)
        done DE+EN: Unzer Invoice (Paylater): DE, AT, CH, NL
        done: DE+EN: Prepayment: all Countries
        done: DE+EN  : WeChat: AT, BE, DK, FI, FR, DE, ES, GB, GR, HU, IE, IS, IT, LI, LU, MT, NL, NO, PT, SE
        done: Australien	 : nein: Österreich       Sofort Überweisung (Klarna Pay now)
.. todo: #EC: Was sind die offizielen Namen der folgenden Zahlungsarten auf EN und DE?
        SEPA Direct Debit: DE, AT
        Sofort: DE, AT, BE, IT, ES, NL

.. todo: Definitionseinschränkungen für Währungen ergänzen: verfügbar mit RC6

======================= ========================================================
Markt                   Zahlungsmethode
======================= ========================================================
Weltweit	            Apple Pay
Weltweit	            Kartenzahlung
Weltweit	            PayPal
Weltweit	            Unzer Vorkasse
Belgien	                Unzer Kauf auf Rechnung (Paylater)
Belgien 	            Alipay
Belgien	                SEPA-Lastschrift
Belgien	                Sofort Überweisung (Klarna Pay now)
Belgien	                WeChat
Belgien                 Bancontact
Dänemark	            Sofort Überweisung (Klarna Pay now)
Dänemark                WeChat
Deutschland	            Unzer Kauf auf Rechnung (Paylater)
Deutschland	            Alipay
Deutschland	            SEPA-Lastschrift
Deutschland	            Giropay
Deutschland	            Unzer Kauf auf Rechnung (Paylater)
Deutschland	            SEPA Lastschrift (abgesichert mit Unzer)
Deutschland	            Sofort Überweisung (Klarna Pay now)
Deutschland	            Unzer Bank Transfer (Überweisung)
Deutschland             WeChat
Estland	                Unzer Kauf auf Rechnung (Paylater)
Estland	                SEPA-Lastschrift
Finnland	            Unzer Kauf auf Rechnung
Finnland	            SEPA-Lastschrift
Finnland	            Sofort Überweisung (Klarna Pay now)
Finnland                WeChat
Frankreich	            Sofort Überweisung (Klarna Pay now)
Frankreich	            WeChat
Griechenland	        Unzer Kauf auf Rechnung (Paylater)
Griechenland	        SEPA-Lastschrift
Griechenland          	WeChat
Großbritannien	        Sofort Überweisung (Klarna Pay now)
Großbritannien      	WeChat
Irland	                Unzer Kauf auf Rechnung (Paylater)
Irland	                SEPA-Lastschrift
Irland	                WeChat
Island	                WeChat
Italien	                Unzer Kauf auf Rechnung (Paylater)
Italien 	            Alipay
Italien	                SEPA-Lastschrift
Italien	                WeChat
Lettland	            Unzer Kauf auf Rechnung (Paylater)
Lettland	            SEPA-Lastschrift
Liechtenstein           WeChat
Litauen	                Unzer Kauf auf Rechnung (Paylater)
Litauen	                SEPA-Lastschrift
Luxemburg	            Unzer Kauf auf Rechnung (Paylater)
Luxemburg	            SEPA-Lastschrift
Luxemburg	            WeChat
Malta	                Unzer Kauf auf Rechnung (Paylater)
Malta	                SEPA-Lastschrift
Malta   	            WeChat
Niederlande	            Alipay
Niederlande	            iDEAL
Niederlande	            Unzer Kauf auf Rechnung (Paylater)
Niederlande	            SEPA-Lastschrift
Niederlande	            Sofort Überweisung (Klarna Pay now)
Niederlande	            WeChat
Norwegen	            Sofort Überweisung (Klarna Pay now)
Norwegen	            WeChat
Österreich	            Alipay
Österreich	            eps Überweisung (Electronic Payment Standard)
Österreich	            Unzer Kauf auf Rechnung (Paylater)
Österreich	            Sofort Überweisung (Klarna Pay now)
Österreich	            SEPA-Lastschrift
Österreich	            Unzer Bank Transfer (Überweisung)
Österreich              WeChat
Polen	                Przelewy24
Polen	                Sofort Überweisung (Klarna Pay now)
Portugal	            Unzer Kauf auf Rechnung (Paylater)
Portugal	            SEPA-Lastschrift
Portugal	            Sofort Überweisung (Klarna Pay now)
Portugal	            WeChat
Schweden	            Sofort Überweisung (Klarna Pay now)
Schweden	            WeChat
Schweiz 	            Unzer Kauf auf Rechnung (Paylater)
Schweiz     	        Sofort Überweisung (Klarna Pay now)
Slowakei	            Unzer Kauf auf Rechnung (Paylater)
Slowakei	            SEPA-Lastschrift
Slowakei	            Sofort Überweisung (Klarna Pay now)
Slowenien	            Unzer Kauf auf Rechnung (Paylater)
Slowenien	            SEPA-Lastschrift
Spanien	                Unzer Kauf auf Rechnung (Paylater)
Spanien 	            Alipay
Spanien	                SEPA-Lastschrift
Spanien	                Sofort Überweisung (Klarna Pay now)
Spanien	                WeChat
Italien	                Sofort Überweisung (Klarna Pay now)
Tschechien	            Sofort Überweisung (Klarna Pay now)
Ungarn	                Sofort Überweisung (Klarna Pay now)
Ungarn	                WeChat
Vereinigte Staaten	    Sofort Überweisung (Klarna Pay now)
Zypern	                Unzer Kauf auf Rechnung (Paylater)
Zypern	                SEPA-Lastschrift
======================= ========================================================

Welche Märkte sind abgedeckt (sortiert nach Zahlungsmethoden)?
--------------------------------------------------------------

=============================================== ================
Zahlungsmethode                                 Markt
=============================================== ================
Alipay	                                        Belgien
Alipay	                                        Deutschland
Alipay	                                        Niederlande
Alipay	                                        Österreich
Alipay	                                        Italen
Alipay	                                        Spanien
Apple Pay                                       Weltweit
Bancontact	                                    Belgien
eps Überweisung (Electronic Payment Standard)	Österreich
Giropay	                                        Deutschland
iDEAL	                                        Niederlande
Kartenzahlung                                   Weltweit
PayPal	                                        Weltweit
Przelewy24	                                    Polen
Unzer Kauf auf Rechnung (Paylater)              Deutschland
Unzer Kauf auf Rechnung (Paylater)              Niederlande
Unzer Kauf auf Rechnung (Paylater)              Österreich
Unzer Kauf auf Rechnung (Paylater)              Schweiz
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
Sofort Überweisung (Klarna Pay now)	            Belgien
Sofort Überweisung (Klarna Pay now)	            Dänemark
Sofort Überweisung (Klarna Pay now)	            Deutschland
Sofort Überweisung (Klarna Pay now)	            Finnland
Sofort Überweisung (Klarna Pay now)	            Frankreich
Sofort Überweisung (Klarna Pay now)	            Großbritannien
Sofort Überweisung (Klarna Pay now)	            Niederlande
Sofort Überweisung (Klarna Pay now)	            Norwegen
Sofort Überweisung (Klarna Pay now)	            Österreich
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
Unzer Vorkasse	                                Weltweit
WeChat                                          Belgien
WeChat	                                        Deutschland
WeChat	                                        Dänemark
WeChat	                                        Finnland
WeChat	                                        Frankreich
WeChat	                                        Griechenland
WeChat	                                        Großbritannien
WeChat	                                        Irland
WeChat	                                        Italien
WeChat	                                        Liechtenstein
WeChat	                                        Luxemburg
WeChat	                                        Malta
WeChat	                                        Niederlande
WeChat	                                        Norwegen
WeChat	                                        Österreich
WeChat	                                        Portugal
WeChat	                                        Schweden
WeChat	                                        Spanien
WeChat	                                        Ungarn
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

