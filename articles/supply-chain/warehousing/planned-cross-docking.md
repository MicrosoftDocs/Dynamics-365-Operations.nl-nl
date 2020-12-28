---
title: Gepland cross-docken
description: In dit onderwerp wordt geavanceerd gepland cross-docking beschreven, waarbij de voorraadhoeveelheid die nodig is voor een order rechtstreeks van ontvangst of maken naar het juiste outbound dock of klaarzetlocatie wordt gestuurd. Alle resterende voorraad uit de inkomende bron wordt via het normale wegzetproces naar de juiste opslaglocatie gestuurd.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425843"
---
# <a name="planned-cross-docking"></a>Gepland cross-docken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt geavanceerd gepland cross-docking beschreven. Cross-docking is een magazijnproces waarbij de voorraadhoeveelheid die nodig is voor een order rechtstreeks van ontvangst of maken naar het juiste outbound dock of klaarzetlocatie wordt gestuurd. Alle resterende voorraad uit de inkomende bron wordt via het normale wegzetproces naar de juiste opslaglocatie gestuurd.

Bij cross-docken kunnen de werknemers het wegzetten van inkomende artikelen en het verzamelen voor uitgaande artikelen overslaan voor voorraat die al voor een uitgaande order is gemarkeerd. Zo wordt het aantal aanrakingsmomenten voor voorraad waar mogelijk zo klein mogelijk gehouden. Omdat er minder interactie is met het systeem, kan worden bespaard op tijd en ruimte op de magazijnvloer.

Voordat cross-docken kan worden uitgevoerd, moet de gebruiker een nieuwe sjabloon voor cross-docken configureren, waarin de voorraadbron en andere reeksen vereisten voor cross-docken worden opgegeven. Wanneer de uitgaande order wordt gemaakt, moet de regel worden gemarkeerd voor een inkomende order die hetzelfde artikel bevat.

Bij ontvangst van inkomende orders identificeert de cross-dockingconfiguratie automatisch dat cross-docken vereist is, en maakt het werk aan voor verplaatsing van de vereiste hoeveelheid op basis van de configuratie van de locatie-instructie.

> [!NOTE]
> Registratie van voorraadtransacties wordt **niet** ongedaan gemaakt wanneer het cross-dockingwerk wordt geannuleerd, zelfs als de instelling voor deze mogelijkheid is ingeschakeld in de parameters van magazijnbeheer.

## <a name="turn-on-the-planned-cross-docking-feature"></a>De functie Gepland cross-docken inschakelen

Voordat u geavanceerd gepland cross-docken kunt gebruiken, moet de functie zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Gepland cross-docken*

## <a name="setup"></a>Instellen

### <a name="regenerate-load-posting-methods"></a>Boekingsmethoden voor lading opnieuw genereren

Gepland cross-docken wordt geïmplementeerd als een boekingsmethode voor lading. Nadat u de functie hebt ingeschakeld, moet u de methoden opnieuw genereren.

1. Ga naar **Magazijnbeheer \> Instellen \> Boekingsmethoden voor lading**.
1. Selecteer in het actievenster **Methoden opnieuw genereren**.

    Wanneer de regeneratie is voltooid, moet u een methode met de **methodenaam** *planCrossDocking* zien.

1. Sluit de pagina.

### <a name="create-a-cross-docking-template"></a>Een cross-dockingsjabloon maken

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Sjablonen voor cross-docken**.
1. Selecteer in het actievenster **Nieuw** om een sjabloon te maken.
1. Stel in de koptekst de volgende waarden in:

    - **Reeks:** *1*

        Dit veld bepaalt de volgorde waarin sjablonen worden geëvalueerd.

    - **Id van cross-dockingsjabloon:** *51*
    - **Beschrijving:** *Magazijn 51*
    - **Beleid voor vraagvrijgave:** *Voor ontvangst van levering*
    - **Magazijn:** *51*

1. De instellingen op het sneltabblad **Planning** bepalen hoe de sjabloon werkt. Stel de volgende waarden in:

    - **Vereisten voor vraag:** *geen*

        In dit veld worden de vereisten van de vraagvoorraad gedefinieerd. Als de vraag vóór vrijgave moet worden gekoppeld aan de levering, selecteert u *Markering*. Selecteer *Orderreservering* als de vraag vóór vrijgave moet worden gereserveerd voor de levering.

    - **Lokaliseringstype:** *Verzendlocaties*

        In dit veld wordt gedefinieerd of het werk voor cross-docken de klaarzet/ladinglocaties van de zending moet gebruiken of naar de locatie-instructies moet kijken om zelf een klaarzet-/ladinglocatie te vinden.

    - **Werksjabloon**: Laat dit veld leeg.

        In dit veld wordt de werksjabloon gedefinieerd die moet worden gebruikt bij het maken van cross-dockingwerk.

    - **Opnieuw valideren bij ontvangst levering:** *Nee*

        Met deze optie wordt bepaald of de levering opnieuw moet worden gevalideerd tijdens de ontvangst. Als deze optie is ingesteld op *Ja*, worden zowel het maximumtijdvenster als het bereik voor vervaldagen gecontroleerd.

    - **Tijdvenster valideren:** *Ja*

        Met deze optie wordt bepaald of het maximumtijdvenster moet worden geëvalueerd wanneer een voorraadbron wordt geselecteerd. Als deze optie is ingesteld op *Ja*, worden de velden die zijn gerelateerd aan de maximum- en minimumtijdvensters beschikbaar.

    - **Maximumtijdvenster:** *5*

        In dit veld wordt de maximale periode gedefinieerd die is toegestaan tussen aankomst van een levering en vertrek van gevraagde artikelen.

    - **Eenheid maximumtijdvenster:** *Dagen*
    - **Minimumtijdvenster:** *0*

        In dit veld wordt de minimale periode gedefinieerd die is toegestaan tussen aankomst van een levering en vertrek van gevraagde artikelen.

    - **Eenheid minimumtijdvenster:** *Dagen*
    - **Bereik vervaldagen:** *0*

        *Criteria voor FEFO (First Expiry, First Out):* De waarde in dit veld bepaalt het maximumaantal dagen tussen de vervaldatum van de eerste batch die zich momenteel in het magazijn bevindt en de batch die wordt ontvangen.

1. Op het sneltabblad **Leveringsbronnen** geeft u de typen leveringen op die geldig zijn voor deze sjabloon. Selecteer **Nieuw** en stel de volgende waarden in:

    - **Volgnummer:** *1*
    - **Leveringsbron:** *Inkooporder*

### <a name="create-a-work-class"></a>Een werkklasse maken

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.
1. Selecteer in het actievenster **Nieuw** om een werkklasse te maken.
1. Stel de volgende waarden in:

    - **Werkklasse-id:** *CrossDock*
    - **Beschrijving:** *Cross-docken*
    - **Werkordertype:** *Cross-docken*

### <a name="create-a-work-template"></a>Een werksjabloon maken

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Stel het veld **Werkordertype** in op *Cross-docking*.
1. Selecteer in het actievenster de optie **Nieuw** om een regel toe te voegen aan het tabblad **Overzicht**.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Volgnummer:** *1*
    - **Werksjabloon:** *51 Cross-dock*
    - **Beschrijving werksjabloon:** *51 Cross-dock*

1. Selecteer **Opslaan** om het sneltabblad **Werksjabloongegevens** beschikbaar te maken.
1. Ga naar het sneltabblad **Werksjabloongegeven** en selecteer **Nieuw** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Werktype:** *Orderverzamelen*
    - **Werkklasse-id:** *CrossDock*

1. Selecteer **Nieuw** om nog een regel toe te voegen en stel de volgende waarden in:

    - **Werktype:** *Wegzetten*
    - **Werkklasse-id:** *CrossDock*

1. Selecteer **Opslaan** en bevestig dat het selectievakje **Geldig** is ingeschakeld voor de sjabloon *51 Cross-docken*.

> [!NOTE]
> De werkklasse-id's voor de werktypen *Verzamelen* en *Wegzetten* moeten hetzelfde zijn.

### <a name="create-location-directives"></a>Maak locatie-instructies aan

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Stel in het linkerdeelvenster het veld **Werkordertype** in op *Cross-docking*.
1. Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:

    - **Volgnummer:** *1*
    - **Naam:** *51 cross-docken voor wegzetten*
    - **Werktype:** *Wegzetten*
    - **Locatie:** *5*
    - **Magazijn:** *51*

1. Selecteer **Opslaan** om het sneltabblad **Regels** beschikbaar te maken.
1. Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Vanaf hoeveelheid:** *1*
    - **Tot hoeveelheid:** *1000000*

1. Selecteer **Opslaan** om het sneltabblad **Locatie-instructieacties** beschikbaar te maken.
1. Ga naar het sneltabblad **Locatie-instructieacties** en selecteer **Nieuw** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Naam:** *Laaddeur*
    - **Gebruik vaste locaties:** *Vaste en niet-vaste locaties*

1. Selecteer **Opslaan** om de knop **Query bewerken** op de werkbalk **Locatie-instructieacties** beschikbaar te maken.
1. Selecteer **Query bewerken** om de query-editor te openen.
1. Controleer of op het tabblad **Bereik** de volgende twee regels zijn geconfigureerd:

    - Regel 1:

        - **Tabel:** *Locaties*
        - **Afgeleide tabel:** *Locaties*
        - **Veld:** *Magazijn*
        - **Criteria:** *51*

    - Regel 2:

        - **Tabel:** *Locaties*
        - **Afgeleide tabel:** *Locaties*
        - **Veld:** *Locatie*
        - **Criteria:** *Laaddeur*

1. Selecteer **OK** om de query-editor te sluiten.

### <a name="create-a-mobile-device-menu-item"></a>Een menuopdracht van mobiel apparaat maken

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in de lijst met menuopdrachten in het linkerdeelvenster de optie **Opslag van inkoop**.
1. Selecteer **Bewerken**.
1. Ga naar het sneltabblad **Werkklassen** en selecteer **Nieuw** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Werkklasse-id:** *CrossDock*
    - **Werkordertype:** *Cross-docken*

1. Selecteer **Opslaan**.

## <a name="scenario"></a>Scenario's

### <a name="create-a-purchase-order"></a>Inkooporder maken

Volg deze stappen om een inkooporder te maken als leveringsbron.

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:

    - **Leverancierrekening:** *104*
    - **Magazijn:** *51*

1. Selecteer **OK** en noteer het ordernummer.
1. Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Inkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *5*

### <a name="create-a-sales-order"></a>Verkooporder maken

Volg deze stappen om een verkooporder te maken als een bron van vraag.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-002*
    - **Magazijn:** *51*

1. Selecteer **OK**.
1. Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *3*

### <a name="create-planned-cross-docking"></a>Gepland cross-docken maken

Volg deze stappen om het geplande cross-docken te maken vanuit de verkooporder.

1. Ga naar de pagina **Verkooporderdetails** voor de verkooporder die u zojuist hebt gemaakt. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven naar magazijn**.

    Met de actie Vrijgeven naar magazijn wordt een zending- en laadregel gemaakt voor de verkooporderregel en wordt geprobeerd om voorraad toe te wijzen.
    
    U ontvangt een melding. Ook wordt het volgende waarschuwingsbericht weergegeven: "Er is geen werk gemaakt voor wave XXXX. Zie het logbestand voor werk aanmaken voor meer informatie." Dit gedrag is verwacht, omdat het magazijn geen voorraad bevat.

1. Selecteer op het sneltabblad **Verkooporderregels** in het menu **Magazijn** boven het raster de waarde **Details van zending**.

    De pagina **Details van zending** wordt weergegeven en toont de zending die voor de verkooporder is gemaakt.

1. In het sneltabblad **Ladingsregels** ziet u dat het veld **Hoeveelheid voor gepland cross-docken** is ingesteld op *3*. Omdat er in het magazijn geen voorraad beschikbaar was, maar een geldige leveringsbron zal aankomen binnen het tijdvenster dat is gedefinieerd in de sjabloon voor cross-docken, is de hoeveelheid voor cross-docken gemaakt.
1. Selecteer op het sneltabblad **Ladingsregels** de optie **Gepland cross-docken** om de details weer te geven van de aangemaakte cross-docking.

## <a name="process-the-cross-docking"></a>De cross-docking verwerken

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Nummerplaat ontvangen in de mobiele magazijnapp

Het systeem ontvangt de 5 stuks van de inkooporder op de ontvangende locatie en er wordt twee keer werk aangemaakt.

De eerste werk-id die wordt gemaakt, heeft als **werkordertype** *Cross-docken* en is gekoppeld aan de verkooporder. De id heeft een hoeveelheid van 3 en wordt naar de uiteindelijke verzendlocatie gestuurd, zodat deze direct kan worden verzonden.

De tweede werk-id die wordt gemaakt, heeft als **werkordertype** *Inkooporders* en is gekoppeld aan de inkooporder. Het bevat de resterende hoeveelheid van 2 die niet is gecross-docked en die moet worden weggezet in opslag.

1. Meld u aan bij het mobiele apparaat als een gebruiker in magazijn *51*.
1. Ga naar **Inkomend \> Inkoop ontvangen**.
1. Voer in het veld **Inkoopordernummer** het inkoopordernummer in.
1. Voer in het veld **Hoeveelheid** de waarde *5* in.
1. Selecteer **OK**.
1. Stel op de volgende pagina het veld **Artikel** in op *A0001*.
1. Selecteer **OK**.
1. Bevestig op de volgende pagina de waarden voor **Inkoopordernummer** , **Artikel** en **Hoeveelheid** door op **OK** te klikken.

    U ontvangt de melding Werk voltooid.

1. Selecteer **Annuleren** om af te sluiten.

### <a name="put-away-to-cross-docking-and-bulk"></a>Wegzetten voor cross-docking en bulk

Momenteel hebben beide werk-id's dezelfde doelnummerplaat. Om de volgende stappen uit te voeren, moet u de werk-id en de doelnummerplaat-id ophalen. U kunt deze informatie ophalen uit de werkgegevens voor de inkooporderregel en de verkooporderregel. U kunt ook naar **Magazijnbeheer \> Werk \> Werkdetails** gaan en filteren op werk waar de waarde van **Magazijn** is ingesteld op *51*.

1. Ga op het mobiele apparaat naar de **Inkomend \> Opslag van inkoop** en voer het nummer van de doelnummerplaat van het werk in.
1. Voer in het veld **Id** de identificatiecode voor de doelnummerplaat uit de werkdetails in.

    Op de pagina voor cross-dockingverzamelen worden de orderverzamellocatie (*RECV*), de doelnummerplaat (*nummerplaat*), het artikel (*A0001*) en de hoeveelheid (*3*) getoond.

1. Selecteer **OK**.
1. Voer in het veld **Doel-NP** een doelnummerplaat in voor de nummerplaat-id die moet worden weggezet (cross-docked) naar de verzendlocatie. U kunt elke gewenste nummerplaat-id selecteren.
1. Selecteer **OK**.
1. Voer op de volgende pagina in het veld **Id** de identificatiecode voor de doelnummerplaat in.
1. Selecteer **OK**.
1. Bevestig het werk voor het verzamelen van de resterende hoeveelheid van 2 en selecteer **OK**.
1. Selecteer op de volgende pagina **Gereed** om het orderverzamelproces te beëindigen en het wegzetproces te starten.

    De mobiele app geeft u de locatie en de nummerplaat weer waarop u het artikel kunt wegzetten.

1. Bevestig de bulkopslag **Wegzetten** door **OK** te selecteren.
1. Bevestig op de volgende pagina de cross-docking **Wegzetten** door op **OK** te klikken.

    U ontvangt de melding Werk voltooid.

1. Selecteer **Annuleren** om af te sluiten.

In de volgende afbeelding wordt weergegeven hoe het voltooide cross-dockingwerk kan worden weergegeven in Microsoft Dynamics 365 Supply Chain Management.

![Cross-dockingwerk voltooid](media/PlannedCrossDockingWork.png "Cross-dockingwerk voltooid")
