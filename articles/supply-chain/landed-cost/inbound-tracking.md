---
title: Inkomende reizen en verzendcontainertrajecten traceren
description: In dit onderwerp wordt uitgelegd hoe u de pagina Inkomende tracering kunt gebruiken om de voortgang van uw reizen en verzendcontainertrajecten bij te houden.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 678f2b6cda0592e0393bb15f372cb4be84778932
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501241"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Inkomende reizen en verzendcontainertrajecten traceren

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Op de pagina **Inkomende tracering** kunt u de voortgang van uw reizen en verzendcontainertrajecten bijhouden. Elke reis en elk traject wordt uitgesplitst naar *activiteiten*, die elk een eigen rij op de pagina hebben. U kunt de pagina gebruiken om geschatte datums en werkelijke datums per activiteit weer te geven en in te voeren.

Normaal gesproken wordt bij deze activiteiten, afhankelijk van de instellingen in het [traceringscontrolecentrum](delivery-information-setup.md#tracking-control-center), automatisch de geschatte aankomstdatum op de eindbestemming weergegeven. Bovendien wordt de leveringsdatum of de bevestigde datum op de inkooporderregels meestal bijgewerkt met de einddatum, afhankelijk van de instellingen. Voor transferorderregels kunt u het systeem instellen om de ontvangstdatum bij te werken.

Als u de pagina **Inkomende tracering** wilt openen, gaat u naar **Francoprijzen \> Tracering \> Inkomende tracering**.

## <a name="filter-the-activities-list"></a>De lijst met activiteiten filteren

Met de velden **Reis** en **Verzendcontainer** boven aan de pagina **Inkomende tracering** kunt u de pagina filteren, zodat alleen activiteiten worden weergegeven die zijn gekoppeld aan de geselecteerde reis en/of verzendcontainer.

## <a name="update-tracking-information"></a>Traceringsgegevens bijwerken

Als u de planning voor een reis of een traject wilt bijwerken, voert u de begindatum van de eerste activiteit in. De geschatte einddatum van de laatste activiteit wordt vervolgens bijgewerkt. De instellingen voor elke etappe en trajectsjabloon in het [traceringscontrolecentrum](delivery-information-setup.md#tracking-control-center) bepalen de geschatte doorlooptijden. De geschatte einddatums gebruiken de doorlooptijd vanaf de begindatum van de activiteit. Wanneer de werkelijke einddatum wordt vastgelegd, wordt de begindatum van de volgende activiteit bijgewerkt naar dezelfde datum als de werkelijke einddatum van de vorige activiteit. De werkelijke doorlooptijd wordt bijgewerkt zodat de vergelijking en analyse kunnen worden uitgevoerd. U kunt extra opmerkingen in het veld **Opmerking** invoeren.

De volgorde van de activiteiten in het raster wordt bepaald door de volgorde van de etappes in de relevante trajectsjabloon. Als de volgorde van de etappes in het gekoppelde traject wordt gewijzigd, verandert ook de traceringscontrole.

U kunt de datums voor alle containers bijwerken door **Begindatum bijwerken** of **Werkelijke einddatum bijwerken** te selecteren in het actiedeelvenster. U kunt ook de datums per container invoeren voor de zending. Door deze aanpak is er meer flexibiliteit, omdat containers kunnen worden opgesplitst in een omgeving met meerdere trajecten.

## <a name="buttons-on-the-action-pane"></a>Knoppen in het actiedeelvenster

Met de knoppen in het actiedeelvenster van de pagina **Inkomende tracering** kunt u werken met inkomende reizen en trajecten. In de volgende tabel wordt beschreven welke knoppen beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Bewerken | Een reis of een traject van een verzendcontainer bewerken. |
| Nieuw | Een nieuwe reis of een traject van een verzendcontainer maken. |
| Delete | Een geselecteerde reis of een traject van een verzendcontainer verwijderen. |
| Begindatum bijwerken | De begindatum van een activiteit bijwerken voor alle containers in een reis. Wanneer de begindatum van een specifieke activiteit of etappe van een traject wordt bijgewerkt, worden de volgende geschatte begindatums bijgewerkt op basis van de opgegeven doorlooptijd. |
| Werkelijke einddatum bijwerken | De einddatum van een activiteit bijwerken voor alle containers in een reis. Wanneer de einddatum van een specifieke activiteit wordt bijgewerkt, worden de daaropvolgende activiteiten bijgewerkt op basis van de opgegeven doorlooptijd. |
| Activiteiten toevoegen | Handmatig een activiteit aan een reis toevoegen U kunt bijvoorbeeld een ontsmettingsactiviteit toevoegen. De toevoeging kan ertoe leiden dat de bevestigde leveringsdatum van de goederen in het vaartuig of de reis wordt gewijzigd. Wanneer een activiteit wordt toegevoegd aan het traject, worden de geschatte dagen pas ingevoerd als de begindatum van de etappe van een traject is bijgewerkt. |

## <a name="information-and-settings-on-the-overview-tab"></a>Informatie en instellingen op het tabblad Overzicht

Op het tabblad **Overzicht** wordt een lijst weergegeven met alle activiteiten die horen bij de container die u boven aan de pagina hebt geselecteerd. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke activiteit.

| Veld | Beschrijving |
|---|---|
| Etappe | De etappe-id voor de activiteit, zoals gedefinieerd door de trajectsjabloon. |
| Leveringsmethode | De verwachte leveringsmethode voor de activiteit. |
| Activiteit | In dit veld wordt meestal de taak of taken aangegeven die aan de activiteit is of zijn gekoppeld. Gebruikelijke voorbeelden zijn *Onderweg* en *Inklaring*. |
| Beschrijving | Een langere omschrijving van de activiteit. |
| Begindatum | Dit veld geeft in eerste instantie de geschatte begindatum van de activiteit weer. Nadat de werkelijke einddatum van de vorige activiteit is ingevoerd, wordt echter de werkelijke begindatum gebruikt. Dit veld wordt gebruikt om de geschatte einddatum te bepalen op basis van de doorlooptijd. |
| Geraamde einddatum | De waarde van dit veld wordt berekend op basis van de begindatum en doorlooptijd. U bewerkt de waarde meestal niet direct. |
| Werkelijke einddatum | Een gebruiker moet dit veld zo snel mogelijk bijwerken nadat de activiteit heeft plaatsgevonden. De werkelijke doorlooptijd wordt vervolgens bijgewerkt. |
| Geraamde dagen | De geschatte tijd (in dagen) die vereist is om de activiteit te voltooien. |
| Werkelijke dagen | De werkelijke tijd (in dagen) die vereist is om de activiteit te voltooien. |
| Notitie | Gebruik dit veld om diverse opmerkingen en details over de activiteit toe te voegen. |

## <a name="information-and-settings-on-the-general-tab"></a>Informatie en instellingen op het tabblad Algemeen

Op het tabblad **Algemeen** wordt informatie weergegeven over de etappe die is geselecteerd op het tabblad **Overzicht**. Hoewel het een aantal gegevens op het tabblad **Overzicht** herhaalt, bevat het ook extra informatie over de geselecteerde etappe.
