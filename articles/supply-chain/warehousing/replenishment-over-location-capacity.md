---
title: Aanvulling boven locatiecapaciteit
description: Dit onderwerp biedt informatie over de functie Aanvulling boven locatiecapaciteit. Deze functie schakelt alle aanvullingswerk in dat nodig is voor de dag om te worden gemaakt en beheert de beschikbaarheid van dat aanvullingswerk om ervoor te zorgen dat de verzamellocatie niet door voorraad heen raakt en ook niet boven de capaciteit komt.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 309df56671bf258e1669ae6d5393de01e2b500f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823234"
---
# <a name="replenishment-over-location-capacity"></a>Aanvulling boven locatiecapaciteit

[!include [banner](../includes/banner.md)]

In sommige magazijnen met een groot volume of weinig ruimte moeten meer artikelen in een dag worden verzonden dan op de verzamellocatie passen. De functie *Aanvulling boven locatiecapaciteit* schakelt alle aanvullingswerk in dat nodig is voor de dag om te worden gemaakt en beheert de beschikbaarheid van dat aanvullingswerk om ervoor te zorgen dat de verzamellocatie niet door voorraad heenraakt en ook niet boven de capaciteit komt.

Met de functie kan meer aanvullingswerk worden gemaakt dan op een locatie past en wordt voltooiing van aanvullingswerk geblokkeerd wanneer de locatie vol is. Als voorraad op de verzamellocatie daalt onder een configureerbare drempel, wordt meer aanvullingswerk beschikbaar gesteld.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>De functie Aanvulling boven locatiecapaciteit inschakelen

Als u deze functie beschikbaar wilt maken, schakelt u de volgende functies in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in (in deze volgorde):

1. Werk blokkeren voor de hele organisatie
1. Aanvulling boven locatiecapaciteit

## <a name="set-up-the-feature-for-the-example-scenario"></a>De functie instellen voor het voorbeeldscenario

Deze sectie bevat richtlijnen en een voorbeeld waarin wordt uitgelegd hoe u deze functie instelt en voorbeeldgegevens voorbereidt voor het voorbeeldscenario dat verderop in dit onderwerp wordt gegeven.

### <a name="enable-sample-data"></a>Voorbeeldgegevens inschakelen

Als u het [voorbeeldscenario](#example-scenario) wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

### <a name="location-profile"></a>Locatieprofiel

Schakel de functionaliteit voor aanvulling boven capaciteit in het locatieprofiel in.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.
1. Selecteer **PICK-06** in het linkerdeelvenster.
1. Selecteer **Bewerken** in het actievenster.
1. Stel op het sneltabblad **Aanvulling** de volgende waarden in:

    - **Locatiecapaciteit overschrijven:** *Ja*

        Indien ingeschakeld, mag de maximale capaciteit van de locatie worden overschreden door aanvullingswerk. Hierdoor worden ook andere velden op het sneltabblad **Aanvulling** ingeschakeld.

    - **Drempeltype werkbeschikbaarheid:** *Hoeveelheid*

        Dit veld bepaalt de methode die wordt gebruikt om te bepalen wanneer meer werk moet worden vrijgegeven. U kunt vrijgeven op hoeveelheid of percentage:

        - *Percentage*: selecteer deze optie om percentagecapaciteit te gebruiken die is gebaseerd op voorraadlimieten of volumes. Als u deze optie selecteert , wordt het veld **Overschrijdingspercentage** ingeschakeld en worden de twee hoeveelheidsvelden, **Overschrijdingshoeveelheid** en **Overschrijdingseenheid** uitgeschakeld.

            U kunt deze optie gebruiken als de verzamellocaties volumes gebruiken.

            Als deze optie is geselecteerd, stelt u het veld **Overschrijdingspercentage** in op het percentage waarbij meer aanvullingswerk beschikbaar wordt gemaakt.

        - *Hoeveelheid*: selecteer deze optie om een specifieke hoeveelheidswaarde te gebruiken. Als u deze optie selecteert , wordt het veld **Overschrijdingspercentage** uitgeschakeld en worden de twee hoeveelheidsvelden, **Overschrijdingshoeveelheid** en **Overschrijdingseenheid** ingeschakeld.

            Gebruik deze optie wanneer u geen volumes gebruikt voor de locaties die worden aangevuld, of wanneer u consistente hoeveelheden hebt waarbij meer voorraad naar de locatie moet worden gebracht.

           Als deze optie is geselecteerd, stelt u de velden **Overschrijdingshoeveelheid** en **Overschrijdingseenheid** in op de hoeveelheid waarbij meer aanvullingswerk beschikbaar wordt gemaakt.

    - **Overschrijdingshoeveelheid:** *0,65*

        In dit veld wordt de hoeveelheid gedefinieerd waarbij de locatie overloopt.

        Werk is beschikbaar wanneer de som van de voorhanden voorraad op de locatie en de werkhoeveelheid onder deze waarde ligt. Aanvullingswerk dat boven deze waarde ligt, wordt geblokkeerd en moet handmatig worden gedeblokkeerd.

        Met locatievoorraadlimieten wordt rekening gehouden wanneer de werkhoeveelheid wordt berekend.

    - **Overschrijdingseenheid:** *PL*

        In dit veld wordt de eenheid gedefinieerd die aan de overschrijdingseenheid is gekoppeld.

        In dit geval wordt meer aanvullingswerk beschikbaar gesteld wanneer de locatie zakt tot 0,65 pallet (PL).

    - **Overlooppercentage**

        In dit veld wordt het percentage gedefinieerd waarbij de locatie overloopt.

        Werk is beschikbaar wanneer de som van de voorhanden voorraad op de locatie en de werkhoeveelheid onder dit percentage ligt. Een hoeveelheidspercentage aanvullingswerk dat boven deze waarde ligt, wordt geblokkeerd en moet handmatig worden gedeblokkeerd.

        Met locatievoorraadlimieten wordt rekening gehouden wanneer het percentage wordt berekend. Als er geen locatievoorraadlimieten zijn gedefinieerd, wordt het percentage werkhoeveelheid berekend op basis van volume als volumebeperkingen voor het locatieprofiel zijn gedefinieerd.

> [!IMPORTANT]
> Als u de demogegevens voor de rechtspersoon **USMF** gebruikt en eerder de functie *Positionering van locatie nummerplaat* hebt ingeschakeld , moet u de instelling **Positionering van nummerplaat inschakelen** uitschakelen voor het locatieprofiel **BULK-06** om de mobiele stappen in het voorbeeldscenario te voltooien.

### <a name="wave-step-code"></a>Stapcode wave

> [!NOTE]
> Als u een wave-stapcode wilt instellen, zoals hier wordt beschreven, moet u eerst [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de functie in te schakelen met de naam *Organisatiebrede wave-stapcode inschakelen*.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wave-stapcodes**.
1. Selecteer **Nieuwe** en stel de volgende waarden in:

    - **Wave-stapcode:** *Aanvulling*
    - **Beschrijving wavestap:** *Aanvulling*
    - **Type wavestap:** *Aanvulling*

1. Selecteer **Opslaan**.

### <a name="replenishment-template"></a>Aanvullingssjabloon

Aanvullingssjablonen zijn een set regels die bepalen wanneer en hoe een locatie wordt aangevuld.

1. Ga naar **Magazijnbeheer \> Instellen \> Aanvulling \> Aanvullingssjablonen**.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer in de sectie **Overzicht** de regel waar het veld **Aanvullingssjabloon** is ingesteld op *Vraag aanvullen*.
1. Stel de volgende waarden in:

    - **Wave-stapcode:** *Aanvulling*
    - **Gebruik van niet-gereserveerde hoeveelheid door waveaanvraag toestaan:** *Ja*

1. Selecteer **Opslaan**.

### <a name="wave-template"></a>Wavesjabloon

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Stel in het linkerdeelvenster het veld **Type wavesjabloon** in op *Verzenden*.
1. Selecteer de sjabloon **61 Verzending** in de lijst.
1. Selecteer **Bewerken** in het actievenster.
1. Stel op het sneltabblad **Algemeen** de optie **Vrijgave van aanvullingswerk automatiseren** in op *Ja*.

    Stel deze optie in op *Ja* om op vraag gebaseerd aanvullingswerk te maken en dit automatisch vrij te geven. U moet de methode van de aanvullingswave toevoegen aan de wavesjabloon en een aanvullingssjabloon maken van het type **Waveaanvraag**. Stel een aanvullingssjabloon in de pagina **Aanvullingssjablonen** in. Als u een aanvullingssjabloon wilt instellen, moet u de aanvullingsmethode toevoegen aan de wavesjabloon.

1. Zoek op het sneltabblad **Methoden** in de kolom **Geselecteerde methoden** naar de volgende regel:

    - **Naam van methode:** *Aanvullen*
    - **Naam:** *Aanvulling*

1. Stel het veld **Wave-stepcode** voor deze regel in op *Aanvulling*.
1. Selecteer **Opslaan**.

## <a name="example-scenario"></a>Voorbeeldscenario

Nadat u alle eerder beschreven voorbeeldgegevens hebt gemaakt en ingesteld, kunt u dit scenario doorlopen om de functie *Aanvulling boven locatiecapaciteit* uit te proberen. Bij de waarden die in dit scenario worden weergegeven, wordt ervan uitgegaan dat u werkt met de standaarddemonstratiegegevens, dat u de rechtspersoon **USMF** hebt geselecteerd en dat u de voorbeeldrecords hebt voorbereid die eerder in dit onderwerp zijn beschreven. Dit scenario dient ook als voorbeeld waarin wordt aangegeven hoe de functie in een productie-instelling kan worden gebruikt.

### <a name="create-replenishment-work"></a>Aanvullingswerk maken

#### <a name="create-sales-order-1"></a>Verkooporder 1 maken

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer in het actievenster de optie **Nieuw** om een dialoogvenster te openen voor het maken van een nieuwe verkooporder.
1. Stel in het dialoogvenster de volgende waarden in:

    - **Klantrekening:** *US-007*
    - **Magazijn:** *61*

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Deze bevat een nieuwe, lege rij op het sneltabblad **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *T0100*
    - **Hoeveelheid:** *40*

1. Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.
1. Selecteer op de pagina **Reservering** **Partij reserveren**.
1. Sluit de pagina.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    U ontvangt informatieve meldingen waarin de wave-id en zending-id worden vermeld die zijn gemaakt. Er wordt ook een aanvullingswave gemaakt.

    U ontvangt ook een waarschuwingsbericht met de mededeling dat de blokkering van Werk-ID XXXX niet ongedaan kan worden gemaakt omdat deze onvoltooid aanvullingswerk bevat.

#### <a name="create-sales-order-2"></a>Verkooporder 2 maken

1. Selecteer op de pagina **Alle verkooporders** in het actievenster de optie **Nieuw** om een dialoogvenster te openen voor het maken van een nieuwe verkooporder.
1. Stel in het dialoogvenster de volgende waarde in:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *61*

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Deze bevat een nieuwe, lege rij op het sneltabblad **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *T0100*
    - **Hoeveelheid:** *60*

1. Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.
1. Selecteer op de pagina **Reservering** **Partij reserveren**.
1. Sluit de pagina.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    U ontvangt informatieve meldingen waarin de wave-id en zending-id worden vermeld die zijn gemaakt. Er wordt ook een aanvullingswave gemaakt.

    U ontvangt ook een waarschuwingsbericht met de mededeling dat de blokkering van Werk-ID XXXX niet ongedaan kan worden gemaakt omdat deze onvoltooid aanvullingswerk bevat.

#### <a name="create-sales-order-3"></a>Verkooporder 3 maken

1. Selecteer op de pagina **Alle verkooporders** in het actievenster de optie **Nieuw** om een dialoogvenster te openen voor het maken van een nieuwe verkooporder.
1. Stel in het dialoogvenster de volgende waarden in:

    - **Klantrekening:** *US-004*
    - **Magazijn:** *61*

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Deze bevat een nieuwe, lege rij op het sneltabblad **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *T0100*
    - **Hoeveelheid:** *30*

1. Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.
1. Selecteer op de pagina **Reservering** **Partij reserveren**.
1. Sluit de pagina.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    U ontvangt informatieve meldingen waarin de wave-id en zending-id worden vermeld die zijn gemaakt. Er wordt ook een aanvullingswave gemaakt.

    U ontvangt ook een waarschuwingsbericht met de mededeling dat de blokkering van Werk-ID XXXX niet ongedaan kan worden gemaakt omdat deze onvoltooid aanvullingswerk bevat.

#### <a name="view-work-details"></a>Werkdetails weergeven

1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. Filter in de sectie **Overzicht** de kolom **Magazijn** voor magazijn *61*.
1. U ziet dat er zeven werk-id's zijn gemaakt voor de drie vraagverkooporders.

    - Drie van de zeven werk-id's hebben de **werkordertype**-waarde *Aanvulling* en vier hebben de **werkordertype**-waarde *Verkooporders*.
    - Alle drie de werk-id's met een **werkordertype**-waarde van *Aanvulling* hebben dezelfde *verzamel-* en *wegzet*-locaties in de sectie **Regels**:

        - **Verzamelen:** *02A01R5S1B*
        - **Wegzetten:** *06A01R2S1B*

    - Er zijn twee werk-id's gemaakt voor verkooporder 1.

1. Noteer de werk-id's van de verkooporders.

Afhankelijk van de voorhanden hoeveelheden kunnen de hoeveelheden werk die worden gemaakt, enigszins variëren. De gemaakte werkkoppen moeten echter wel overeenkomen met dit scenariovoorbeeld.

#### <a name="on-hand-inventory-license-plate-id"></a>Nummerplaat-id van voorhanden voorraad

Verderop in dit scenario gebruikt u de mobiele app Magazijnbeheer (of een emulator), waarin u de nummerplaat moet identificeren om de scenario's voor verzameling en aanvulling te voltooien.

Voer de volgende stappen uit om de nummerplaat-id's te vinden die u later nodig hebt.

1. Ga naar **Voorraadbeheer \> Query's en rapporten \> Voorhanden voorraad**.
1. Selecteer de knop **Filters weergeven** om het filterdeelvenster te openen.
1. Voer de volgende filtercriteria in om de nummerplaten voor het scenario op te halen. Gebruik het filter *begint met*.

    - **Artikelnummer:** *T0100*
    - **Magazijn:** *61*

1. Selecteer **Toepassing**.
1. Selecteer in het actievenster de optie **Dimensies**.
1. Selecteer in het dialoogvenster **Weergave van dimensies** in de sectie **Opslagdimensies** alle waarden.
1. Selecteer in de sectie **Transacties** **Artikelnummer** en **Hoeveelheid \<\> 0**.
1. Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster te sluiten.
1. Het raster **Voorhanden** toont de nummerplaatnummers voor artikel *T0100* op elke locatie. Noteer de nummerplaat die zich op elke locatie bevindt, want u hebt deze gegevens later nodig.
1. Sluit de pagina.

### <a name="process-steps"></a>Processtappen

U voert de magazijnlocatieaanvulling uit voor de eerste twee werk-Id's. Werk aan het derde aanvullingswerk wordt geblokkeerd totdat het voorraadniveau op de verzamellocatie onder de drempel valt.

#### <a name="replenishment"></a>Aanvulling

1. Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker in magazijn *61*. (Geef *61* op als gebruikers-id en *1* als wachtwoord.)
1. Ga naar **Voorraad \> Aanvulling**.

    U wordt gevraagd om het eerste aanvullingswerk te voltooien. Het artikelnummer, de hoeveelheid en de locatie waar moet worden verzameld, worden weergegeven.

1. Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.
1. Klik op de knop **OK** (vinkjesymbool).

    Het systeem genereert een nummerplaatnummer voor de nieuwe nummerplaat voor het verzamelde artikel.

1. Selecteer **OK** om de waarde te bevestigen.

    Er wordt wegzetwerk weergegeven dat de gebruiker instrueert de doelnummerplaat op de aanvullingslocatie weg te zetten. De *wegzet* locatie moet **06A01R2S1B** zijn.

1. Bevestig de wegzetgegevens en klik op **OK**.

    U ontvangt het bericht 'Werk voltooid' en de details van de volgende aanvullingsverzameltaak worden weergegeven: het artikelnummer, de hoeveelheid en de locatie waaruit moet worden verzameld. De verzamellocatie is gelijk aan de eerste aanvullingslocatie. Daarom heeft de nummerplaat dezelfde nummerplaat-id die is gebruikt voor de eerste aanvullingswerktaak.

1. Herhaal de vorige stappen om het aanvullingswerk voor de tweede taak te voltooien. De hoeveelheid en de doelnummerplaat verschillen van de hoeveelheid en de doelnummerplaat van de eerste werktaak.

Nadat het tweede aanvullingswerk is voltooid, wordt het bericht 'Werk voltooid' weergegeven. Het mobiele apparaat informeert u ook dat er geen werk beschikbaar is, zelfs als enig aanvullingswerk resteert. Deze werking treedt op omdat het aanvullingswerk de beschikbaarheidsstatus *Geblokkeerd* heeft en daarom is gemarkeerd als **Geblokkeerd**.

De status *Geblokkeerd* is ingeschakeld omdat het locatieprofiel voor de verzamellocatie waaraan het werk wordt toegewezen, een **Overschrijdingshoeveelheid**-waarde van *0,65 PL* heeft. De twee eerdere aanvullingswerktaken hebben de locatie bijna tot op de overschrijdingslimiet gevuld voor artikel *T0100*. (De eenheidsomrekening voor het artikel is *1 PL = 100 stuks*.) Het resterende aanvullingswerk zou daarom de locatie de limiet doen overschrijden.

Dit aanvullingswerk blijft geblokkeerd tot er voldoende voorraad is verzameld vanaf deze locatie om de locatie onder de werkvrijgavedrempel te brengen in de menuopdracht van het mobiele apparaat.

#### <a name="sales-order-pick"></a>Verkooporderverzameling

Voordat de resterende aanvullingswerktaak kan worden voltooid, moet de voorraad op de verzamellocatie worden verminderd tot een niveau waarop het resterende aanvullingswerk kan worden gedeblokkeerd. Met andere woorden, de som van de hoeveelheid voorhanden voorraad op de locatie en de aanvullingshoeveelheid mogen de waarde **Overschrijdingshoeveelheid** niet overschrijden. Wanneer deze som kleiner is dan de overschrijdingshoeveelheid, wordt het resterende aanvullingswerk gedeblokkeerd.

1. Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker in magazijn *61*. (Geef *61* op als gebruikers-id en *1* als wachtwoord.)
1. Ga naar **Uitgaand \> Orderverzamelen**.
1. Voer de eerste werk-id voor verkooporder 1 in.

    Raadpleeg de werk-id's voor verkooporders waarvan u eerder een notitie hebt gemaakt, op de pagina **Werkgegevens**. Met de werk-id die u hier invoert, wordt verzamelwerk voor een hoeveelheid van 10 stuks gegenereerd vanaf twee aparte locaties.

1. Selecteer **OK**.

    De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit voor de eerste locatie moet worden verzameld.

1. Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.
1. Klik op de knop **OK** (vinkjesymbool).

    De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit voor de volgende locatie moet worden verzameld.

1. Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.
1. Klik op de knop **OK** (vinkjesymbool).

    Op de pagina **Verkooporders: wegzetten** wordt aangegeven dat u het voltooide verzamelwerk moet wegzetten op de uitgaande faseringslocatie.

1. Selecteer **OK**.

    U ontvangt de melding Werk voltooid.

1. Voer de tweede werk-id voor verkooporder 1 in.

    Er is slechts één verzameltaak voor deze werk-id.

1. Selecteer **OK**.

    De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit moet worden verzameld.

1. Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.

    De nummerplaat die u opgeeft, is een van de door het systeem gegenereerde nummerplaten uit de aanvullingswerktaken. Als u er zeker van wilt zijn dat u de juiste nummerplaat-id gebruikt, controleert u de voorraad op de pagina **Voorhanden lijst** voor het artikel, de locatie en de hoeveelheid.

1. Klik op de knop **OK** (vinkjesymbool).
1. Bevestig de instructies voor de wegzettaak naar de uitgaande faseringslocatie.
1. Selecteer **OK**.

    U ontvangt de melding Werk voltooid.

Verkooporder 2 is geblokkeerd voor verzamelen omdat de aanvullingstaak waaraan deze is gekoppeld, niet is voltooid. Op dit moment is er nog steeds een hoeveelheid van 30 stuks op de verzamellocatie en is de aanvullingshoeveelheid voor verkooporder 2 60 stuks. De som van de voorhanden voorraad en de aanvullingsvoorraad (90 stuks) overschrijdt de overschrijdingshoeveelheid van 0,65 PL (of 65 stuks). Voordat het aanvullingswerk kan worden voltooid, moet verkooporder 3 worden verzameld.

1. Voer de werk-id voor verkooporder 3 in.

    Er is slechts één verzameltaak voor deze werk-id.

1. Selecteer **OK**.

    De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit moet worden verzameld.

1. Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.

    De nummerplaat die u opgeeft, is een van de door het systeem gegenereerde nummerplaten uit de aanvullingswerktaken. Als u er zeker van wilt zijn dat u de juiste nummerplaat-id gebruikt, controleert u de voorraad op de pagina **Voorhanden lijst** voor het artikel, de locatie en de hoeveelheid.

1. Klik op de knop **OK** (vinkjesymbool).
1. Bevestig de instructies voor de wegzettaak naar de uitgaande faseringslocatie.
1. Selecteer **OK**.

    U ontvangt de melding Werk voltooid.

Zodra de som van de voorhanden hoeveelheid op de verzamellocatie en de aanvullingshoeveelheid lager is dan de drempelwaarde, kunt u het resterende aanvullingswerk verwerken.

Ga terug naar de pagina **Werkgegevens** en u ziet dat de beschikbaarheid van aanvullingswerk voor de laatste aanvulling (voor verkooporder 2) *Open* is, omdat er nu voldoende ruimte op de locatie is om de aanvulling te accepteren.

U kunt dit aanvullingswerk nu uitvoeren via het mobiele apparaat.

1. Ga naar **Voorraad \> Aanvulling**.

    U wordt gevraagd om het resterende aanvullingswerk te voltooien. Het artikelnummer, de hoeveelheid en de locatie waar moet worden verzameld, worden weergegeven.

1. Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.
1. Klik op de knop **OK** (vinkjesymbool).

    Het systeem genereert een nummerplaatnummer voor de nieuwe nummerplaat voor het verzamelde artikel.

1. Selecteer **OK** om de waarde te bevestigen.

    Er wordt wegzetwerk weergegeven dat de gebruiker instrueert de doelnummerplaat op de aanvullingslocatie weg te zetten. De *wegzet* locatie moet **06A01R2S1B** zijn.

1. Bevestig de wegzetgegevens en klik op **OK**.

    U ontvangt berichten over 'Werk voltooid' en 'Geen werk beschikbaar'.

U kunt nu verkooporder 2 verzamelen. Dit werd gedeblokkeerd toen het aanvullingswerk werd voltooid dat is gekoppeld aan de verkooporder.

1. Voer de werk-id voor verkooporder 2 in.

    Er is slechts één verzameltaak voor deze werk-id.

1. Selecteer **OK**.

    De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit moet worden verzameld.

1. Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.

    De nummerplaat die u opgeeft, is de door het systeem gegenereerde nummerplaat uit de aanvullingswerktaak. Als u er zeker van wilt zijn dat u de juiste nummerplaat-id gebruikt, controleert u de voorraad op de pagina **Voorhanden lijst** voor het artikel, de locatie en de hoeveelheid.

1. Klik op de knop **OK** (vinkjesymbool).
1. Bevestig de instructies voor de wegzettaak naar de uitgaande faseringslocatie.
1. Selecteer **OK**.

    U ontvangt de melding Werk voltooid.

## <a name="notes-and-tips"></a>Opmerkingen en tips

- Deze functionaliteit werkt met alle aanvullingstypen: wavevraag, min/max, ladingsvraag en vakken.
- U kunt desgewenst de beschikbaarheid van aanvullingswerk voor elke werkkop handmatig wijzigen vanaf de pagina **Werkgegevens**.
- Wanneer het systeem de beschikbaarheid van aanvullingswerk instelt, houdt het rekening met voorraad die al aanwezig is op de locatie voordat enig werk is voltooid
- Elk verkooporderwerk is gekoppeld aan specifiek aanvullingswerk. Er is geen corresponderende functionaliteit voor beschikbaarheid van verkoopwerk.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]