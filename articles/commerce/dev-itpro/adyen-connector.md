---
title: Overzicht van Dynamics 365 Payment Connector voor Adyen
description: Dit artikel biedt een overzicht van de Microsoft Dynamics 365-betalingsconnector voor Adyen.
author: rassadi
ms.date: 10/27/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 931fc69cda8daa2e06b6f1155fbf0369fd2bca55
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728304"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Overzicht van Dynamics 365 Payment Connector voor Adyen

[!include [banner](../includes/banner.md)]

Dit artikel biedt een overzicht van de Microsoft Dynamics 365-betalingsconnector voor Adyen en omvat een uitgebreide lijst van ondersteunde functies. Gerelateerde artikelen hebben betrekking op het aanmelden bij Adyen, de configuratie van de connector, veelgestelde vragen en richtlijnen voor het oplossen van enkele veelvoorkomende problemen.

## <a name="key-terms"></a>Belangrijke termen

| Voorwaarde | Description |
|---|---|
| Betalingsconnector | Een extensie die de communicatie tussen Microsoft Dynamics 365 Commerce (en gekoppelde onderdelen) en een betalingsservice mogelijk maakt. De connector die in dit artikel wordt beschreven, is geïmplementeerd met de standaard-SDK voor betalingen. |
| Kaart aanwezig | Verwijst naar betalingstransacties waarbij een fysieke kaart wordt gepresenteerd en gebruikt op een betalingsterminal die is verbonden met het Dynamics 365-verkooppunt. |
| Kaart niet aanwezig | Verwijst naar betalingstransacties waarbij geen fysieke kaart aanwezig is, zoals e-commerce- of callcenterscenario's. In deze scenario's worden de betalingsgegevens handmatig ingevoerd op een e-commercewebsite, in een callcenterstrom of op de POS- of betalingsterminal. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Ondersteunde functies, functionaliteit, versies en terminals

De kant-en-klare Dynamics 365-betalingsconnector voor Adyen gebruikt de standaard-SDK voor betalingen. Daarom bevat het geen speciale mogelijkheden die niet ook beschikbaar zijn voor andere betalingsconnectors.

### <a name="supported-versions"></a>Ondersteunde versies

#### <a name="microsoft-dynamics-365-supported-versions"></a>Ondersteunde Microsoft Dynamics 365-versies
De first-party, kant-en-klare Dynamics 365-betalingsconnector voor Adyen wordt ondersteund in Microsoft Dynamics 365 Finance 8.1.3 (januari 2019) en hoger, en in Microsoft Dynamics 365 Retail 8.1.3 en hoger. Derden kunnen echter nog wel andere betalingsconnectors voor Adyen ontwikkelen voor eerdere versies van Microsoft Dynamics 365.

#### <a name="supported-adyen-firmware-versions"></a>Ondersteunde firmwareversies van Adyen

In de onderstaande lijst worden de minimale en maximale Adyen-versies beschreven die worden ondersteund voor elke versie van het Microsoft Dynamics 365 Retail POS.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Versie 10.0.25 van Dynamics 365 Retail POS
| Minimale Adyen-firmwareversie | Maximale Adyen-firmwareversie |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Versie 10.0.26 van Dynamics 365 Retail POS
| Minimale Adyen-firmwareversie | Maximale Adyen-firmwareversie |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Versie 10.0.27 van Dynamics 365 Retail POS
| Minimale Adyen-firmwareversie | Maximale Adyen-firmwareversie |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Versie 10.0.28 van Dynamics 365 Retail POS
| Minimale Adyen-firmwareversie | Maximale Adyen-firmwareversie |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Versie 10.0.29 van Dynamics 365 Retail POS
| Minimale Adyen-firmwareversie | Maximale Adyen-firmwareversie |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Versie 10.0.30 van Dynamics 365 Retail POS
| Minimale Adyen-firmwareversie | Maximale Adyen-firmwareversie |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Mogelijk brengt Adyen kleine versie-updates uit nadat Microsoft de grote versie heeft getest. Zolang een grote versie wordt ondersteund, zijn kleine versie-updates binnen dezelfde grote versie geen probleem. Deze updates zijn doorgaans zeer gerichte fixes en voldoen niet aan de criteria voor volledig opnieuw testen, zolang dezelfde grote firmwareversie eerder is getest. De vermelde maximumversie van Adyen-firmware in documentatie mag niet worden overschreden. 
>
> De migratie van een Adyen-fimwareversie vóór versie 53 naar versie 53 vereist POS-kb **4577957** voor maandelijkse updates van Commerce-versies 10.0.11 tot en met 10.0.14. Als een van deze versies in gebruik is en de hotfix niet bevat, zijn na de upgrade van de betalingsterminal alleen betalingen via NFC toegestaan. Dit probleem wordt verholpen door de hotfix toe te passen op het POS. Als de POS-versie ouder is dan versie 10.0.11, kunt u een ondersteuningsverzoek indienen om aan te geven dat een oplossing voor KB **4577957** vereist is voor een niet-werkend MPOS.
> 
> Voor Adyen-firmwareversies 59p7 tot en met 62p9 wordt bij de bewerking **uitbetaling van geschenkkaart** twee keer om PIN-invoer gevraagd in gevallen waarin de geschenkkaart handmatig wordt ingevoerd. Dit probleem doet zich niet voor wanneer de geschenkkaart wordt ingelezen. Adyen onderzoekt dit. 

### <a name="supported-payment-terminals"></a>Ondersteunde betalingsterminals
De Dynamics 365-betalingsconnector voor Adyen maakt gebruik van de apparaatonafhankelijke [Adyen Payment Terminal-API](https://www.adyen.com/blog/introducing-the-terminal-api). Deze ondersteunt alle betalingsterminals die door deze API (Application Programming Interface) worden ondersteund. Zie de pagina [Adyen POS-terminals](https://www.adyen.com/pos-payments/terminals) voor een volledige lijst met ondersteunde betalingsterminals .

### <a name="supported-payment-instruments"></a>Ondersteunde betaalmiddelen

#### <a name="supported-debit-and-credit-cards"></a>Ondersteunde betaalkaarten en creditcards

| Merk | Variant | Kaart aanwezig | e-Commerce | Callcenter |
|---|---|:-:|:-:|:-:|
| MasterCard | Credit | ✔ | ✔ | ✔ |
| MasterCard | Debet | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VISA | Credit | ✔ | ✔ | ✔ |
| VISA | Debet | ✔ | ✔ | ✔ |
| VISA | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA Aravia Card | ✔ | ✔ | ✔ |
| AMEX | Credit | ✔ | ✔ | ✔ |
| AMEX | Debet | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Commercial | ✔ | ✔ | ✔ |
| AMEX | AMEX Consumer | ✔ | ✔ | ✔ |
| AMEX | AMEX Corporate | ✔ | ✔ | ✔ |
| AMEX | AMEX Small Business | ✔ | ✔ | ✔ |
| Discover | Standaard | ✔ | ✔ | ✔ |
| Discover | Android Pay | ✔ |  |  |
| Discover | Apple Pay | ✔ |  |  |
| Discover | Samsung Pay | ✔ |  |  |
| Diners   | Standaard | ✔ | ✔ | ✔ |
| Dineromail | Standaard | ✔ | ✔ | ✔ |
| JCB | Standaard | ✔ | ✔ | ✔ |
| Union Pay\* | Standaard | ✔ |  |  |
| Interac Debit\* | Standaard | ✔ |  |  |

\*De terugkerende kaarttokens van Interac en Union Pay worden niet geleverd door Adyen, dus ze kunnen niet worden ondersteund voor kaartloze transacties.

#### <a name="supported-gift-cards"></a>Ondersteunde geschenkbonnen
| Schema | Kaart aanwezig | Kaart niet aanwezig |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

U moe extra stappen uitvoeren om deze externe geschenkkaartschema's via de Dynamics 365-betalingsonnector voor Adyen te ondersteunen. Zie [Ondersteuning voor externe geschenkkaarten](/dynamics365/unified-operations/retail/dev-itpro/gift-card) voor meer informatie.

#### <a name="supported-wallets"></a>Ondersteunde wallets

| Schema | Kaart aanwezig | Kaart niet aanwezig |
|---|---|---|
| Alipay | Ondersteuning wordt toegevoegd in een toekomstige versie. | Nr. |
| WeChat | Ondersteuning wordt toegevoegd in een toekomstige versie. | Nr. |

#### <a name="supported-card-present-input-methods"></a>Ondersteunde invoermethoden met kaart
| Invoermethode | Ondersteund | Opmerkingen |
|---|:-:|---|
| Insteken | ✔ | |
| Doorhalen | ✔ | |
| Aanraken | ✔ | |
| Handmatige invoer via POS-gebruikersinterface. |  | Wordt op dit moment niet ondersteund |
| Handmatige invoer via betalingsterminal. | ✔ | Ondersteunt handmatige invoer van creditcards, betaalpassen en geschenkkaarten met invoer van pincode. | 


#### <a name="supported-card-present-countries"></a>Landen waar transacties met kaart worden ondersteund

In de volgende landen zijn Commerce-onderdelen beschikbaar en worden transacties met kaart ondersteund door Adyen. Ga naar de pagina [Internationale beschikbaarheid](/dynamics365/get-started/availability) voor de huidige internationale beschikbaarheid van Commerce.

| Land/regio | Ondersteund |
| --- | :-: |
| Australië | ✔ |
| Oostenrijk | ✔ |
| België | ✔ |
| Canada | ✔ |
| Tsjechische Republiek | ✔ |
| Denemarken | ✔ |
| Estland | ✔ |
| Finland | ✔ |
| Frankrijk | ✔ |
| Duitsland | ✔ |
| Hongkong | ✔ |
| Hongarije | ✔ |
| IJsland | ✔ |
| Ierland | ✔ |
| Italië | ✔ |
| Japan | Toekomstige versie |
| Letland | ✔ |
| Litouwen | ✔ |
| Maleisië | ✔ |
| Nederland | ✔ |
| Nieuw-Zeeland | ✔ |
| Noorwegen | ✔ |
| Polen | ✔ |
| Singapore | ✔ |
| Zwitserland | ✔ |
| Spanje | ✔ |
| Zweden | ✔ |
| Zwitserland | ✔ |
| Verenigd Koninkrijk | ✔ |
| Verenigde Staten | ✔ |
| Brazilië | Toekomstige versie |

#### <a name="supported-card-not-present-countries"></a>Landen waar transacties zonder kaart worden ondersteund

De volgende landen worden door Adyen ondersteund voor transacties zonder kaart. [Neem contact op met Adyen](https://www.adyen.com/contact/sales) voor meer informatie over ondersteuning voor een specifiek land. Ga naar de pagina [Internationale beschikbaarheid](/dynamics365/get-started/availability) voor de huidige internationale beschikbaarheid van Commerce.

| Land/regio | 
| --- |
| Argentinië |
| Armenië |
| Australië |
| Oostenrijk |
| Bahrein |
| België |
| Brazilië |
| Bulgarije |
| Canada |
| Chili |
| China |
| Colombia |
| Kroatië |
| Cyprus |
| Tsjechische Republiek  |
| Denemarken |
| Egypte |
| Estland |
| Finland |
| Frankrijk |
| Georgië |
| Duitsland |
| Gibraltar |
| Griekenland |
| Guernsey |
| Hongkong |
| Hongarije |
| IJsland |
| India |
| Indonesië |
| Ierland |
| Isle of Man |
| Israël |
| Italië |
| Japan |
| Jersey |
| Korea |
| Koeweit |
| Letland |
| Litouwen |
| Luxemburg |
| Maleisië |
| Malta |
| Mexico |
| Marokko |
| Nederland |
| Nieuw-Zeeland |
| Noorwegen |
| Peru |
| Polen |
| Portugal |
| Qatar |
| Roemenië |
| Saoedi-Arabië |
| Servië |
| Singapore |
| Slowakije |
| Slovenië |
| Zuid-Afrika |
| Spanje |
| Zweden |
| Zwitserland |
| Taiwan |
| Tanzania |
| Thailand |
| Turkije |
| Verenigde Arabische Emiraten (VAE) |
| Verenigd Koninkrijk |
| Verenigde Staten van Amerika, inclusief Puerto Rico  |

#### <a name="supported-dynamics-365-payment-features"></a>Ondersteunde betalingsfuncties van Dynamics 365

De volgende tabel bevat de functies die door de Dynamics 365-betalingsconnector voor Adyen worden ondersteund. Deze functies maken gebruik van verbeteringen die in december 2018 zijn geïntroduceerd in de betalings-SDK en een aantal onderdelen. Deze zijn niet exclusief voor de Dynamics 365-betalingsconnector voor Adyen. Zie [Een integratie van een end-to-end-betaling voor een betalingsterminal maken](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension) voor meer informatie over het opnemen van deze verbeteringen voor een andere betalingsconnector.

| Schema | Kaart aanwezig | Kaart niet aanwezig |
|---|:-:|:-:|
| [Contant geld voor geschenkbonsaldo](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Bescherming tegen dubbele betaling](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Tokenisatie voor meerdere kanalen | ✔ | ✔ |
| Gekoppelde restituties | ✔<br>(Vanaf 10.0.1) | ✔<br>(Vanaf 10.0.1) |
| [Online betalingen opslaan](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Vanaf 10.0.2) | 
| [Externe geschenkbonnen voor callcenter en e-commerce](./gift-card.md) | ✔<br>(Vanaf 10.0.10) | 
| [Omleiding van SCA-betalingen](../adyen_redirect.md) | | ✔<br>(Vanaf 10.0.12) |
| [Speciale betalingsterminals en -prompts voor een printer en kassalade](../pos-multi-hws.md) | ✔<br>(Vanaf 10.0.12) | |
| [Ondersteuning voor fooien op SDK-niveau via de Adyen-connector](tipping.md) | ✔<br>(Vanaf 10.0.14) | |
| [Incrementeel registreren voor orderfacturering](incremental-capture.md) |  | ✔<br>(Vanaf 10.0.18) |
| [Walletbetalingen](../wallets.md) |  | ✔<br>(Vanaf 10.0.20) |
| [Google Pay met Adyen](google-pay-adyen.md) |  | ✔<br>(Vanaf 10.0.27) |

## <a name="next-steps"></a>Volgende stappen

Raadpleeg [Dynamics 365-betalingsconnector voor Adyen instellen](adyen-connector-setup.md) voor meer informatie over het instellen en configureren van de Dynamics 365-betalingsconnector voor Adyen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Dynamics 365 Payment Connector voor Adyen instellen](adyen-connector-setup.md)

[Veelgestelde vragen over Dynamics 365 Payment Connector voor Adyen](adyen-connector-faq.md)

[Problemen met Dynamics 365 Payment Connector voor Adyen oplossen](adyen-connector-troubleshoot.md)

[Veelgestelde vragen over betalingen](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
