---
title: Containerverpakkingsstrategieën
description: In dit onderwerp worden de verschillen tussen containerverpakkingsstrategieën beschreven en voorbeelden gegeven.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4e5faf8e4544b2bcb58f3c578789b2bd379a27b0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572356"
---
# <a name="container-packing-strategies"></a>Containerverpakkingsstrategieën

[!include [banner](../includes/banner.md)]

Een *containerverpakkingsstrategie* is een strategie die u kunt gebruiken om toewijzingen van artikelen over containers te definiëren. In dit onderwerp worden de verschillen tussen de strategieën *Verpakken in alle open containers* en *Alleen in huidige container verpakken* uitgelegd.

- **Verpakken in alle open containers**: het systeem moet alle geopende containers controleren die al tijdens de containervormingscyclus zijn gemaakt, om ervoor te zorgen dat het artikel in een van deze containers past. Tijdens het verpakken wordt elk artikel gecontroleerd om te bepalen of het artikel in een van de eerder gemaakte containers past. Als het artikel niet in een bestaande container past, wordt een nieuwe container gemaakt en gaat het systeem verder totdat de gehele order is verpakt.

    Containervorming is nodig voor bijvoorbeeld *n* bestelde artikelen. In het ergste geval worden, telkens als het systeem een artikel verwerkt dat niet in een bestaande container past, in totaal (\[(*n* – 1) × (*n* + 1)\] ÷ 2) controles uitgevoerd om na te gaan of het artikel in de bestaande containers past.

- **Alleen in huidige container verpakken**: het systeem moet alleen de meest recent gemaakte container controleren om te zien of het artikel erin past. Tijdens het verpakken wordt elk artikel gecontroleerd om te bepalen of het artikel in de meest recent gemaakte container past. Als het artikel niet in die container past, wordt een nieuwe container gemaakt en gaat het verder totdat de gehele order is verpakt.

    Containervorming is nodig voor bijvoorbeeld *n* bestelde artikelen. In het ergste geval voert het systeem in totaal (*n* – 1) controles uit om te beoordelen of het artikel in de containers past.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Voorbeeld van de stroom voor containerverpakkingsstrategieën

U stelt de volgende artikelen in voor containervorming:

| Artikel | Fysieke dimensies (breedte × diepte × hoogte) | Gewicht |
|---|---|---|
| HDMI 6' kabel | 1 × 1 × 1 | 1 |
| HDMI 12' kabel | 2 × 1 × 1 | 1 |
| HDMI 18' kabel | 3 × 1 × 1 | 2 |

U stelt ook de volgende doos in die voor het inpakken wordt gebruikt.

| Container | Fysieke dimensies (lengte × breedte × hoogte) | Gewicht | Volume |
|---|---|---|---|
| Middelgrote doos | 6 × 3 × 2 | 10 | 100 |

Tot slot kunt u een order instellen met de volgende producten en hoeveelheden.

| Verkooporderregel | Hoeveelheid |
|---|---|
| HDMI 12' kabel | 9 |
| HDMI 18' kabel | 8 |
| HDMI 6' kabel | 13 |

De volgende tabel biedt een overzicht van hoe containervorming werkt wanneer u de strategie *Verpakken in alle open containers* gebruikt en wanneer u de strategie *Alleen in huidige container verpakken* gebruikt.

| Inpakken in alle open containers | In de huidige container verpakken |
|---|---|
| <p>HDMI 12' kabel:</p><ol><li>Maak een nieuwe container, CONT0001.</li><li>Doe 9 losse eenheden in container CONT0001.</li></ol> | <p>HDMI 12' kabel:</p><ol><li>Maak een nieuwe container, CONT0001.</li><li>Doe 9 losse eenheden in container CONT0001.</li></ol> |
| <p>HDMI 18' kabel:</p><ol><li>Controleer of het artikel in container CONT0001 zou passen.</li><li>Maak een nieuwe container, CONT0002.</li><li>Doe 5 losse eenheden in container CONT0002.</li><li>Maak een nieuwe container, CONT0003.</li><li>Doe 3 losse eenheden in container CONT0003.</li></ol> | <p>HDMI 18' kabel:</p><ol><li>Controleer of het artikel in container CONT0001 zou passen.</li><li>Maak een nieuwe container, CONT0002.</li><li>Doe 5 losse eenheden in container CONT0002.</li><li>Maak een nieuwe container, CONT0003.</li><li>Doe 3 losse eenheden in container CONT0003.</li></ol> |
| <p>HDMI 6' kabel:</p><ol><li>Controleer of het artikel in container CONT0001 zou passen.</li><li>Doe 1 losse eenheid in container CONT0001.</li><li>Controleer of het artikel in container CONT0002 zou passen.</li><li>Controleer of het artikel in container CONT0003 zou passen.</li><li>Doe 4 losse eenheden in container CONT0003.</li><li>Maak een nieuwe container, CONT0004.</li><li>Doe 8 losse eenheden in container CONT0004.</li></ol> | <p>HDMI 6' kabel:</p><ol><li>Controleer of het artikel in container CONT0003 zou passen.</li><li>Doe 4 losse eenheden in container CONT0003.</li><li>Maak een nieuwe container, CONT0004.</li><li>Doe 9 losse eenheden in container CONT0004.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Voorbeeldscenario: afzonderlijke orders per container verpakken

Deze sectie bevat een scenario waarin het systeem is ingesteld om meerdere orders in één zending te consolideren. Er vindt dus containervorming plaats vanuit de verkooporder om ervoor te zorgen dat elke order met meerdere producten in een eigen container wordt verpakt.

Met deze functionaliteit kunt u scenario's verwerken waarbij u slechts één verkooporder in elke container moet verpakken, zodat het distributiecentrum volle containers tussen detailhandels kan cross-docken. Behalve de detailhandelscenario's (order per detailhandel en verzending naar een distributiecentrum voor cross-docken) wordt deze techniek ook vaak gebruikt in lean toeleveringsketens (verkooporder per just-in-time productieregel).

In dit scenario kunt u zien hoe u het aantal containers kunt verminderen dat tijdens het verpakken wordt gecontroleerd als u de strategie *Alleen in huidige container verpakken* gebruikt voor containervorming.

### <a name="prerequisites"></a>Vereisten

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>De functie Verzendingen consolideren in uw systeem inschakelen

In dit scenario wordt de functie *Verzendingen consolideren* gebruikt. Als de functie niet al beschikbaar is in uw systeem, moet u deze via [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) inschakelen.

#### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Dit scenario verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd. Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.

### <a name="inspect-or-create-container-types"></a>Containertypen controleren of maken

Volg de volgende stappen om uw containertypen te controleren of om zo nodig nieuwe containertypen te maken.

1. Ga naar **Magazijnbeheer** \> **Instellingen** \> **Containers** \> **Containertypen**.
1. Zorg ervoor dat elk van de volgende containertypen beschikbaar is in de demogegevens. Bewerk of maak zo nodig containertypen.

    - Containertype 1:

        - **Containertypecode:** *Doos-groot*
        - **Omschrijving:** *Grote doos*
        - **Maximaal nettogewicht:** *100*
        - **Volume:** *400*
        - **Lengte:** *4*
        - **Breedte:** *10*
        - **Hoogte:** *10*

    - Containertype 2:

        - **Containertypecode:** *Doos-middel*
        - **Omschrijving:** *Middelgrote doos*
        - **Maximaal nettogewicht:** *50*
        - **Volume:** *200*
        - **Lengte:** *2*
        - **Breedte:** *10*
        - **Hoogte:** *10*

    - Containertype 3:

        - **Containertypecode:** *Doos-klein*
        - **Omschrijving:** *Kleine doos*
        - **Maximaal nettogewicht:** *20*
        - **Volume:** *100*
        - **Lengte:** *1*
        - **Breedte:** *10*
        - **Hoogte:** *10*

### <a name="inspect-or-create-container-groups"></a>Containergroepen controleren of maken

Volg de volgende stappen om uw containergroepen te controleren of om zo nodig nieuwe containergroepen te maken.

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Containers** \> **Containergroepen**.
1. Zorg ervoor dat de volgende containergroep beschikbaar is in de demogegevens. Als de groep niet beschikbaar is, selecteert u **Nieuw** om deze te maken.

    - **Containergroep-id:** *Dozen*
    - **Omschrijving:** *Doosgrootten*

1. Zorg ervoor dat de volgende regels bestaan op het sneltabblad **Details** voor de containergroep *Dozen*. Als dat niet zo is, selecteert u **Nieuw** om ze toe te voegen.

    - Regel 1:

        - **Volgnummer:** *1*
        - **Containertype:** *doos-groot*
        - **Containergebruikspercentage:** *100*

    - Regel 2:

        - **Volgnummer:** *2*
        - **Containertype:** *Doos-middel*
        - **Containergebruikspercentage:** *100*

    - Regel 3:

        - **Volgnummer:** *3*
        - **Containertype:** *Doos-klein*
        - **Containergebruikspercentage:** *100*

### <a name="create-a-new-container-build-template"></a>Een nieuwe containervormingssjabloon maken

Ga als volgt te werk om een nieuwe containervormingssjabloon te maken.

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Containers** \> **Containervormingssjablonen**.
1. Selecteer **Nieuw** om een containervormingssjabloon te maken met de volgende instellingen:

    - **Volgnummer:** *1*
    - **Containersjabloon-id:** *Doos*
    - **Containergroep-id:** *Dozen*
    - **Basisquerytypen:** *Verkooptoewijzingsregel*
    - **Stapcode wave:** *234*
    - **Gesplitst verzamelen toestaan:** *Ja*
    - **Containerverpakkingsstrategie:** *Alleen in huidige container verpakken*
    - **Verpakken per instructie-eenheid:** *Nee*

1. Selecteer, terwijl de nieuwe rij voor de nieuwe sjabloon nog steeds is geselecteerd, de optie **Query bewerken** in het actievenster.
1. Er wordt een standaarddialoogvenster voor Query-editor weergegeven. Selecteer op het tabblad **Sorteren** de optie **Toevoegen** om een rij met de volgende instellingen toe te voegen:

    - **Tabel:** *Tijdelijke werktransacties*
    - **Afgeleide tabel:** *Tijdelijke werktransacties*
    - **Veld:** *Ordernummer*
    - **Zoekrichting:** *Oplopend*

    > [!IMPORTANT]
    > Als u niet alle andere geopende containers wilt controleren en het proces wilt versnellen door één container tegelijk te controleren, moet u de strategie *Alleen in huidige container verpakken* gebruiken naast het sorteren op ordernummer. Deze combinatie werkt als een werkopsplitsing in een werksjabloon.

1. Selecteer **OK** om het dialoogvenster Query-editor te sluiten.
1. Selecteer, terwijl de nieuwe rij voor de nieuwe sjabloon nog steeds is geselecteerd, de optie **Beperkingen op mengen containers** in het actievenster.

    U voegt nu een beperking toe, zodat artikelen van één order in één container worden geplaatst. Artikelen uit een andere order worden in een aparte container geplaatst.

1. Selecteer **Nieuw** om een mengbeperking te maken met de volgende instellingen:

    - **Tabel:** *Verkooporders*
    - **Veld selecteren:** *SalesId* (Het veld wordt in het raster weergegeven als *Verkooporder*.)

1. Selecteer **OK** om de beperking toe te voegen.
1. Sluit de pagina.

### <a name="set-up-a-wave-template-for-containerization"></a>Een wavesjabloon instellen voor containervorming

Ga als volgt te werk om een wavesjabloon in te stellen.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Stel in het lijstvenster het veld **Type wavesjabloon** in op *Verzenden*.
1. Selecteer de slabloon **63 Containervorming** in de lijst.
1. Selecteer **Bewerken** in het actievenster.
1. Zoek op het sneltabblad **Methoden** in de kolom **Geselecteerde methoden** naar de volgende regel:

    - **Methodenaam:** *containervorming*
    - **Naam:** *Containervorming*

1. Stel het veld **Stapcode wave** voor de regel in op *234*.

### <a name="set-up-a-work-template"></a>Een werksjabloon instellen

Ga als volgt te werk om een werksjabloon in te stellen.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Stel het veld **Werkordertype** in op *Verkooporders*.
1. Zoek en selecteer in het raster **Overzicht** de werksjabloon die moet worden gebruikt om afzonderlijke orders per container te verpakken. Selecteer voor dit scenario de sjabloon **63 Verzameling naar container**.
1. Selecteer **Query bewerken** in het actievenster.
1. Er wordt een standaarddialoogvenster voor Query-editor weergegeven. Voeg de volgende regels toe op het tabblad **Sorteren**:

    - Regel 1:

        - **Tabel:** *Tijdelijke werktransacties*
        - **Afgeleide tabel:** *Tijdelijke werktransacties*
        - **Veld:** *Zending-id*
        - **Zoekrichting:** *Oplopend*

    - Regel 2:

        - **Tabel:** *Tijdelijke werktransacties*
        - **Afgeleide tabel:** *Tijdelijke werktransacties*
        - **Veld:** *Ordernummer*
        - **Zoekrichting:** *Oplopend*

    - Regel 3:

        - **Tabel:** *Tijdelijke werktransacties*
        - **Afgeleide tabel:** *Tijdelijke werktransacties*
        - **Veld:** *Container-id*
        - **Zoekrichting:** *Oplopend*

1. Selecteer **OK** om het dialoogvenster Query-editor te sluiten.
1. Het volgende bericht wordt weergegeven: 'Groeperen wordt opnieuw ingesteld, doorgaan?' Selecteer **Ja** om door te gaan.
1. Terwijl de sjabloon **63 Verzameling naar container** nog steeds is geselecteerd, selecteert u **Opsplitsingen voor werkkoptekst** in het actievenster.

    U moet nu instellingen toepassen om het werk op te splitsen zodat elke container in de order aan één werkorder wordt gekoppeld.

1. Schakel het selectievakje **Groeperen op dit veld** in voor elke rij op de pagina **Opsplitsingen voor werkkoptekst** (**Zending-id**, **Ordernummer** en **Container-id**).
1. Sluit de pagina.

### <a name="set-up-shipment-consolidation-policies"></a>Beleidsregels voor consolidatie van zendingen instellen

Voer de volgende stappen uit om een beleid voor consolidatie van zendingen in te stellen.

1. Ga naar **Magazijnbeheer \> Instellen \> Vrijgave naar magazijn \> Consolidatiebeleid voor zendingen**.
1. Stel in het lijstvenster het veld **Beleidstype** in op *Verkooporders*.
1. Selecteer het beleid **Standaard** in de lijst.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer op het sneltabblad **Consolidatievelden** in de lijst **Geselecteerde velden** de rij waarin het veld **Veldnaam** is ingesteld op *Ordernummer*.
1. Selecteer de knop **Verwijderen** ![linkerpijl.](media/backward-button.png) om het veld naar de lijst **Resterende velden** te verplaatsen.
1. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-physical-dimensions-for-the-product"></a>Fysieke dimensies voor het product instellen

Volg deze stappen om fysieke dimensies in te stellen voor de producten die in dit scenario worden gebruikt.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer het product waarvan het veld **Artikelnummer** is ingesteld op *A0001*.
1. Selecteer in het actievenster op het tabblad **Voorraad beheren** in de groep **Magazijn** de optie **Fysieke afmetingen**.
1. Op de pagina **Fysieke dimensies** ziet u de volgende regel in het raster:

    - **Eenheid:** *st.*
    - **Brutogewicht:** *3,00*
    - **Breedte:** *2,00*
    - **Diepte:** *2,00*
    - **Hoogte:** *4,00*
    - **Volume:** *16,00*

1. Sluit de pagina.
1. Selecteer het product waarvan het veld **Artikelnummer** is ingesteld op *A0002*.
1. Selecteer in het actievenster op het tabblad **Voorraad beheren** in de groep **Magazijn** de optie **Fysieke afmetingen**.
1. Op de pagina **Fysieke dimensies** ziet u de volgende regel in het raster:

    - **Eenheid:** *st.*
    - **Brutogewicht:** *4,00*
    - **Breedte:** *3,00*
    - **Diepte:** *1,00*
    - **Hoogte:** *3,00*
    - **Volume:** *9,00*

### <a name="create-sales-order-1"></a>Verkooporder 1 maken

Volg de onderstaande stappen om een verkooporder te maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Er verschijnt een dialoogvenster voor het maken van een nieuwe verkooporder. Stel de volgende waarden in:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *63*

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Voeg op het sneltabblad **Verkooporderregels** de volgende verkoopregels toe:

    - Regel 1:

        - **Artikelnummer:** *A0001*
        - **Hoeveelheid:** *2*

    - Regel 2:

        - **Artikelnummer:** *A0002*
        - **Hoeveelheid:** *2*

1. Selecteer de eerste regel en selecteer vervolgens **Voorraad \> Reservering**.
1. Selecteer op de pagina **Reservering** **Partij reserveren**. Sluit de pagina vervolgens.
1. Herhaal de vorige twee stappen voor de tweede regel.
1. Sluit de pagina.

### <a name="create-sales-order-2"></a>Verkooporder 2 maken

Voer de volgende stappen uit om een tweede verkooporder te maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Er verschijnt een dialoogvenster voor het maken van een nieuwe verkooporder. Stel de volgende waarden in:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *63*

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Voeg op het sneltabblad **Verkooporderregels** de volgende verkoopregels toe:

    - Regel 1:

        - **Artikelnummer:** *A0001*
        - **Hoeveelheid:** *4*

    - Regel 2:

        - **Artikelnummer:** *A0002*
        - **Hoeveelheid:** *4*

1. Selecteer de eerste regel en selecteer vervolgens **Voorraad \> Reservering**.
1. Selecteer op de pagina **Reservering** **Partij reserveren**. Sluit de pagina vervolgens.
1. Herhaal de vorige twee stappen voor de tweede regel.
1. Sluit de pagina.

### <a name="create-the-load"></a>De lading maken

Voer de volgende stappen uit om een lading te maken voor elke order die u voor dit scenario hebt gemaakt en geef deze vervolgens vrij naar het magazijn.

1. Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.
1. Op het tabblad **Verkoopregels** zoekt en selecteert u alle verkooporderregels uit de verkooporders die u voor dit scenario hebt gemaakt.
1. Selecteer in het actievenster op het tabblad **Vraag en aanbod** in de groep **Toevoegen** de optie **Aan nieuwe lading**. De geselecteerde orderregels worden aan een nieuwe lading toegevoegd.
1. Selecteer in het dialoogvenster **Ladingsjabloon toewijzen** in het veld **Ladingsjabloon-id** een ladingsjabloon, zoals *40' Container*.
1. Selecteer **OK** om het dialoogvenster te sluiten.
1. In de sectie **Ladingen** zoekt en selecteert u de lading die u net hebt gemaakt.
1. Selecteer **Vrijgeven \> Vrijgeven aan magazijn**.
1. Selecteer **OK** in het dialoogvenster **Vrijgeven aan magazijn** om de geselecteerde lading vrij te geven aan het magazijn.

### <a name="verify-the-shipments-and-containers"></a>De zendingen en containers controleren

Met de volgende procedure kunt u de gemaakte zendingen controleren. Gebruik dit om de order te controleren die u voor dit scenario hebt gemaakt zodat u er zeker van bent dat u de verwachte resultaten hebt verkregen.

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.
1. Zoek en selecteer de zending die is gemaakt voor de lading die u zojuist hebt vrijgegeven.
1. Selecteer op het tabblad **Transport** in het actievenster de optie **Containers weergeven**.
1. Bevestig dat de artikelen van de verkooporders door middel van containervorming in twee verschillende containers zijn ondergebracht.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Containervorming](wave-containerization.md)
