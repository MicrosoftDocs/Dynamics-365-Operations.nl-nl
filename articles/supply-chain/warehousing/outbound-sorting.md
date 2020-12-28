---
title: Uitgaand sorteren
description: Dit onderwerp biedt informatie over uitgaand sorteren. Deze functionaliteit vereenvoudigt het verwerken van kleine containers en helpt magazijnmedewerkers de palletcapaciteit in de vrachtwagen beter te plannen en te organiseren.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 84c4ec83ed16762e6c3c1a22425cf60e5b3ae8da
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425863"
---
# <a name="outbound-sorting"></a>Uitgaand sorteren

[!include [banner](../includes/banner.md)]

Deze functionaliteit vereenvoudigt het verwerken van kleine containers en helpt magazijnmedewerkers de palletcapaciteit in de vrachtwagen beter te plannen en te organiseren. Wanneer u uitgaand sorteren gebruikt, kunt u verpakte containers naar de juiste pallet sorteren nadat deze op een inpakstation zijn geweest. U kunt ook een inpakhiërarchie maken.

Met deze functie kunt u pallets maken vanuit containers die zijn verpakt via de inpakfunctionaliteit. De container wordt niet naar de uiteindelijke verzendlocatie verzonden, omdat deze zich in de oorspronkelijke inpakstroom bevindt. In plaats daarvan kunnen werknemers de container sluiten en verplaatsen naar een locatie van het sorteertype. Ze kunnen vervolgens containers sorteren op posities die elk een nummerplaat (LP) hebben. Nadat de containers zijn gesorteerd, kunt u werk maken om de gehele LP te verzenden naar de uiteindelijke verzend- of faseringslocaties, op basis van locatierichtlijnen of uw eigen vereisten. Bovendien kan de actie van het afsluiten van de sorteerpositie de voorraad onmiddellijk naar de uiteindelijke verzendlocatie verplaatsen en de order verzamelen.

## <a name="turn-on-the-outbound-sorting-feature"></a>De functie voor uitgaande sortering inschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Uitgaande sortering*

## <a name="setup"></a>Instellen

Voor dit scenario moet u standaard **USMF**-demogegevens en magazijn *62* gebruiken. U moet ook de instellingen voltooien die in de volgende subsecties worden beschreven.

### <a name="set-up-a-wave-template"></a>Een wavesjabloon instellen

Met deze instellingen wordt de wave automatisch verwerkt en wordt werk gemaakt wanneer een regel aan het magazijn wordt vrijgegeven.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Selecteer **Magazijn 62** in de lijst met sjablonen.
1. Controleer op het sneltabblad **Algemeen** of de optie **Wave verwerken bij vrijgave door magazijn** is ingesteld op *Ja*.

### <a name="set-up-a-worker"></a>Een werknemer instellen

Het inpakstation wordt gezien als een locatie. Magazijnmedewerkers die zich aanmelden bij het inpakstation zien en werken aan alleen verzendingen en containers die op die specifieke inpaklocatie zijn gepland. Een gebruiker die zich aanmeldt bij Microsoft Dynamics 365, moet als werknemer zijn ingesteld in Magazijnbeheer. Als de naam van de gebruiker niet wordt weergegeven in de lijst met werknemers, gebruikt u de volgende procedure om ze toe te voegen.

> [!NOTE]
> Bij deze stappen wordt ervan uitgegaan dat de gebruiker al bestaat in het systeem en is gekoppeld als een werknemer of medewerker in de module **Human Resources**.

1. Ga naar **Magazijnbeheer \> Instellen \> Medewerker**.
1. Selecteer **Nieuw**.
1. Selecteer in het veld **Medewerker** de doelgebruiker in de lijst met werknemers.
1. Selecteer **Selecteren**.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het sneltabblad **Gebruikers** de optie **Nieuw** om een account voor een mobiel apparaat te maken en stel hiervoor de volgende waarden in:

    - **Gebruikers-id:** voer een unieke id in.
    - **Gebruikersnaam:** voer een naam in voor de id.
    - **Standaardmagazijn:** *62*
    - **Menunaam:** *Hoofd*

1. Selecteer **Opslaan** in het actievenster.
1. Het dialoogvenster **Wachtwoord instellen** wordt weergegeven. Maak een eenvoudig wachtwoord dat de gebruiker kan gebruiken om zich aan te melden bij de mobiele app. Stel de volgende waarden in:

    - **Wachtwoord:** geef een eenvoudig wachtwoord op.
    - **Wachtwoord bevestigen:** voer nogmaals hetzelfde wachtwoord in.

1. Selecteer **Wachtwoord instellen**.

    Een melding in het actiecentrum geeft aan dat het wachtwoord is ingesteld voor de gebruiker die u hebt gemaakt.

### <a name="create-a-location-type"></a>Een locatietype maken

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locatietypen**.
1. Selecteer in het actievenster de optie **Nieuw** om een locatietype te maken en stel hiervoor de volgende waarden in:

    - **Locatietype:** *SORTEREN*
    - **Omschrijving:** *Sorteren*

1. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-warehouse-management-parameters"></a>Parameters voor Magazijnbeheer instellen

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Stel op het tabblad **Algemeen** op het sneltabblad **Locatietypen** het veld **Locatietype voor sorteren** in op *SORTEREN*.
1. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-a-location-profile"></a>Een locatieprofiel instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst de volgende waarden in:

    - **Locatieprofiel-id:** *Sorteren*
    - **Naam:** *Sorteren*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Locatie-indeling:** *ASRB* (gang-rek-plank-bak)
    - **Locatietype:** *SORTEREN*
    - **Bijhouden nummerplaat gebruiken:** *Ja*
    - **Gemengde artikelen toestaan:** *Ja* (wanneer u deze optie op *Ja* instelt, wordt de optie **Gemengde voorraadbatches toestaan** automatisch ingesteld op *Ja* en kan dit niet onafhankelijk worden gewijzigd.)

1. Selecteer **Opslaan**.

### <a name="set-up-a-location"></a>Een locatie instellen

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**.
1. Schakel in de koptekst het selectievakje **Controlecijfers genereren voor locatie** uit.
1. Selecteer in het actievenster de optie **Nieuw** om een locatie te maken en stel hiervoor de volgende waarden in:

    - **Magazijn:** *62*
    - **Locatie:** *SORT*
    - **Locatieprofiel-id:** *SORTEREN*

1. Selecteer **Opslaan**.

### <a name="set-up-an-outbound-sorting-template"></a>Een sjabloon voor uitgaande sortering instellen

Met de sjabloon voor uitgaande sortering wordt bepaald of werk wordt gemaakt op basis van de sorteerlocatie en of handmatig of automatisch wordt gesorteerd.

Voor dit scenario maakt u een uitgaande sorteersjabloon om pallets op te bouwen na het inpakstation.

1. Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Uitgaande sorteersjabloon**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst van de nieuwe sjabloon de volgende waarden in:

    - **Id van uitgaande sorteersjabloon:** *AutoWerk*
    - **Omschrijving:** *Automatisch werk maken*
    - **Sjabloontype uitgaande sortering:** *container*
    - **Magazijn:** *62*
    - **Locatie:** *SORT*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Verificatie sorteren:** *Positie scannen*
    - **Werk maken bij positie sluiten:** *Ja*

        Als deze optie wordt ingesteld op *Ja*, wordt werk gemaakt wanneer de positie is gesloten om voorraad te verplaatsen naar de definitieve verzendlocatie. Als dit wordt ingesteld op *Nee*, wordt voorraad onmiddellijk verzameld op de order wanneer de positie wordt gesloten.

    - **Positietoewijzing:** *automatisch*

        Als dit veld wordt ingesteld op *Handmatig*, moet de gebruiker altijd aangeven op welke positie de voorraad moet worden gesorteerd. Als dit wordt ingesteld op *Automatisch* wijst het systeem de voorraad automatisch toe aan een positie, indien mogelijk op basis van de opsplitsingen in de sorteersjablonen.

1. Selecteer **Opslaan** om de optie **Query bewerken** beschikbaar te maken in het actievenster.
1. Selecteer **Query bewerken** in het actievenster.
1. Voeg in de query-editor op het tabblad **Sorteren** een regel toe met de volgende waarden:

    - **Tabel:** *Zendingen*
    - **Afgeleide tabel:** *Zendingen*
    - **Veld:** *Vervoerdersservice*

        Wanneer u deze waarde hebt geselecteerd, kan de volgende melding worden weergegeven: "Vervoerdersservice is geen indexveld. Wilt u hieraan sortering toevoegen?" Selecteer **Ja**.

    - **Zoekrichting:** *Oplopend*

1. Selecteer **OK**.
1. Het volgende bericht kan worden weergegeven: 'Groeperen wordt opnieuw ingesteld, doorgaan?' Selecteer **Ja**.

    De knop **Onderbrekingen van sjabloon uitgaande sortering** in het actievenster wordt beschikbaar.

1. Selecteer in het actievenster **Onderbrekingen van sjabloon uitgaande sortering**.
1. Stel in het dialoogvenster **Criteria voor uitgaande sortering** de volgende waarden in:

    - **Naam verwijzingstabel:** *Zendingen*
    - **Naam verwijzingsveld:** *Vervoerdersservice*
    - **Groeperen op-veld:** schakel dit selectievakje in om zendingen te groeperen op vervoerdersservice.

1. Selecteer **OK** om de instellingen op te slaan en het dialoogvenster te sluiten.

### <a name="set-up-container-packing-policies"></a>Inpakbeleid voor container instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Containers \> Inpakbeleid voor container**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst van het nieuwe beleid de volgende waarden in:

    - **Inpakbeleid voor container:** *Sorteren*
    - **Omschrijving:** *Sorteren*

1. Stel op het sneltabblad **Overzicht** de volgende waarden in:

    - **Magazijn:** *62*
    - **Standaardlocatie voor sorteren:** *SORTEREN*
    - **Gewichteenheid:** *kg*
    - **Beleid van de containerafsluiting:** *automatische vrijgave*
    - **Vrijgavebeleid voor container:** *container aan uitgaande sorteerpositie toewijzen*

1. Selecteer **Opslaan**.

### <a name="set-up-packing-profiles"></a>Verpakkingsprofielen instellen

Maak een nieuw inpakprofiel dat wordt gebruikt in combinatie met de sorteerfunctionaliteit.

1. Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Verpakkingsprofielen**.
1. Selecteer in het actievenster de optie **Nieuw** om een regel te maken en stel hiervoor de volgende waarden in:

    - **Verpakkingsprofiel-id:** *Sorteren*
    - **Omschrijving:** *Sorteren*
    - **Inpakbeleid voor container:** *Sorteren*
    - **Modus container-id:** *automatisch*
    - **Containertype:** *doos-groot*
    - **Container automatisch maken bij sluiten van container:** uitgeschakeld (= *Nee*)

1. Selecteer **Opslaan**.

### <a name="set-up-work-classes"></a>Werkklassen instellen

Stel een werkklasse in die wordt gebruikt in combinatie met sorteren.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.
1. Selecteer in het actievenster de optie **Nieuw** om een werkklasse voor sorteren te maken en stel hiervoor de volgende waarden in:

    - **Werkklasse-id:** *Sorteren*
    - **Omschrijving:** *Sorteren*
    - **Type werkorder:** *Orderverzameling van gesorteerde voorraad*

1. Selecteer **Opslaan**.

### <a name="set-up-mobile-device-menu-items"></a>Menuopdrachten voor een mobiel apparaat instellen

#### <a name="set-up-a-new-pallet-menu-item"></a>Een nieuwe menuopdracht voor pallets instellen

Maak een menuopdracht voor mobiele apparaten om pallets op te bouwen tijdens het sorteren.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst de volgende waarden in:

    - **Naam van menuopdracht:** *Pallet opbouwen*
    - **Titel:** *Pallet opbouwen*
    - **Modus:** *indirect*
    - **Bestaand werk gebruiken:** *Nee*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Activiteitscode:** *uitgaande sortering*

        Als dit veld is ingesteld op *Uitgaande sortering*, wordt het veld **Id van uitgaande sorteersjabloon** weergegeven.

    - **Verwerkingsinstructies gebruiken:** *Ja*

        Als het veld **Activiteitscode** is ingesteld op *Uitgaande sortering*, wordt deze optie automatisch ingesteld op *Ja*.

    - **Id van uitgaande sorteersjabloon:** *AutoWerk*

1. Selecteer **Opslaan**.

#### <a name="set-up-a-new-loading-menu-item"></a>Een nieuwe menuopdracht voor laden instellen

Maak vervolgens een menuopdracht waarmee gebruikers de gesorteerde voorraadartikelen kunnen verplaatsen naar de verzendlocatie.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst de volgende waarden in:

    - **Naam menuopdracht:** *Laden uit sortering*
    - **Titel:** *Laden uit sortering*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Ja*

1. Op het sneltabblad **Algemeen** moet het veld **Bestuurd door** zijn ingesteld op *Door gebruiker bestuurd*.
1. Selecteer **Nieuw** op het sneltabblad **Werkklassen** en stel de volgende waarden in:

    - **Werkklasse-id:** *SORTEREN*
    - **Type werkorder:** *Orderverzameling van gesorteerde voorraad*

1. Selecteer **Opslaan**.

### <a name="set-up-the-mobile-device-menu"></a>Het menu voor het mobiele apparaat instellen

U moet nu de nieuwe menuopdrachten toevoegen aan het menu voor het mobiele apparaat.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer het menu **Uitgaand**.
1. Selecteer **Bewerken** in het actievenster.
1. Zoek en selecteer **Pallet opbouwen** in de kolom **Beschikbare menu's en menu opdrachten**.
1. Selecteer de pijl naar rechts om **Pallet opbouwen** naar de kolom **Menustructuur** te verplaatsen.
1. Gebruik de knoppen pijl omhoog en pijl omlaag om de menuopdracht **Pallet opbouwen** op de gewenste positie in het menu van het mobiele apparaat te plaatsen.
1. Selecteer **Opslaan**.
1. Herhaal deze procedure om de menuoptie **Laden uit sorteren** toe te voegen aan het menu **Uitgaand**.

### <a name="set-up-location-directives"></a>Locatie-instructies instellen

De *locatierichtlijnen* zijn regels die verzamelings- en wegzetlocaties identificeren voor voorraadverplaatsing. U moet nu een regel maken om het sorteerwerk te beheren.

#### <a name="set-up-a-single-sku-directive"></a>Een richtlijn voor een enkele SKU instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Wijzig in het linkerdeelvenster de waarde van het veld **Werkordertype** in *Orderverzameling van gesorteerde voorraad*.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst de volgende waarden in:

    - **Reeks:** *1*
    - **Naam:** *Laaddeur*

1. Stel op het sneltabblad **Locatierichtlijnen** de volgende waarden in:

    - **Werktype:** *Wegzetten*
    - **Locatie:** *6*
    - **Magazijn:** *62*
    - **Meerdere SKU's:** *Nee*

1. Selecteer **Opslaan** om de werkbalk op het sneltabblad **Regels** beschikbaar te maken.
1. Selecteer **Nieuw** op het sneltabblad **Regels** en stel de volgende waarden in op de nieuwe regel. Accepteer de standaardwaarden voor alle overige velden.

    - **Reeks:** *1*
    - **Van:** *0*
    - **Tot:** *1.000.000*

1. Selecteer **Opslaan** om de werkbalk op het sneltabblad **Locatie-instructieacties** beschikbaar te maken.
1. Selecteer **Nieuw** op het sneltabblad **Locatie-instructieacties** en stel de volgende waarden in op de nieuwe regel. Accepteer de standaardwaarden voor alle overige velden.

    - **Reeks:** *1*
    - **Naam:** *Laaddeur*

1. Selecteer **Opslaan**.
1. Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.
1. Zoek in de query-editor op het tabblad **Bereik** de rij waar het veld **Veld** is ingesteld op *Locatie*. Stel het veld **Criteria** voor deze rij in op *Laaddeur*.
1. Selecteer **OK** om de instellingen op te slaan en de query-editor te sluiten.

#### <a name="set-up-a-multiple-sku-directive"></a>Een richtlijn voor meerdere SKU's instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Wijzig in het linkerdeelvenster de waarde van het veld **Werkordertype** in *Orderverzameling van gesorteerde voorraad*.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de koptekst de volgende waarden in:

    - **Reeks:** *2*
    - **Naam:** *Meerdere laaddeuren*

1. Stel op het sneltabblad **Locatierichtlijnen** de volgende waarden in:

    - **Werktype:** *Wegzetten*
    - **Locatie:** *6*
    - **Magazijn:** *62*
    - **Meerdere SKU'S:** *Ja*

1. Selecteer **Opslaan** om de werkbalk op het sneltabblad **Regels** beschikbaar te maken.
1. Selecteer **Nieuw** op het sneltabblad **Regels** en stel de volgende waarden in op de nieuwe regel. Accepteer de standaardwaarden voor alle overige velden.

    - **Reeks:** *1*
    - **Van:** *0*
    - **Tot:** *1.000.000*

1. Selecteer **Opslaan** om de werkbalk op het sneltabblad **Locatie-instructieacties** beschikbaar te maken.
1. Selecteer **Nieuw** op het sneltabblad **Locatie-instructieacties** en stel de volgende waarden in op de nieuwe regel. Accepteer de standaardwaarden voor alle overige velden.

    - **Reeks:** *1*
    - **Naam:** *Meerdere laaddeuren*

1. Selecteer **Opslaan**.
1. Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.
1. Zoek in de query-editor op het tabblad **Bereik** de rij waar het veld **Veld** is ingesteld op *Locatie*. Stel het veld **Criteria** voor deze rij in op *Laaddeur*.
1. Selecteer **OK** om de instellingen op te slaan en de query-editor te sluiten.

### <a name="set-up-work-templates"></a>Werksjablonen instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Wijzig de waarde van het veld **Werkordertype** in *Orderverzameling van gesorteerde voorraad*.
1. Selecteer in het actievenster **Nieuw** om een werksjabloon te maken.
1. Stel op het tabblad **Overzicht** de volgende waarden in:

    - **Reeks:** *1*
    - **Werksjabloon:** *Sorteren*
    - **Omschrijving werksjabloon:** *Sorteren*

1. Selecteer **Opslaan** om het sneltabblad **Werksjabloongegevens** beschikbaar te maken.
1. Selecteer **Nieuw** op het sneltabblad **Details van werksjabloon** om een regel toe te voegen en stel de volgende waarden voor de regel in:

    - **Werktype:** *Orderverzamelen*
    - **Werkklasse-id:** *SORTEREN*

1. Selecteer nogmaals **Nieuw** om een tweede regel toe te voegen en stel de volgende waarden in:

    - **Werktype:** *Wegzetten*
    - **Werkklasse-id:** *SORTEREN*

1. Selecteer **Opslaan**.

## <a name="scenario"></a>Scenario's

Dit scenario simuleert een situatie waarin verpakte containers automatisch worden gesorteerd op verschillende posities (pallets) na het inpakstation, afhankelijk van de vervoerdersservice. Nadat alle artikelen van de lading zijn verpakt en op adres zijn gesorteerd, worden de pallets verplaatst naar de laaddeur.

### <a name="create-sales-orders-and-picking-work"></a>Verkooporders en werk voor orderverzamelen maken

#### <a name="create-sales-order-1"></a>Verkooporder 1 maken

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-005*
    - **Magazijn:** *62*

1. Selecteer **OK** om het dialoogvenster te sluiten.

    De nieuwe verkooporder wordt geopend.

1. Schakel over naar de weergave **Koptekst**.
1. Stel op het sneltabblad **Levering** in de sectie **Transport** de volgende waarden in:

    - **Vervoerder:** *Air Cargo*
    - **Vervoerdersservice:** *Air*

1. Ga naar de weergave **Regels**.
1. Als een nieuwe, lege regel niet automatisch wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels** selecteert u de optie **Regel toevoegen** om een regel toe te voegen.
1. Stel de volgende waarden in voor de nieuwe orderregel:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *2*

1. Terwijl de nieuwe orderregel nog steeds is geselecteerd op het sneltabblad **Verkooporderregels**, selecteert u **Reservering** in het menu **Voorraad** boven het raster.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.
1. U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven. Noteer de nummers van de wave-id en de zending-id.

#### <a name="sales-order-2"></a>Verkooporder 2

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-006*
    - **Magazijn:** *62*

1. Selecteer **OK** om het dialoogvenster te sluiten.
1. De nieuwe verkooporder wordt geopend. Deze moet een nieuwe, lege regel bevatten in het raster op het sneltabblad **Verkooporderregels**. Stel de volgende waarden in op deze orderregel:

    - **Artikel:** *A0001*
    - **Hoeveelheid:** *1*

1. Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Leveringsmethode** in op *Flowe-STD*.
1. Selecteer **Regel toevoegen** op het sneltabblad **Regels verkooporder** en stel de volgende waarden in op de tweede orderregel:

    - **Artikel:** *A0002*
    - **Hoeveelheid:** *1*

1. Wijzig op het sneltabblad **Regeldetails** op het tabblad **Levering** de waarde van het veld **Leveringsmethode** in *Air C-Air*.
1. Selecteer de eerste orderregel op het sneltabblad **Verkooporderregels**. Selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Selecteer de tweede orderregel op het sneltabblad **Verkooporderregels**. Selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.
1. U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven. Er zijn twee wave-id-nummers en twee verzend-id-nummers gemaakt, één voor elke leveringsmethode voor de verkooporderregels.

#### <a name="get-the-work-ids-from-the-work-details"></a>De werk-id's ophalen uit de werkdetails

1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. Op de pagina worden de werk-id's weergegeven die zijn gemaakt op basis van verkooporders. Gebruik de wave-id's en verzend-id's van de verkooporders die u hebt gemaakt om de werk-id voor elke wave en zending te vinden. Noteer deze werk-id's omdat u ze in de volgende stappen nodig hebt. U ziet dat er twee werk-id's zijn gemaakt voor de tweede verkooporder. Als er verschillende artikelen worden verzameld vanuit verschillende locaties, worden afzonderlijke werk-id's gegenereerd.

### <a name="pick-items-for-the-sales-orders"></a>Artikelen voor de verkooporders verzamelen

Voltooi het gemaakte werk door met het mobiele apparaat de artikelen naar het inpakstation te verplaatsen.

1. Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).
1. Selecteer **Uitgaand** in het hoofdmenu.
1. Selecteer **Orderverzamelen** in het menu **Uitgaand**.
1. Voer in het veld **Id** de werk-id in die voor verkooporder 1 is gemaakt.
1. Selecteer **OK**.
1. Voer op de pagina **Verkooporders - verzamelen** een doel-LP in die is gemaakt voor verkooporder 1. U ziet dat de orderverzamellocatie (*bulk-001*), artikel (*A0001*) en hoeveelheid (*2 stuks*) worden weergegeven.
1. Selecteer **OK**.
1. Bekijk de informatie op de pagina **Verkooporders: wegzetten**. Het veld **Loc** moet aangeven dat de verzamelde artikelen naar de *Inpak* locatie gaan.
1. Selecteer **OK**.

    Op de pagina **Een werk-id/nummerplaat-id scannen** ziet u het bericht "Werk voltooid", wat aangeeft dat de werk-id van verkooporder 1 is voltooid.

    U gaat nu verkooporder 2 verzamelen.

1. Voer in het veld **Id** de werk-id in die voor verkooporder 2 is gemaakt, waarin regel 1 artikel *A0001* bevat.
1. Selecteer **OK**.
1. Voer op de pagina **Verkooporders - verzamelen** een doel-LP in. U ziet dat de orderverzamellocatie (*bulk-001*), artikel (*A0001*) en hoeveelheid (*1 stuks*) worden weergegeven.
1. Selecteer **OK**.
1. Bekijk de informatie op de pagina **Verkooporders: wegzetten**. Het veld **Loc** moet aangeven dat de verzamelde artikelen naar de *Inpak* locatie gaan.
1. Selecteer **OK**.

    Op de pagina **Een werk-id/nummerplaat-id scannen** ontvangt u het bericht "Werk voltooid". Dit bericht geeft aan dat de werk-id van regel 1 van verkooporder 2 is voltooid.

1. Voer in het veld **Id** de werk-id in die voor verkooporder 2 is gemaakt, waarin regel 2 artikel *A0002* bevat.
1. Selecteer **OK**.
1. Voer op de pagina **Verkooporders - verzamelen** een doel-LP in. U ziet dat de orderverzamellocatie (*bulk-002*), artikel (*A0001*) en hoeveelheid (*1 stuks*) worden weergegeven.
1. Selecteer **OK**.
1. Bekijk de informatie op de pagina **Verkooporders: wegzetten**. Het veld **Loc** moet aangeven dat de verzamelde artikelen naar de *Inpak* locatie gaan.
1. Selecteer **OK**.

    Op de pagina **Een werk-id/nummerplaat-id scannen** ontvangt u het bericht "Werk voltooid". Dit bericht geeft aan dat de werk-id van regel 2 van verkooporder 2 is voltooid.

### <a name="pack-sales-orders-into-containers"></a>Verkooporders in containers inpakken

#### <a name="pack-sales-order-1-into-containers"></a>Verkooporder 1 in containers inpakken

1. Ga naar **Magazijnbeheer \> Verpakking en containervorming \> Verpakken**.

    Het dialoogvenster **Inpakstation selecteren** verschijnt. Het veld **Medewerker** moet standaard zijn ingesteld op de naam van de medewerker die u eerder hebt ingesteld.

1. Stel de volgende waarden in voor het weergeven en bewerken van zendingen en containers die zijn gepland op de specifieke inpaklocatie:

    - **Locatie:** *6*
    - **Magazijn:** *62*
    - **Locatie:** *Verpakken*
    - **Verpakkingsprofiel-id:** *Sorteren*

1. Selecteer **OK** om het dialoogvenster te sluiten.
1. Voer op de pagina **Verpakken** in het veld **Nummerplaat of zending** de doel-LP in voor verkooporder 1. Selecteer vervolgens de toets **Tab** of **ENTER** op het toetsenbord om het veld te verlaten.
1. Selecteer **Nieuwe container** in het actievenster.
1. Accepteer alle standaardinstellingen en selecteer **OK**. Noteer de container-id.
1. Stel op het sneltabblad **Artikel verpakken** de volgende waarden in:

    - **Hoeveelheid:** *1*
    - **Id:** artikel *A0001*

1. Selecteer **Container sluiten** in het actievenster.
1. Selecteer in het dialoogvenster **Container sluiten** de optie **Systeemgewicht ophalen** om het veld **Brutogewicht** bij te werken.
1. Selecteer **OK**. De container wordt verplaatst naar de locatie *SORTEREN* en kan worden gesorteerd.
1. Maak een tweede container om het tweede artikel uit de nummerplaat voor verkooporder 1 toe te voegen aan een nieuwe container.
1. Selecteer **Nieuwe container** in het actievenster.
1. Accepteer alle standaardinstellingen en selecteer **OK**. Noteer de container-id.
1. Stel op het sneltabblad **Artikel verpakken** de volgende waarden in:

    - **Hoeveelheid:** *1*
    - **Id:** artikel *A0001*

1. Selecteer **Container sluiten** in het actievenster.
1. Selecteer in het dialoogvenster **Container sluiten** de optie **Systeemgewicht ophalen** om het veld **Brutogewicht** bij te werken.
1. Selecteer **OK**. De container wordt verplaatst naar de locatie *SORTEREN* en kan worden gesorteerd.

#### <a name="pack-sales-order-2-into-containers"></a>Verkooporder 2 in containers inpakken

1. Voer op de pagina **Verpakken** in het veld **Nummerplaat of zending** de doel-LP in voor regel 1 van verkooporder 2. Selecteer vervolgens de toets **Tab** of **ENTER** op het toetsenbord om het veld te verlaten.
1. Selecteer **Nieuwe container** in het actievenster.
1. Accepteer alle standaardinstellingen en selecteer **OK**. Noteer de container-id.
1. Stel op het sneltabblad **Artikel verpakken** de volgende waarden in:

    - **Hoeveelheid:** *1*
    - **Id:** artikel *A0001*

1. Selecteer **Container sluiten** in het actievenster.
1. Selecteer in het dialoogvenster **Container sluiten** de optie **Systeemgewicht ophalen** om het veld **Brutogewicht** bij te werken.
1. Selecteer **OK**. De container wordt verplaatst naar de locatie *SORTEREN* en kan worden gesorteerd.
1. Voer in het veld **Nummerplaat of zending** de doel-LP in voor regel 2 van de verkooporder 2. Selecteer vervolgens de toets **Tab** of **ENTER** op het toetsenbord om het veld te verlaten.
1. Selecteer **Nieuwe container** in het actievenster.
1. Accepteer alle standaardinstellingen en selecteer **OK**. Noteer de container-id.
1. Stel op het sneltabblad **Artikel verpakken** de volgende waarden in:

    - **Hoeveelheid:** *1*
    - **Id-veld:** artikel *A0002*

1. Selecteer **Container sluiten** in het actievenster.
1. Selecteer in het dialoogvenster **Container sluiten** de optie **Systeemgewicht ophalen** om het veld **Brutogewicht** bij te werken.
1. Selecteer **OK**. De container wordt verplaatst naar de locatie *SORTEREN* en kan worden gesorteerd.

Als u de containerdetails wilt weergeven, gaat u naar **Magazijnbeheer \> Verpakking en containervorming \> Containers** en zoekt u naar de container-id's die tijdens de verpakking zijn gemaakt.

### <a name="sort-the-containers"></a>De containers sorteren

> [!IMPORTANT]
> Wanneer u de menuopdracht **Pallet opbouwen** opent in de mobiele app om uitgaande sortering uit te voeren, ziet u een knop met het opschrift **Vol**. *Gebruik de knop **Vol** niet om de positie te sorteren of te sluiten.*
>
> De knop **Vol** is standaard aanwezig en kan niet worden uitgeschakeld of verwijderd van de pagina. Deze wordt niet gebruikt voor de functie *Uitgaande sortering*.

#### <a name="sort-the-first-container"></a>Eerste container sorteren

1. Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).
1. Selecteer **Uitgaand** in het hoofdmenu.
1. Selecteer **Orderverzamelen** in het menu **Pallet opbouwen**.
1. Voer in het veld **LP/con** de eerste container-id in die aan verkooporder 1 is gekoppeld.
1. Selecteer **OK**.
1. Omdat er nog geen sorteerposities bestaan, moet u deze opgeven. Voer in het veld **Sorteerpositie-id** de tekst *SP01* in.
1. Omdat er geen LP is gekoppeld aan sorteerpositie *SP01*, moet u deze opgeven. Voer in het veld **LP** de waarde *PLP01* in.
1. Selecteer **OK**.
1. Aangezien de validatie van de sorteerpositie is ingeschakeld, moet u de sorteerpositie-id opnieuw invoeren. Voer in het veld **Sorteerpositie-id** de tekst *SP01* in.
1. Selecteer **OK**.

    U ziet de melding "Werk voltooid".

> [!TIP]
> Als u de sorteerpositie en de LP erin wilt weergeven, gaat u naar **Magazijnbeheer \> Verpakking en containervorming \> Toewijzingen uitgaande sorteerpositie**.
>
> Op de pagina **Toewijzingen uitgaande sorteerpositie** worden alle sorteerposities weergegeven die momenteel actief zijn. In het veld **Positietransacties sorteren** wordt de LP weergegeven die is gekoppeld aan elke sorteerpositie en de containers in de sorteerpositie. U ziet dat er op dit moment één sorteerpositie bestaat en dat in het sneltabblad **Criteria voor sorteerpositie** een criterium wordt weergegeven voor **Zending - vervoerdersservice - Air**.

#### <a name="sort-the-remaining-containers"></a>De resterende containers sorteren

1. Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).
1. Selecteer **Uitgaand** in het hoofdmenu.
1. Selecteer **Orderverzamelen** in het menu **Pallet opbouwen**.
1. Voer in het veld **LP/con** de tweede container-id in die aan verkooporder 1 is gekoppeld.
1. Selecteer **OK**. Omdat de sorteersjabloon zo is ingesteld dat deze automatisch wordt gesorteerd en er al een sorteerpositie met overeenkomstige criteria bestaat, wordt u automatisch doorverwezen naar de juiste sorteerpositie.
1. Selecteer **OK**.
1. Bevestig de sorteerpositie-id om aan te geven dat de voorraad zich op de juiste plaats bevindt. Voer in het veld **Sorteerpositie-id** de tekst *SP01* in.
1. Selecteer **OK**.

    Het werk voor de tweede container wordt uitgevoerd vanuit verkooporder 1. U gaat nu de overige containers van verkooporder 2 sorteren.

1. Voer in het veld **LP/Con** de container-id in van de container van verkooporder 2 die artikel *A0001* bevat. Aangezien de vervoerdersservice verschilt, wordt u gevraagd een nieuwe sorteerpositie in te voeren en een LP aan die positie toe te wijzen. Gebruik de sorteerpositie *SP02* en LP *PLP02*.
1. Selecteer **OK**.
1. Bevestig de sorteerpositie door *SP02* in te voeren in het veld **Sorteerpositie-id**.
1. Selecteer **OK**.

    Het werk voor de container is voltooid.

1. Voer in het veld **LP/Con** de container-id in voor de resterende container van verkooporder 2 die artikel *A0002* bevat. Aangezien de vervoerdersservice dezelfde is als de vervoerder voor verkooporder 1, wordt in het systeem de bestaande sorteerpositie weergegeven met de overeenkomstige criteria.
1. Selecteer **OK**.
1. Bevestig de sorteerpositie door *SP01* in te voeren in het veld **Sorteerpositie-id**.
1. Selecteer **OK**.

    Het werk voor de container is voltooid.

### <a name="close-the-outbound-sorting-positions"></a>De uitgaande sorteerposities sluiten

Wanneer alle voorraad is gesorteerd, moet de positie worden gesloten voordat het werk kan worden gemaakt. Werk voor de gesorteerde voorraadverzameling wordt gemaakt om de voorraad naar de laaddeur te verplaatsen.

#### <a name="close-a-position-from-the-mobile-device"></a>Een positie vanaf het mobiele apparaat sluiten

1. Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).
1. Selecteer **Uitgaand** in het hoofdmenu.
1. Selecteer **Orderverzamelen** in het menu **Pallet opbouwen**.
1. Voer in het veld **LP/Con** een container-id in die is gesorteerd om positie *SP01* te sorteren.
1. Selecteer **OK**.
1. Het volgende bericht wordt weergegeven: "De container is al gesorteerd om SP01 te positioneren. De positie sluiten?" Selecteer **Sluiten**.

    Werk is voltooid.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Een positie sluiten vanuit toewijzingen voor een uitgaande sorteerpositie

1. Ga naar **Magazijnbeheer \> Verpakking en containervorming \> Toewijzingen uitgaande sorteerpositie**.
1. Selecteer **SP02** in de linkerkolom. Deze rij met de uitgaande sorteerpositie is de rij die u gaat sluiten.
1. Selecteer **Positie sluiten** in het actievenster. De sorteerpositierecord wordt gesloten en wordt niet meer weergegeven.

    > [!TIP]
    > Als u alle gesloten positierecords wilt weergeven, schakelt u het selectievakje **Gesloten weergeven** in.

### <a name="sorted-inventory-picking"></a>Gesorteerde orderverzameling voorraad

U moet het werk voor de gesorteerde voorraadverzameling voltooien. Wanneer dit is voltooid, wordt de voorraad verzameld voor de verkooporder. Op dat moment zijn alle andere magazijnprocessen van toepassing.

1. Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).
1. Selecteer **Uitgaand** in het hoofdmenu.
1. Selecteer in het menu **Uitgaand** de optie **Laden uit sortering**.
1. Voer de id van het doel-LP in voor de eerste sorteerpositie *SP01*. Stel het veld **Id** in op *PLP01*.
1. Selecteer **OK**.
1. De pagina **Orderverzameling van gesorteerde voorraad: orderverzamelen** toont het werk dat moet worden uitgevoerd voor het orderverzamelen. Kies uit de locatie *SORTEREN* en de doel-LP *PLP01*, die meerdere artikelen en een hoeveelheid van *3* heeft.
1. Selecteer **OK**.
1. De pagina **Orderverzameling van gesorteerde voorraad: wegzetten** toont het werk dat moet worden uitgevoerd voor het wegzetten. Zet weg naar de locatie *Laaddeur* en de doel-LP *PLP01*, die meerdere artikelen en een hoeveelheid van *3* heeft.
1. Selecteer **OK**.

    Werk is voltooid.

1. Voer de id van het doelnummerplaat in voor de tweede sorteerpositie *SP02*. Stel het veld **Id** in op *PLP02*.
1. Selecteer **OK**.
1. De pagina **Orderverzameling van gesorteerde voorraad: orderverzamelen** toont het werk dat moet worden uitgevoerd voor het orderverzamelen. Kies uit de locatie *SORTEREN* en de doel-LP *PLP02*, die meerdere artikelen en een hoeveelheid van *1* heeft.
1. Selecteer **OK**.
1. De pagina **Orderverzameling van gesorteerde voorraad: wegzetten** toont het werk dat moet worden uitgevoerd voor het wegzetten. Zet weg naar de locatie *Laaddeur* en de doel-LP *PLP02*, die meerdere artikelen en een hoeveelheid van *1* heeft.
1. Selecteer **OK**.

    Werk is voltooid.

Vanaf dit punt zijn alle andere magazijnprocessen van toepassing.
