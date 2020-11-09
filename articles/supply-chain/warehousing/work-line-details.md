---
title: Details werkregel
description: Dit onderwerp biedt informatie over de pagina Details werkregel, waarin een uitgebreide, sorteerbare en filterbare lijst met afzonderlijke werkregels in het systeem wordt weergegeven.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bcb340b21e06b294a40784bf3a1da71b0daf7655
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015890"
---
# <a name="work-line-details"></a>Details werkregel

[!include [banner](../includes/banner.md)]

De pagina **Details werkregel** geeft een uitgebreide, sorteerbare en filterbare lijst met afzonderlijke werkregels in het systeem weer. Het bevat een volledig overzicht van het werk dat wordt gepland en uitgevoerd in het magazijn. U kunt eenvoudig schakelen tussen het weergeven van alle werkregels en het weergeven van alleen openstaande werkregels. Details die voor elke regel worden opgegeven zijn onder andere de werkstatus, het artikelnummer, de locatie, de werkhoeveelheid, de lading-id en de zending-id.

## <a name="turn-on-the-work-line-details-feature"></a>De functie Details werkregel inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Details werkregel*

## <a name="open-and-use-the-work-line-details-page"></a>De pagina Details werkregel openen en gebruiken

Als u de lijst met details van werkregels wilt weergeven, gaat u naar **Magazijn beheer \> Werk \> Details werkregel**. Van hieruit kunt u de volgende acties uitvoeren:

- Met het veld **Filteren** zoeken naar regels met een specifieke waarde voor elke beschikbare parameter. (Houd er rekening mee dat er veel parameters beschikbaar zijn die niet als kolommen in het raster worden getoond.)
- Het selectievakje **Gesloten weergeven** gebruiken om gesloten regels weer te geven of te verbergen.
- **Dimensies weergeven** selecteren om het dialoogvenster **Weergave van dimensies** te openen, waar u diverse dimensiekolommen in het raster zichtbaar kunt maken of verbergen.
- Een kolomkop selecteren om een menu te openen waarin u kunt kiezen of u de lijst wilt sorteren of filteren op waarden in die kolom.
- Een werkregel selecteren en vervolgens **Locatie wijzigen** selecteren om een dialoogvenster te openen waarin u de locatie voor die werkregel kunt wijzigen. De locatie die u opgeeft, vervangt de instelling van de locatie-instructie.
- Een werkregel selecteren en **Werkregel annuleren** selecteren om een dialoogvenster te openen waarin u de hoeveelheid van de werkregel gedeeltelijk of volledig kunt reduceren.
- Hoeveelheden corrigeren.
- De transacties achter een werkregel weergeven.

## <a name="try-out-the-feature"></a>De functie uitproberen

Deze sectie bevat een demo met drie onderdelen waarin u kunt zien hoe u werkt met details van werkregels.

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u deze scenario's wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

U kunt deze demo ook gebruiken als instructie wanneer u met een productiesysteem werkt. U moet dan echter uw eigen waarden vervangen en hebt u mogelijk niet de beschikking over bepaalde typen vereiste records die met de standaard demogegevens worden verstrekt.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Controleren of in de scenarioconfiguratie voldoende voorhanden voorraad is opgenomen

Als u werkt met de **USMF-** voorbeeldgegevens, moet u eerst controleren of uw systeem zo is geconfigureerd dat op elke relevante verzamellocatie voldoende voorraad aanwezig is. Voor deze demo wordt er vanuit gegaan dat de volgende voorraad beschikbaar is:

- **Artikel M9200:** 45 ea. (or meer)
- **Artikel M9202:** 10 ea. (or meer)

Voer de volgende stappen uit om te controleren of voldoende voorraad beschikbaar is en om eventuele vereiste wijzigingen aan te brengen.

1. Ga naar **Magazijnbeheer \> Instellingen \> Locatie-instructies** en bepaal welke orderverzamellocaties worden gebruikt voor het orderverzamelen van verkoop orders in magazijn 51. (Zie voor meer informatie [Aanvulling en Magazijnwerk beheren met werksjablonen en locatierichtlijnen](control-warehouse-location-directives.md).)
1. Controleer de voorraadniveaus op de relevante locaties.
1. Pas de voorraad zo nodig aan. U kunt handmatige verplaatsingen maken en aanvulling of elke andere stroom toepassen om de voorraad aan te passen.

### <a name="part-1-create-picking-work"></a>Deel 1: Orderverzamelingswerk maken

Voordat u werk gaat maken, moet u controleren of het magazijn is geconfigureerd om op de verwachte manier te reageren op werkaanvragen.

Volg deze stappen om verzamelwerk te maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer de optie **Nieuw** om het dialoogvenster **Verkooporder maken** te openen.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - Stel op het sneltabblad **Klant** het veld **Klantaccount** in op _US-001_.
    - Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op _51_.

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Deze bevat een nieuwe lege rij in het raster **Verkooporderregels**. Stel de volgende waarden in voor deze orderregel:

    - **Artikelnummer:** _M9200_
    - **Hoeveelheid:** _20_
    - **Eenheid:** _EA_

1. Selecteer de nieuwe orderregel en selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering** om de pagina **Reservering** te openen.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**. Het systeem maakt een zending, voegt deze toe aan een nieuwe lading en maakt het vereiste werk.
1. Maak een tweede verkooporder voor dezelfde klantaccount en hetzelfde magazijn die u voor de eerste order hebt gebruikt. Voeg aan deze order de volgende twee orderregels toe:

    - **Regel 1:** Stel op de nieuwe regel het veld **Artikelnummer** in op _M9200_ en het veld **Hoeveelheid** op _25_ en het veld **Eenheid** op _EA_.
    - **Regel 2:** Stel op de nieuwe regel het veld **Artikelnummer** in op _M9202_ en het veld **Hoeveelheid** op _10_ en het veld **Eenheid** op _EA_.

1. Herhaal stap 6 tot en met 8 om de voorraad voor elke orderregel te reserveren (één voor één) en herhaal stap 9 om de order vrij te geven naar het magazijn.

### <a name="part-2-change-the-location-for-a-work-line"></a>Deel 2: De locatie voor een werkregel wijzigen

1. Ga naar **Magazijnbeheer \> Instellingen \> Details werkregel**.
1. Zoek en selecteer een van de werkregels die u voor deze demo hebt gemaakt.
1. Selecteer **Locatie wijzigen** om het dialoogvenster **Nieuwe locatie selecteren** te openen.
1. Selecteer in het dialoogvenster **Nieuwe locatie selecteren** in het veld **Locatie** een nieuwe locatie voor de werkregel.
1. Selecteer **OK** om de wijziging toe te passen en het dialoogvenster te sluiten.

> [!IMPORTANT]
> U kunt locatiewijzigingen alleen indienen als op de nieuwe locatie voldoende voorraad beschikbaar is (voor orderverzamelen) of als validatie op locatietype slaagt (voor wegzetten).

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>Deel 3: De hoeveelheid van een werkregel wijzigen of een werkregel annuleren

1. Ga naar **Magazijnbeheer \> Instellingen \> Details werkregel**.
1. Zoek en selecteer een van de werkregels die u voor deze demo hebt gemaakt. U kunt alleen hoeveelheden voor werkregels annuleren of wijzigen als het werk type _Orderverzamelen_ is.
1. Selecteer **Werkregel annuleren** om het dialoogvenster **Te annuleren hoeveelheid** te openen.
1. Wijzig in het dialoogvenster **Te annuleren hoeveelheid** de waarde in het veld **Hoeveelheid** om de hoeveelheid op te geven die moet worden *afgetrokken van* de hoeveelheid die op dat moment is opgegeven voor de regel. Standaard wordt in het veld **Hoeveelheid** de volledige hoeveelheid weergegeven.

    - Als u de volledige hoeveelheid annuleert, wordt de waarde van de **werkstatus** gewijzigd in _Geannuleerd_ , maar wordt in het veld **Werkhoeveelheid** nog steeds de oorspronkelijke waarde weergegeven.
    - Als u slechts een deel van de hoeveelheid annuleert, wordt de waarde in het veld **Werkhoeveelheid** bijgewerkt naar de nieuwe waarde, maar verandert de waarde in het veld **Werkstatus** niet.

1. Selecteer **OK** om de wijziging toe te passen en het dialoogvenster te sluiten.

> [!IMPORTANT]
> Als u slechts een deel van de hoeveelheid voor een werkregel annuleert, moet u ook de verouderde hoeveelheid uit de ladingregel verwijderen. Als u dit niet doet, kan de ladingregel niet worden bevestigd voor verzending, tenzij minderlevering op de juiste manier is ingesteld.
