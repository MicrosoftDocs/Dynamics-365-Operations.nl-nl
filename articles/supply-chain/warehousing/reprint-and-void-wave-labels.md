---
title: Wavelabels opnieuw afdrukken en ongeldig maken
description: In dit onderwerp wordt uitgelegd hoe u bestaande wavelabels ongeldig kunt maken en opnieuw kunt afdrukken.
author: GarmMSFT
manager: PJacobse
ms.date: 07/09/2020
ms.topic: reprint-and-void-wave-labels
ms.service: dynamics-ax-applications
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 4c221a2817d71d79a5515379d2a33793660ebde5
ms.sourcegitcommit: 137e2bd30f0a85bd2e1baf1cf16b993edd2094f9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/09/2020
ms.locfileid: "3546418"
---
# <a name="reprint-and-void-wave-labels"></a>Wavelabels opnieuw afdrukken en ongeldig maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u labels beheert die door waveverwerking worden gegenereerd. (Zie [Wavelabels afdrukken configureren](../warehousing/configure-wave-label-printing.md) voor een gedetailleerde beschrijving en configuratie-instructies.)

U kunt wavelabels op elk gewenst moment opnieuw afdrukken. Het kan bijvoorbeeld zijn dat u één label wilt afdrukken als een bestaand label verloren is gegaan of beschadigd is geraakt. Het kan ook zijn dat een magazijnmedewerker of supervisor een hele rol labels moet opnieuw afdrukken als het nummer en/of de samenstelling van een hele reeks wavelabels is gewijzigd (bijvoorbeeld vanwege een voorraadtekort of andere redenen). Ook als alleen het aantal dozen is gewijzigd, moet de gehele rol opnieuw worden afgedrukt om te zorgen dat het totale aantal in de sectie "Doos X van Y" van elk label correct is.

De functie voor het opnieuw afdrukken van wavelabels ondersteunt de volgende functionaliteit:

- Druk labels opnieuw af via de magazijnapp of de rich client.
- Maak labels ongeldig en druk ze tegelijk opnieuw af. (De mogelijkheid om labels ongeldig te maken is bijvoorbeeld opgenomen in korte orderverzamelscenario's.)
- Schoon de wavelbelhistorie op.

Dit onderwerp bevat een verzameling scenario's met voorbeelden voor hoe u met de functie voor het opnieuw afdrukken van wavelabels kunt werken.

> [!IMPORTANT]
> Als u de scenario's wilt doorlopen die in dit onderwerp worden weergegeven, moet u eerst de relevante afdrukfuncties voor waves inschakelen en configureren, zoals wordt beschreven in [Wavelabels afdrukken configureren](../warehousing/configure-wave-label-printing.md). Diverse scenario's in dit onderwerp vereisen ook dat u eerst de scenario's in dat onderwerp doorloopt om vereiste voorbeeldgegevens te genereren.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>Scenario 1: Labels opnieuw afdrukken vanaf de webclient

U kunt wavelabels weergeven en opnieuw afdrukken op de volgende pagina's. Selecteer in het actievenster van elke pagina op het tabblad **Zendingen** in de groep **Verwante informatie** de optie **Wavelabels**.

- Alle zendingen \> Details van zending
- Alle ladingen \> Details van lading
- Alle waves
- Wavelabels
- Historie wavelabel

Voer de volgende stappen uit om een wavelabel opnieuw af te drukken vanaf de webclient.

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer de wave waarvoor u de labels opnieuw wilt afdrukken.
1. Selecteer in het actievenster op het tabblad **Wave** in de groep **Afdrukken** de optie **Wavelabels**.
1. Voer een of beide van de volgende stappen uit:

    - Selecteer in het veld **Printernaam** een printer als u het label opnieuw wilt afdrukken. (Laat dit veld leeg als u alleen de details van het wavelabel wilt bijwerken zonder het label opnieuw af te drukken.)
    - Schakel het selectievakje **Details van wavelabel bijwerken** in om het label bij te werken. (Laat dit selectievakje uitgeschakeld als u alleen het vorige label wilt afdrukken.)

    > [!NOTE]
    > Telkens wanneer een wavelabel wordt afgedrukt of opnieuw wordt afgedrukt, worden de bijbehorende gegevens geconverteerd via de desbetreffende indeling voor wavelabels en worden alle tijdelijke aanduidingen vervangen door werkelijke waarden. De resulterende tekenreeks wordt opgeslagen als een record in de wavelabelhistorie. Als het selectievakje **Details van wavelabel bijwerken** is uitgeschakeld, worden de opgeslagen ZPL-gegevens (Zebra Programming Language) gebruikt wanneer een label opnieuw wordt afgedrukt. Als het selectievakje **Details van wavelabel bijwerken** is ingeschakeld, wordt er een nieuwe tekenreeks gegenereerd. De bestaande wavelabels worden ook opnieuw berekend en eventuele overtollige labels (bijvoorbeeld als de gerelateerde werkregels zijn geannuleerd of gewijzigd) worden als **Ongeldig** gemarkeerd en worden niet opnieuw afgedrukt.

1. Klik op **OK** om uw selectie te bevestigen.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>Scenario 2: Labels opnieuw afdrukken vanuit de magazijnapp

Dit scenario is doorgaans van toepassing als een labelrol verloren is gegaan of beschadigd is geraakt. In dit voorbeeld ziet u hoe u menuopdrachten kunt instellen voor mobiele apparaten waarmee werknemers één en meerdere labels opnieuw kunnen afdrukken. Vervolgens wordt weergegeven hoe u deze nieuwe menuopdrachten gebruikt terwijl u met een mobiel apparaat werkt.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>De vereiste menuopdrachten en een menu voor het mobiele apparaat instellen

Voordat werknemers etiketten kunnen afdrukken vanaf een mobiel apparaat, moet u de menuopdrachten voor deze functionaliteit instellen en deze vervolgens toe te voegen aan het menu van de magazijnapp.

#### <a name="create-new-mobile-device-menu-items"></a>Nieuwe menuopdrachten maken voor een mobiel apparaat

Voer de volgende stappen uit om een nieuwe verzameling menuopdrachten te maken voor het opnieuw afdrukken van labels vanuit de magazijnapp.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Maak een menuopdracht en stel de volgende waarden in:

    - **Naam van menuopdracht:** *Eén wavelabel opnieuw afdrukken*
    - **Titel:** *Eén wavelabel opnieuw afdrukken*
    - **Modus:** *Indirect*
    - **Activiteitscode:** *Eén wavelabel opnieuw afdrukken*

1. Maak een tweede menuopdracht en stel de volgende waarden in:

    - **Naam van menuopdracht:** *Labels opnieuw afdrukken (artikel)*
    - **Titel:** *Wavelabels opnieuw afdrukken (artikel)*
    - **Modus:** *Indirect*
    - **Activiteitscode:** *Meerdere wavelabels opnieuw afdrukken*
    - **Groeperingsfilter voor werklijst weergeven:** *Ja*
    - **Systeemgroeperingsveld:** *ShipmentID*
    - **Systeemgroeperingslabel:** *ShipmentID*
    - **Afdrukmodus:** *Product*

1. Selecteer in het actievenster de **veldlijst** om een pagina te openen waar u de velden kunt selecteren die moeten worden weergegeven om werknemers de juiste labelrol te laten opgeven.
1. U kunt maximaal zeven velden weergeven. Gebruik de vervolgkeuzelijsten om het veld te selecteren dat op elke beschikbare positie wordt weergegeven. Laat alle velden leeg die u niet nodig hebt. 

    Dit is een voorbeeld:

    - **Weergaveveld:** *LabelItemId*
    - **Weergaveveld 2:** *LabelItemName*
    - **Weergaveveld 3:** *InventQty*
    - **Weergaveveld 4:** *LabelUnitId*

1. Sluit de pagina.
1. Maak een derde menuopdracht en stel de volgende waarden in:

    - **Naam van menuopdracht:** *Labels opnieuw afdrukken (opsomming)*
    - **Titel:** *Wavelabels opnieuw afdrukken (opsomming)*
    - **Modus:** *Indirect**
    - **Activiteitscode:** *Meerdere wavelabels opnieuw afdrukken*
    - **Groeperingsfilter voor werklijst weergeven:** *Ja*
    - **Systeemgroeperingsveld:** *ShipmentID*
    - **Systeemgroeperingslabel:** *ShipmentID*
    - **Afdrukmodus:** *Opsomming*

1. Selecteer in het actievenster de **veldlijst** en gebruik vervolgens de vervolgkeuzelijsten om de velden te selecteren die moeten worden weergegeven zodat werknemers de juiste labelrollen kunnen opgeven (bijvoorbeeld *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId* en *NumberOfLabels*).
1. Sluit de pagina.
1. Maak een vierde menuopdracht en stel de volgende waarden in:

    - **Naam van menuopdracht:** *Labels opnieuw afdrukken (met laatste)*
    - **Titel:** *Wavelabels opnieuw afdrukken (met laatste)*
    - **Modus:** *Indirect*
    - **Activiteitscode:** *Meerdere wavelabels opnieuw afdrukken*
    - **Groeperingsfilter voor werklijst weergeven:** *Ja*
    - **Systeemgroeperingsveld:** *ShipmentID*
    - **Systeemgroeperingslabel:** *ShipmentID*
    - **Afdrukmodus:** *Laatste juiste wavelabel-id*

1. Selecteer in het actievenster de **veldlijst** en gebruik vervolgens de vervolgkeuzelijsten om de velden te selecteren die moeten worden weergegeven zodat werknemers de juiste labelrollen kunnen opgeven (bijvoorbeeld *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId* en *NumberOfLabels*).
1. Sluit de pagina.

#### <a name="set-up-the-mobile-device-menu"></a>Het menu voor het mobiele apparaat instellen

Voer de volgende stappen uit om de nieuwe menuopdrachten toe te voegen aan het menu van de magazijnapp.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer een bestaand menu **Uitgaand**.
1. Zoek in de lijst aan de linkerkant de menuopdrachten voor opnieuw afdrukken die u zojuist hebt gemaakt en voeg deze toe aan de lijst aan de rechterkant met de pijl naar rechts.
1. Sluit de pagina.

### <a name="use-cases"></a>Scenario's

In de scenario's hieronder ziet u voorbeelden van menuopdrachten voor mobiele apparaten die u instelt om werknemers in staat te stellen wavelabels opnieuw af te drukken.

Voordat u deze toepassingen doorloopt, moet aan de volgende vereisten zijn voldaan:

- Er moeten demogegevens zijn geïnstalleerd en u moet de rechtspersoon **USMF** selecteren.
- Het afdrukken van wavelabels moet worden geconfigureerd en sommige labels moeten worden gegenereerd, zoals wordt beschreven in [Wavelabels afdrukken configureren](../warehousing/configure-wave-label-printing.md).

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Scenario 2.1: Eén wavelabel is onjuist en moet opnieuw worden afgedrukt.

1. Meld u aan bij de magazijnapp als een gebruiker die toegang heeft tot magazijn *62*. (In de standaard demogegevens kunt u zich aanmelden aan met *62* als gebruikers-id en *1* als wachtwoord.)
1. Ga naar **Uitgaand \> Eén wavelabel opnieuw afdrukken**.
1. Voer de wavelabel-id in of scan deze.
1. Selecteer de printer waarop u opnieuw wilt afdrukken.
1. Selecteer **OK** om de actie te bevestigen.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Scenario 2.2: er zijn meerdere labels voor dozen van hetzelfde artikel beschadigd en deze moeten opnieuw worden afgedrukt. Elk label heeft een productstreepjescode, maar geen opsomming of SSCC-nummer.

1. Meld u aan bij de magazijnapp als een gebruiker die toegang heeft tot magazijn *62*. (In de standaard demogegevens kunt u zich aanmelden aan met *62* als gebruikers-id en *1* als wachtwoord.)
1. Ga naar **Uitgaand \> Labels opnieuw afdrukken (artikel)**.
1. Voer de zending-id in of scan deze.
1. Selecteer de tegel met de labelrol die u opnieuw wilt afdrukken.
1. Scan de productstreepjescode van een bestaand label om te bevestigen dat de juiste regel is geselecteerd.
1. Voer het aantal labels in dat u opnieuw wilt afdrukken.
1. Selecteer de printer waarop u opnieuw wilt afdrukken.
1. Selecteer **OK** om de actie te bevestigen.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Scenario 2.3: Verschillende labels voor dozen zijn niet afgedrukt vanwege een storing in de printer. Omdat de labels een opsomming hebben, kunt u het bereik voor de dozen definiëren dat opnieuw moet worden afgedrukt.

1. Meld u aan bij de magazijnapp als een gebruiker die toegang heeft tot magazijn *62*. (In de standaard demogegevens kunt u zich aanmelden aan met *62* als gebruikers-id en *1* als wachtwoord.)
1. Ga naar **Uitgaand \> Labels opnieuw afdrukken (opsomming)**.
1. Voer de zending-id in of scan deze.
1. Selecteer de tegel met de labelrol die u opnieuw wilt afdrukken.
1. Voer de eerste doos in waarvoor u een label opnieuw wilt afdrukken.
1. Voer de laatste doos in waarvoor u een label wilt afdrukken. U kunt het veld ook leeg laten om de labels voor alle dozen na de eerst opgegeven doos opnieuw af te drukken.
1. Selecteer de printer waarop u opnieuw wilt afdrukken.
1. Selecteer **OK** om de actie te bevestigen.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Scenario 2.4: Verschillende labels voor dozen zijn niet afgedrukt vanwege een storing in de printer. Het laatste juiste label heeft een wavelabel-id die wordt afgedrukt als streepjescode.

1. Meld u aan bij de magazijnapp als een gebruiker die toegang heeft tot magazijn *62*. (In de standaard demogegevens kunt u zich aanmelden aan met *62* als gebruikers-id en *1* als wachtwoord.)
1. Ga naar **Uitgaand \> Labels opnieuw afdrukken (met laatste)**.
1. Voer de zending-id in of scan deze.
1. Selecteer de tegel met de labelrol die u opnieuw wilt afdrukken.
1. Voer de wavelabel-id van het laatste correcte wavelabel in of scan deze. De app geeft het volgende label in de reeks aan als de eerste doos waarvoor een label opnieuw wordt afgedrukt.
1. Voer de laatste doos in waarvoor u een label wilt afdrukken. U kunt het veld ook leeg laten om de labels voor alle dozen na de eerst opgegeven doos opnieuw af te drukken.
1. Selecteer de printer waarop u opnieuw wilt afdrukken.
1. Selecteer **OK** om de actie te bevestigen.

## <a name="scenario-3-short-pick-and-reprint"></a>Scenario 3: Kort orderverzamelen en opnieuw afdrukken

Voordat u dit scenario doorloopt, moet aan de volgende vereisten zijn voldaan:

- Er moeten demogegevens zijn geïnstalleerd en u moet de rechtspersoon **USMF** selecteren.
- Het afdrukken van wavelabels moet worden geconfigureerd en sommige labels moeten worden gegenereerd, zoals wordt beschreven in [Wavelabels afdrukken configureren](../warehousing/configure-wave-label-printing.md).

### <a name="set-up-work-exceptions"></a>Werkuitzonderingen instellen

Uitzonderingen voor werk bepalen het gedrag voor kort orderverzamelen. Voer de onderstaande stappen uit om een werkuitzondering te maken.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkuitzonderingen**.
1. Maak een record met de volgende instellingen:

    - **Code werkuitzondering:** *Kort orderverzamelen en afdrukken*
    - **Uitzonderingstype:** *Kort orderverzamelen*
    - **Voorstellen om wavelabels opnieuw af te drukken:** *Ja*

### <a name="void-and-reprint-after-a-short-pick"></a>Ongeldig maken en opnieuw afdrukken na kort orderverzamelen

1. Meld u aan bij de magazijnapp als een gebruiker die toegang heeft tot magazijn *62*. (In de standaard demogegevens kunt u zich aanmelden aan met *62* als gebruikers-id en *1* als wachtwoord.)
1. Open een werkstroom voor het werk van de verkooporder die is gemaakt bij het oorspronkelijk afdrukken van wavelabels.
1. Selecteer **Kort orderverzamelen**.
1. Selecteer de code voor de werkuitzondering die u voor dit scenario hebt gemaakt.
1. Als u de juiste uitzondering hebt geselecteerd, is het selectievakje **Ongeldig maken en opnieuw afdrukken** beschikbaar. Schakel dit selectievakje in en bevestig. Wanneer dit is bevestigd, wordt de labelrolreeks die is opgegeven in het veld **Label build-id** herberekend op basis van de hoeveelheid van de gewijzigde werkregel. Deze wordt vervolgens opnieuw afgedrukt op de opgegeven printer.
