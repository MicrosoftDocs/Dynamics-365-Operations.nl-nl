---
title: Speciale betalingsterminals en -prompts voor een printer en kassalade
description: Dit onderwerp biedt informatie over de mogelijkheid om een speciale betalingsterminal te hebben en de gebruiker te vragen om een kassalade en een kassabonprinter te selecteren.
author: rubendel
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a3c7eb9580f9155dd33f6351f37eb1edd269a3d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018628"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Speciale betalingsterminals en -prompts voor een printer en kassalade

[!include [banner](includes/banner.md)]

Dit onderwerp biedt informatie over de mogelijkheid om een speciale betalingsterminal te hebben en de gebruiker te vragen om een kassalade en een kassabonprinter te selecteren.

## <a name="overview"></a>Overzicht

Moderne detailhandelaren zoeken naar manieren om de kassa-ervaring in winkels te stroomlijnen. Recente trends naar papierloze kassa's door middel van elektronische betalingen zijn niet alleen bedoeld om de inkoopervaring te versoepelen, maar beperken ook de noodzaak om over een volledig assortiment randapparatuur te beschikken voor iedere winkelmedewerker.

Microsoft Dynamics 365 Commerce ondersteunt deze trends door een scenario mogelijk te maken waarbij aan een POS-apparaat (Point of Sale) altijd een speciale betalingsterminal is toegewezen, maar hierbij geen eigen kassabonprinter of kassalade hoort. Wanneer medewerkers een ontvangstbewijs moeten afdrukken of een contante betaling moeten accepteren, worden ze gevraagd om een hardwarestation te selecteren waar deze apparaten zijn geconfigureerd.

## <a name="key-terms"></a>Belangrijke termen

| Voorwaarde | Omschrijving |
|---|---|
| Registreren | De entiteit die wordt gebruikt om een exemplaar van een POS-kassa te configureren. |
| Apparaat | Een representatie van het fysieke exemplaar van een POS-kassa en de toepassing Modern POS die hieraan is toegewezen. |
| Specifiek hardwarestation | De bedrijfslogica van het hardwarestation die is ingebouwd in de toepassingen Modern POS voor Windows en Modern POS voor Android. |
| D/k-poort (Drawer Kick) | Een traditionele methode om een kassalade aan te sluiten op een kassabonprinter. |
| Op netwerk aangesloten randapparaten | Ingebouwde ondersteuning voor netwerkbetalingsterminals, kassabonprinters en kassaladen. |

## <a name="supported-pos-clients-and-devices"></a>Ondersteunde POS-clients en -apparaten

De functionaliteit die in dit onderwerp wordt beschreven, wordt ondersteund door de clients Modern POS voor Windows en Modern POS voor Android.

Deze functie ondersteunt netwerkbetalingsterminals en kassabonprinters. U kunt ondersteuning voor kassalades bieden door de kassalade via de d/k-poort aan de netwerkprinter voor kassabonnen te koppelen.

Kant-en-klare ondersteuning voor deze functionaliteit wordt geboden door de [Dynamics 365-betalingsconnector voor Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3). Andere betalingsconnectors kunnen worden ondersteund via de Commerce-SDK voor betalingen. Ondersteunde kassabonprinters zijn onder andere netwerkprinters voor kassabonnen van Star Micronics en Epson.

Als u kassabonprinters van Star Micronics wilt instellen, gebruikt u het Star Micronics-printerhulpprogramma om het apparaat zo te configureren dat het via het netwerk kan worden gebruikt. Dit hulpprogramma biedt ook het IP-adres van het apparaat.

Als u Epson-kassabonprinters wilt instellen, gebruikt u het hulpprogramma Epson ePOS-Print om het apparaat in te stellen voor het gebruik van netwerkprotocollen.

Zie [Overzicht van ondersteuning voor netwerkrandapparaten](./dev-itpro/network-peripherals.md) voor meer informatie over het instellen van netwerkrandapparatuur.

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Een speciale betalingsterminals en prompt voor een printer en kassalade instellen

### <a name="set-up-hardware-profiles"></a>Hardwareprofielen instellen

U moet beschikken over twee typen hardwareprofielen. De eerste wordt toegewezen aan de kassa. De tweede wordt op het winkelniveau aan een hardwarestation toegewezen en wordt gebruikt om netwerkprinters voor kassabonnen en kassalades logisch te groeperen.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Een hardwareprofiel instellen voor de kassa

Voer de volgende stappen uit om het hardwareprofiel in te stellen dat aan de kassa is toegewezen.

1. Zoek in Dynamics 365 Commerce naar **Hardwareprofiel**.
2. Selecteer **Nieuw**.
3. Wijs een hardwareprofielnummer toe en voer vervolgens een omschrijving in. Dit hardwareprofiel wordt toegewezen aan de kassa zelf. Daarom is een omschrijving zoals **Specifiek met uitwijk** voldoende.
4. Stel op de sneltabbladen voor verschillende apparaattypen de volgende apparaattypen in.

    | Apparaat | Type | Apparaatnaam | Extra gegevens |
    |---|---|---|---|
    | Printer | Netwerk | *Alle* | De apparaatnaam is hoofdlettergevoelig. De **id van het ontvangstbewijsprofiel** moet gelijk zijn aan de **id van het ontvangstbewijsprofiel** die is toegewezen aan de netwerkprinter die is ingesteld in het hardwareprofiel dat is toegewezen aan het hardwarestation op kanaalniveau. |
    | Kassalade | Netwerk | *Alle* | De apparaatnaam is hoofdlettergevoelig. Stel de optie **Gebruik van gedeelde ploeg toestaan** in op **Ja**. |
    | EFT-service | Adyen | Niet van toepassing | Raadpleeg [Dynamics 365-betalingsconnector voor Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3) voor informatie over het configureren van de kant-en-klare Adyen-betalingsconnector. Andere betalingsconnectors kunnen worden ondersteund via de [Commerce-SDK voor betalingen](./dev-itpro/end-to-end-payment-extension.md). |
    | Pinapparaat | Netwerk | **MicrosoftAdyenDeviceV001** | Geen. |

5. Zoek in Dynamics 365 Commerce naar **Kassa's**.
6. Selecteer een kassa door het kassanummer te selecteren en selecteer vervolgens **Bewerken**.
7. Wijs het hardwareprofiel dat u zojuist hebt gemaakt aan de kassa toe die een specifieke betalingsterminal moet gebruiken. Het apparaat dat aan deze kassa wordt toegewezen, moet de toepassing Modern POS voor Windows of Modern POS voor Android gebruiken.
8. Selecteer **Opslaan**.
9. Selecteer in het actievenster op het tabblad **Kassa's** de optie **IP-adressen configureren**.
10. Voer op het sneltabblad **Pinapparaat** het IP-adres van de betalingsterminal in. Zie [Dynamics 365-betalingsconnector voor Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3) voor meer informatie over het ophalen van het IP-adres van de betalingsterminal met de Adyen-connector.
11. Selecteer **Opslaan**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Een hardwareprofiel instellen voor de kassabonprinter en kassalade

Voer de volgende stappen uit om het hardwareprofiel in te stellen dat wordt gebruikt om de netwerkprinter voor kassabonnen en kassalade te groeperen.

1. Zoek in Dynamics 365 Commerce naar **Hardwareprofiel**.
2. Selecteer **Nieuw**.
3. Wijs een hardwareprofielnummer toe en voer vervolgens een omschrijving in. Dit hardwareprofiel wordt gebruikt om de kassabonprinter en kassalade te groeperen. Daarom is een omschrijving zoals **Netwerkprinter en kassalade** voldoende.
4. Stel op de sneltabbladen voor verschillende apparaattypen de volgende apparaattypen in.

    | Apparaat | Type | Omschrijving | Extra gegevens |
    |---|---|---|---|
    | Printer | Netwerk | **Epson** of **Star** | De apparaatnaam is hoofdlettergevoelig. De **id van het ontvangstbewijsprofiel** moet gelijk zijn aan de **id van het ontvangstbewijsprofiel** die is toegewezen aan de printer die is ingesteld in het hardwareprofiel dat is toegewezen aan de kassa. |
    | Kassalade | Terugval | **Epson** of **Star** | De apparaatnaam is hoofdlettergevoelig. Stel de optie **Gebruik van gedeelde ploeg toestaan** in op **Ja**. |

5. Selecteer **Opslaan**.

### <a name="set-up-hardware-stations"></a>Hardwarestations instellen

U moet twee hardwarestations hebben. De eerste wordt toegewezen aan de kassa. De tweede wordt geselecteerd indien vereist, wanneer een ontvangstbewijs moet worden afgedrukt of een kassalade moet worden geopend.

#### <a name="register-a-hardware-station"></a>Een hardwarestation registreren

1. Zoek in Dynamics 365 Commerce naar **Alle winkels**.
2. Selecteer een winkel door de waarden voor **Id van detailhandelafzetkanaal** en vervolgens **Bewerken** te selecteren.
3. Selecteer op het sneltabblad **Hardwarestations** de optie **Toevoegen**.
4. Stel het veld **Type hardwarestation** in op **Specifiek**.
5. Voer een beschrijving in, maar stel geen andere waarden voor dit hardwarestation in. Dit hardwarestation wordt altijd gebruikt voor de kassa. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Een hardwarestation instellen voor de kassabonprinter en kassalade

1. Zoek in Dynamics 365 Commerce naar **Alle winkels**.
2. Selecteer een winkel door de waarden voor **Id van detailhandelafzetkanaal** en vervolgens **Bewerken** te selecteren.
3. Selecteer op het sneltabblad **Hardwarestations** de optie **Toevoegen**.
4. Stel het veld **Type hardwarestation** in op **Specifiek**.
5. Voer een omschrijving in. Dit hardwarestation wordt gebruikt voor de kassabonprinter en kassalade.
6. Selecteer in het veld **Hardwareprofiel** het hardwareprofiel dat u eerder voor de kassabonprinter en kassalade hebt gemaakt.
7. Selecteer **Opslaan**.
8. Terwijl het hardstation voor de kassabonprinter en de kassalade nog is geselecteerd, selecteert u **IP-adressen configureren**.
9. Haal het IP-adres voor de printer op en voer dit in als het IP-adres voor zowel de kassabonprinter als de kassalade.
10. Selecteer **Opslaan**.
11. Zoek naar **Distributiesplanningen**.
12. Selecteer distributieplanning **1090** en selecteer vervolgens **Nu uitvoeren**.
13. Selecteer distributieplanning **1070** en selecteer vervolgens **Nu uitvoeren**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Stel het systeem zo in dat wordt gevraagd om een kassabonprinter en kassalade te selecteren wanneer nodig.

1. Sluit de huidige ploeg in een ondersteunde POS-client als er een ploeg is geopend.
2. Meld u aan en selecteer **Niet-ladebewerkingen**.
3. Gebruik de bewerking **Hardwarestations beheren** om een hardwarestation in te schakelen.
4. Selecteer het hardwarestation dat u voor de kassa hebt gemaakt om dit actief te maken.
5. Meld u af en weer aan bij het POS en open een ploeg.

De betalingsterminal die aan het hardwareprofiel is toegewezen, is nu altijd actief en u wordt gevraagd of er een kassabonprinter of kassalade nodig is.

Veel verkopers die deze functie hebben aangevraagd, willen minder afval produceren door ontvangstbewijzen per e-mail te verzenden en elektronische betalingen te stimuleren. Afhankelijk van de configuratie van de POS, wordt winkelmedewerkers alleen gevraagd een kassabonprinter of kassalade te selecteren wanneer een klant een fysiek ontvangstbewijs wil of wil betalen.

Winkelmedewerkers wordt gevraagd om een hardwarestation slechts één keer per transactie te selecteren, tenzij een ontvangstbewijs moet worden afgedrukt en contant wordt betaald en het geselecteerde hardwareprofiel niet beide apparaten bevat. In dat geval wordt de winkelmedewerker opnieuw gevraagd om een hardwarestation te selecteren dat kan worden gebruikt om de transactie te voltooien.

## <a name="related-articles"></a>Gerelateerde artikelen

- [POS Hybrid-app instellen in Android en iOS](./dev-itpro/hybridapp.md)
- [Dynamics 365-betalingsconnector voor Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3)
- [Overzicht van ondersteuning voor netwerkrandapparaten](./dev-itpro/network-peripherals.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
