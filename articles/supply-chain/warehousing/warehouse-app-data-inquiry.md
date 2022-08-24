---
title: Gegevens met de omleidingen van de mobiele app Warehouse Management
description: Dit artikel beschrijft hoe u menuopdrachten voor gegevensaanvragen op mobiele apparaten kunt configureren en gebruiken als onderdeel van omleidingen.
author: perlynne
ms.date: 08/01/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c3ea53379badb3cb2ed71b7f102956d71c3f047a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220536"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Gegevens met de omleidingen van de mobiele app Warehouse Management

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Inleiding functie

Door de mogelijkheid te bieden om streepjescodes te scannen, kunt u met de mobiele app Warehouse Management op een eenvoudige en nauwkeurige manier gegevens vastleggen als onderdeel van magazijnprocessen. Streepjescodes zijn soms echter beschadigd en onleesbaar of de vereiste gegevens zijn mogelijk niet als streepjescode aanwezig in de processtromen van uw bedrijf. In deze gevallen kan handmatige invoer van de gegevens veel tijd in beslag nemen en kunnen er zelfs onjuiste gegevens worden vastgelegd. De resultaten hiervan kunnen een verminderde effectiviteit en een lager serviceniveau zijn.

Door een flexibel proces voor gegevensonderzoek te gebruiken, kunnen werknemers gemakkelijk de vereiste informatie opzoeken als onderdeel van de ingebouwde flows in de mobiele app Management Warehouse en filteropties toepassen zodat alleen de relevante gegevens worden getoond. Handmatige selectie is daardoor sneller en nauwkeuriger.

In de stroom voor inkooporderontvangst is bijvoorbeeld een inkoopordernummer vereist voor overeenkomst met de binnenkomende voorraad. Als onderdeel van dit proces kunt u menuopdrachten eenvoudig configureren om een kaartlijstweergave van de relevante inkoopordernummers te geven. Op deze manier kunt u de ontvangststroom voortzetten door middel van een snelle point-to-select-benadering. In dit artikel worden voorbeeldscenario's beschreven, maar de functionaliteit kan ook worden gebruikt binnen een of alle mobiele app-flows van Warehouse Management.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>De functie voor gegevensonderzoeksstroom inschakelen en de vereisten ervan

Voordat u de functionaliteit kunt gebruiken die in dit artikel wordt beschreven, moet u de volgende procedure uitvoeren om de vereiste functies in te schakelen.

1. Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**. Raadpleeg [Overzicht functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie over het gebruik van de werkruimte **Functiebeheer**.
1. Schakel de functie in die op de volgende manier wordt weergegeven:

    - **Module:** *Warehouse Management*
    - **Functienaam:** *Schakel de stapinstructiesfunctie van de Warehouse-app in*

    Deze functie is een vereiste voor de functie *Gegevensonderzoeksstroom in de app Warehouse Management*. Zie voor meer informatie over de *stapinstructies voor de Warehouse-app* de informatie in [Stappentitels en instructies voor de mobiele app Warehouse Management aanpassen](mobile-app-titles-instructions.md).

1. Schakel de functie in die op de volgende manier wordt weergegeven:

    - **Module:** *Warehouse Management*
    - **Functienaam:** *Omleidingen van app Warehouse Management*

    Deze functie is een vereiste voor de functie *Gegevensonderzoeksstroom in de app Warehouse Management*. Raadpleeg [Omleidingen configureren voor stappen in menuopdrachten van mobiele apparaten](warehouse-app-detours.md) voor meer informatie over de functie *Omleidingen van de app Warehouse management*.

1. Als de functie *Omleidingen van de app Warehouse Management* niet al was ingeschakeld, werk dan de veldnamen in de mobiele app Warehouse Management bij door te gaan naar **Warehouse management \> Instellingen \> Mobiel apparaat \> Veldnamen van Warehouse-app** en **Standaardinstelling aanmaken** te selecteren. Herhaal deze stap voor elke rechtspersoon (bedrijf) waar u de mobiele app Warehouse Management gebruikt. Zie [Velden configureren voor de mobiele app Magazijnbeheer](configure-app-field-names-priorities-warehouse.md) voor meer informatie.
1. Schakel de functie in die op de volgende manier wordt weergegeven:

    - **Module:** *Warehouse Management*
    - **Naam functie:** *Gegevensonderzoeksstroom voor Warehouse management-app*

    Deze functie is de enige functie die in dit artikel wordt beschreven.

## <a name="example-scenarios"></a>Voorbeeldscenario's

In dit artikel worden voorbeeldscenario's gebruikt om aan te geven hoe u de functie *Gegevensonderzoeksstroom voor Warehouse management-app* kunt gebruiken om de ontvangststroom voor inkoop te verbeteren. Voor de scenario's worden de standaard voorbeeldgegevens gebruikt, waaronder een stroom met de naam *Inkoop ontvangen*. Deze stroom begint door werknemers te vragen een inkoopordernummer te identificeren waartegen zij zullen ontvangen. Om werknemers de inkooporder gemakkelijker te laten identificeren, verbetert u de eerste pagina van de stroom door de volgende nieuwe query-opties toe te voegen als [omwegen](warehouse-app-detours.md):

- **Inkooporders opzoeken op leverancier**: open een pagina waarop werknemers wordt gevraagd om een (deel van een) leveranciersnaam in te voeren. Er kunnen jokertekens worden gebruikt. Als een werknemer bijvoorbeeld vandaag een inkomende levering verwacht van een leverancier met *Tailspin* in de naam, dan kan **Tail\*** worden ingevoerd om een reeks kaarten voor openstaande inkooporders weer te geven die deze tekst bevatten. Elke kaart heeft verschillende velden met informatie over elke inkooporder. Naast de naam van de leverancier kunt u de kaarten zo ontwerpen zodat het accountnummer van de leverancier, de leveringsdatum en de documentstatus worden weergeven.
- **Inkooporders voor vandaag opzoeken**: open een pagina waar werknemers niet wordt gevraagd gegevens in te voeren, maar waar vooraf geconfigureerde filters worden getoond (zoals de datum van vandaag). Op de pagina wordt vervolgens een reeks kaarten getoond die met het filter overeenkomen. Werknemers gaan door met het selecteren van een kaart voor de inkooporder waar ze voorraadartikelen op willen registreren.
- **Inkooporders opzoeken op artikel**: open een pagina waarin werknemers wordt gevraagd de streepjescode van een artikel in de binnengekomen voorraad te scannen. De stroom vermeldt vervolgens alle openstaande inkooporders die regels bevatten voor het gescande artikelnummer. Om situaties te dekken waarin een streepjescode niet kan worden gelezen, kunt u nog een zoekopdracht voor omleiding op deze pagina toevoegen zodat de werknemers in een specifieke inkooporder kunnen zoeken op artikelnummer.

In elk geval identificeert de werknemer een inkooporder door een kaart te selecteren en vervolgens terug te keren naar de eerste pagina, die het nummer van de geselecteerde inkooporder toont. De werknemer kan vervolgens de registratiestroom voor inkomende voorraadartikelen voortzetten.

## <a name="enable-sample-data"></a>Voorbeeldgegevens inschakelen

Om de voorbeeldscenario's te doorlopen die in dit artikel worden beschreven, moet u werken op een systeem waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon (het bedrijf) *USMF* selecteren voordat u begint.

## <a name="configure-the-mobile-device-menu-items"></a>De menuopdrachten voor mobiele apparaten configureren

Om elk van de nieuwe query-opties aan te maken die u aan de eerste pagina van de stroom moet toevoegen, moet u deze instellen als een menuopdracht van een mobiel apparaat. Later maakt u de query-opties beschikbaar als omleidingen naar de stroom *Inkoop ontvangen*.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>De menuopdracht 'Inkooporders opzoeken op leverancier' aanmaken

Maak de menuopdracht **Inkooporders opzoeken op leverancier** aan door de volgende stappen uit te voeren.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in het actievenster **Nieuw** om een menuopdracht voor een mobiel apparaat toe te voegen.
1. Stel de volgende waarden in voor de nieuwe menuopdracht:

    - **Naam menuopdracht:** *Inkooporders opzoeken op leverancier*
    - **Titel:** *Inkooporders opzoeken op leverancier*
    - **Modus:** *indirect*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Activiteitencode:** *Gegevensonderzoek*
    - **Proceshandleiding gebruiken:** *Ja* (deze waarde wordt automatisch geselecteerd).
    - **Tabelnaam:** *PurchTable* (u wilt inkoopordernummers op zoeken uit deze tabel).

1. Selecteer in het actievenster **Query bewerken** om een query te definiëren die is gebaseerd op de geselecteerde basistabel (in dit geval de tabel inkooporders).
1. Voeg in de query-editor op het tabblad **Bereik** de volgende regels toe aan het raster:

    | Tabel | Afgeleide tabel | Veld | Criteria |
    |---|---|---|---|
    | Inkooporders | Inkooporders | Status van inkooporder | Openstaande order |
    | Inkooporders | Inkooporders | Leveringsdatum | (dayRange(-10,10)) |
    | Inkooporders | Inkooporders | Naam van leverancier | |

1. Selecteer **OK**.

    In dit voorbeeld is de nieuwe menuopdracht geconfigureerd voor het zoeken naar openstaande inkooporders die naar verwachting op enig moment tussen de afgelopen 10 dagen en 10 dagen in de toekomst zullen binnenkomen.

    In de query is de kolom **Criteria** voor *Naam leverancier* leeg gelaten. Werknemers kunnen deze waarde dus opgeven terwijl ze de mobiele app Warehouse management gebruiken.

    Als u wilt opgeven hoe de lijst wordt gesorteerd, kunt u de sortering instellen op het tabblad **Sorteren**.

1. Naast het definiëren van de query, moet u ook selecteren welke velden worden getoond op de kaarten op de querylijstpagina. Selecteer daarvoor **Veldenlijst** in het actievenster.
1. Stel op de pagina **Veldenlijst** de volgende waarden in:

    - **Weergaveveld 1:** *PurchId* (dit veld wordt weergegeven als header voor elke kaart).
    - **Weergaveveld 2:** *PurchStatus*
    - **Weergaveveld 3:** *PurchName*
    - **Weergaveveld 4:** *OrderAccount*
    - **Weergaveveld 5:** *DeliveryDate*
    - **Weergaveveld 6:** *displaydocumentStatus()* (deze waarde is een weergavemethode, zoals de '()' aan het einde aangeeft).

1. Selecteer **Opslaan** in het actievenster. Sluit de pagina vervolgens.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>De menuopdracht 'Inkooporders opzoeken voor vandaag' aanmaken

Maak de menuopdracht **Inkooporders opzoeken voor vandaag** aan door de volgende stappen uit te voeren.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in het actievenster **Nieuw** om een menuopdracht voor een mobiel apparaat toe te voegen.
1. Stel de volgende waarden in voor het nieuwe artikel:

    - **Naam menuopdracht:** *Inkooporders opzoeken voor vandaag*
    - **Titel:** *Inkooporders opzoeken voor vandaag*
    - **Modus:** *indirect*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Activiteitencode:** *Gegevensonderzoek*
    - **Proceshandleiding gebruiken:** *Ja* (deze waarde wordt automatisch geselecteerd).
    - **Tabelnaam:** *PurchTable* (u wilt inkoopordernummers op zoeken uit deze tabel).

1. Selecteer in het actievenster **Query bewerken** om een query te definiëren die is gebaseerd op de geselecteerde basistabel (in dit geval de tabel inkooporders).
1. Voeg in de query-editor op het tabblad **Bereik** de volgende regels toe aan het raster:

    | Tabel | Afgeleide tabel | Veld | Criteria |
    |---|---|---|---|
    | Inkooporder | Inkooporder | Status van inkooporder | Openstaande order |
    | Inkooporder | Inkooporder | Leveringsdatum | (Day(0)) |

1. Selecteer **OK**.

    In dit voorbeeld is de nieuwe menuopdracht geconfigureerd voor het zoeken naar openstaande inkooporders die naar verwachting vandaag zullen binnenkomen.

    Als u wilt opgeven hoe de lijst wordt gesorteerd, kunt u de sortering instellen op het tabblad **Sorteren**.

1. Naast het definiëren van de query, moet u ook selecteren welke velden worden getoond op de kaarten op de querylijstpagina. Selecteer daarvoor **Veldenlijst** in het actievenster.
1. Stel op de pagina **Veldenlijst** de volgende waarden in:

    - **Weergaveveld 1:** *PurchName* (dit veld wordt weergegeven als header voor elke kaart).
    - **Weergaveveld 2:** *PurchId*
    - **Weergaveveld 3:** *PurchStatus*
    - **Weergaveveld 4:** *DlvMode*
    - **Weergaveveld 5:** *DlvTerm*
    - **Weergaveveld 6:** *OrderAccount*
    - **Weergaveveld 7:** *VendorName()* (deze waarde is een weergavemethode, zoals de '()' aan het einde aangeeft).

1. Selecteer **Opslaan** in het actievenster. Sluit de pagina vervolgens.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>De menuopdracht 'Inkooporders opzoeken op artikel' aanmaken

Maak de menuopdracht **Inkooporders opzoeken op artikel** aan door de volgende stappen uit te voeren.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in het actievenster **Nieuw** om een menuopdracht voor een mobiel apparaat toe te voegen.
1. Stel de volgende waarden in voor het nieuwe artikel:

    - **Naam menuopdracht:** *Inkooporders opzoeken op artikel*
    - **Titel:** *Inkooporders opzoeken op artikel*
    - **Modus:** *indirect*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Activiteitencode:** *Gegevensonderzoek*
    - **Proceshandleiding gebruiken:** *Ja* (deze waarde wordt automatisch geselecteerd).
    - **Tabelnaam:** *PurchLine* (u wilt inkoopordernummers op zoeken op basis van artikelnummer via de regelgegevens).

1. Selecteer in het actievenster **Query bewerken** om een query te definiëren die is gebaseerd op de geselecteerde basistabel (in dit geval de tabel met inkooporderregels, maar u kunt alle waarden gebruiken die aan de header zijn gerelateerd door een verbinding te leggen met de *PurchTable*).
1. Voeg in de query-editor op het tabblad **Bereik** de volgende regels toe aan het raster:

    | Tabel | Afgeleide tabel | Veld | Criteria |
    |---|---|---|---|
    | Inkooporderregels | Inkooporderregels | Regelstatus | Openstaande order |
    | Inkooporderregels | Inkooporderregels | Leveringsdatum | (dayRange(-10,10)) |
    | Inkooporderregels | Inkooporderregels | Artikelnummer | |

1. Selecteer **OK**.

    In dit voorbeeld is de nieuwe menuopdracht geconfigureerd voor het zoeken naar openstaande inkooporderregels die naar verwachting op enig moment tussen de afgelopen 10 dagen en 10 dagen in de toekomst zullen binnenkomen.

    In de query is de kolom **Criteria** voor *Artikelnummer* leeg gelaten. Werknemers kunnen deze waarde dus opgeven terwijl ze de mobiele app Warehouse management gebruiken.

    Als u wilt opgeven hoe de lijst wordt gesorteerd, kunt u de sortering instellen op het tabblad **Sorteren**.

1. Naast het definiëren van de query, moet u ook selecteren welke velden worden getoond op de kaarten op de querylijstpagina. Selecteer daarvoor **Veldenlijst** in het actievenster.
1. Stel op de pagina **Veldenlijst** de volgende waarden in:

    - **Weergaveveld 1:** *PurchId* (de waarde van dit veld wordt gebruikt als header voor elke kaart).
    - **Weergaveveld 2:** *VendAccount*
    - **Weergaveveld 3:** *PurchQty*
    - **Weergaveveld 4:** *PurchUnit*
    - **Weergaveveld 5:** *PurchStatus*

1. Selecteer **Opslaan** in het actievenster. Sluit de pagina vervolgens.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>De nieuwe menuopdrachten voor mobiele apparaten toevoegen aan een menu

Uw drie nieuwe menuopdrachten voor mobiele apparaten zijn nu klaar om te worden toegevoegd aan het menu voor mobiele apparaten. Deze taak moet worden voltooid voordat de menuopdrachten kunnen worden gebruikt als onderdeel van een omleidingsproces. In dit voorbeeld maakt u een nieuw submenu en voegt u de nieuwe menuopdrachten hieraan toe.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst van de nieuwe record de volgende waarden in:

    - **Naam:** *Opvragen*
    - **Beschrijving:** *Opvragen*

1. Selecteer in de lijst **Beschikbare menu's en menuopdrachten** de eerste van de net aangemaakte menuopdrachten voor mobiele apparaten. Selecteer vervolgens de knop pijl-rechts om die opdracht te verplaatsen naar de lijst **Menustructuur**.
1. Herhaal de vorige stap voor de andere twee nieuwe menuopdrachten.
1. Selecteer in het lijstvenster aan de linkerkant het **Hoofd** menu.
1. Blader in de lijst **Beschikbare menu's en menuopdrachten** naar beneden naar het gedeelte **Menu's** en selecteer het nieuwe menu **Opvragen**. Selecteer vervolgens de knop pijl-rechts om die opdracht te verplaatsen naar de lijst **Menustructuur**.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Omleidingen configureren in uw stappen voor mobiele apparaten

Om de instelling te voltooien, moet u nu de omleidingsconfiguratie gebruiken op de pagina **Stappen voor mobiele apparaten** om de drie nieuwe menuopdrachten van het mobiele apparaat toe te voegen aan de bestaande identificatiestap voor de inkooporder in de stroom *Inkoop ontvangen*.

1. Ga naar **Warehouse management \> Instellen > Mobiel apparaat \> Stappen voor mobiele apparaten**
1. Voer in het veld **Filter** de tekst *PONum* in. Selecteer vervolgens in de vervolgkeuzelijst *Stap ID: 'PONum'*.
1. Selecteer, terwijl de record die wordt gevonden, wordt geselecteerd in het raster, in het actievenster **Stapconfiguratie toevoegen**. Zet in de vervolgkeuzelijst in het dialoogvenster dat verschijnt het veld **Menuopdracht** op *Inkoop ontvangen*. Selecteer vervolgens **OK** om het dialoogvenster te sluiten.
1. Selecteer op de pagina met gegevens voor de nieuwe stapconfiguratie (**Inkoop ontvangen: PONum**); selecteer op het sneltabblad **Beschikbare omleidingen (menuopdrachten)** de optie **Toevoegen** op de werkbalk.
1. Zoek in het dialoogvenster **Omleiding toevoegen** de eerder aangemaakte menuopdracht **Inkooporders opzoeken op leverancier** op en selecteer deze.
1. Selecteer **OK** om het dialoogvenster te sluiten en de geselecteerde menuopdracht toe te voegen aan de lijst met omleidingen.
1. Selecteer de nieuwe omleiding en daarna **Te verzenden velden selecteren** op de werkbalk.
1. Voeg in het dialoogvenster **Te verzenden velden selecteren** niets toe aan het gedeelte **Verzenden vanuit inkoop ontvangen** omdat u geen waarden wilt doorgeven aan de menuopdracht van de omleiding. Stel echter in het gedeelte **Terughalen uit inkooporders opzoeken op leverancier** de volgende waarde in voor de lege rij die daar al is toegevoegd:

    - **Kopieer vanuit inkooporders opzoeken op leverancier:** *inkooporder*
    - **Plak in Inkoop ontvangen:** *Inkooporder*

1. Selecteer **OK** om het dialoogvenster te sluiten.
1. Herhaal stap 4 tot en met 9 voor de andere twee nieuwe menuopdrachten (**Inkooporders opzoeken voor vandaag** en **Inkooporders opzoeken op artikel**). Voor de menuopdracht **Inkooporders opzoeken op leverancier** geldt dat u geen gegevens naar deze omleidingen wilt verzenden, maar een inkoopordernummer wilt retourneren.
1. Sluit de pagina.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Probeer een stroom voor inkoop ontvangen met een gegevensonderzoek als onderdeel van een omleiding

Volg deze stappen om de nieuwe instellingen voor de mobiele app te testen.

1. Maak meerdere inkooporders aan met regels voor magazijn 51.
1. Ga naar een mobiel apparaat of emulator waarin de mobiele app Magazijnbeheer wordt uitgevoerd en meld u aan bij magazijn 51 met *51* als gebruikers-id en *1* als wachtwoord.
1. Selecteer in het menu van de mobiele app **Inkomend** en vervolgens **Inkoop ontvangen**.

    De volgende pagina, met daarop de drie nieuwe menuopdrachten, moet nu zichtbaar worden.

    ![Inkoop ontvangen met behulp van inkoopordernummer](media/wma-purchase-receive-po-num-with-detours.png "Inkoop ontvangen met behulp van inkoopordernummer")

1. Probeer de verschillende mogelijkheden uit en merk op dat u een inkoopordernummer kunt terugsturen door een van de kaarten in de lijst te selecteren.

    ![Inkoop ontvangen met behulp van inkooporders opzoeken op leverancier, voorbeeld 1](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Inkoop ontvangen met behulp van inkooporders opzoeken op leverancier, voorbeeld 1")

    ![Inkoop ontvangen met behulp van inkooporders opzoeken op leverancier, voorbeeld 2](media/wma-purchase-receive-lookup-po-vendor-detours.png "Inkoop ontvangen met behulp van inkooporders opzoeken op leverancier, voorbeeld 2")

> [!TIP]
> In plaats van de ontvangststroom uit te voeren door een zoekactie uit te voeren via de menuopdracht **Inkoop ontvangen**, kunt u vanuit een onderzoeksstroom starten (**Hoofd \> Onderzoeken \> Inkooporders opzoeken op leverancier**) en een omleiding op te roepen om de gewenste stroom uit te voeren door een van de kaarten in de lijst te selecteren. Als u deze benadering wilt gebruiken, kunt u een omleiding definiëren op de pagina **Stappen mobiel apparaat** voor de stap met een **stap-ID-waarde** van *GenericDataInquiryList*. Omdat deze stroom een omleidingsstroom is, kunt u vanuit deze stroom niet meer omleidingen aanroepen. Wanneer u bijvoorbeeld bij het invoerscherm voor artikelnummer komt, is de opzoekactie niet beschikbaar omdat het systeem momenteel slechts één omleidingsniveau ondersteunt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
