---
title: U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld
description: U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7b57d3151852c9a2880185b7d9414e4246b7efb6429fcfce04c7cdae4ee00e37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760919"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld

Foutcode: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Symptomen

Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:

> Enkele artikelen die nodig zijn voor lading %1 zijn nog niet verzameld en naar de uiteindelijke verzendlocatie verplaatst.

U kunt de zending voor de lading daarom nog niet bevestigen.

## <a name="cause"></a>Oorzaak

De lading of zending kan niet in de huidige status worden bevestigd, omdat mogelijk een van de volgende voorwaarden van toepassing is:

- Het gerelateerde werk is nog niet verzameld en naar de uiteindelijke verzendlocatie verplaatst.
- De verzamelde werkhoeveelheid komt niet overeen met de gemaakte werkhoeveelheid op de ladingsregel.
- De locatie-instructie is met de verpakkingslocatie geconfigureerd als de uiteindelijke verzendlocatie tijdens het gebruik van wavesjablonen voor containervorming.

## <a name="resolution"></a>Oplossing

Daarom bevindt de lading of zending zich momenteel in een staat waarbij de verzendingsbevestiging mislukt. Om dit probleem te verhelpen, voert u een van de volgende taken uit:

- Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.
- Annuleer de werk-id's die zijn gemaakt met de verpakkingslocatie als de uiteindelijke verzendlocatie, configureer de locatierichtlijn opnieuw en verzend de lading opnieuw.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen

Gebruik de volgende procedure om de ladingsregels te controleren en ervoor te zorgen dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer de ladingsregel op het sneltabblad **Laadregels**.
1. Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.
1. Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.
1. Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.
1. Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Annuleer de werk-id's die zijn gemaakt met de verpakkingslocatie als de uiteindelijke verzendlocatie, configureer de locatierichtlijn opnieuw en verzend de lading opnieuw

Gebruik de volgende procedure om de werk-id's te annuleren die de verpakkingslocatie hebben als definitieve wegzetlocatie, waarbij geautomatiseerde containervorming is ingesteld.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.
1. Het dialoogvenster **Werk annuleren** wordt geopend. In het veld **Werk-id** geeft de id op van het werk dat u wilt annuleren. De geselecteerde werk-id moet bij **Werkstatus** de waarde *Openstaand*, *In uitvoering*, *Geannuleerd*, *Gecombineerd* of *Afgesloten* hebben.
1. Selecteer **OK**.
1. Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.
1. Herhaal deze procedure zo nodig voor de andere werk-id's.

Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.

Gebruik de volgende procedure om de locatie-instructie opnieuw te configureren, zodat de verpakkingslocatie niet wordt gebruikt als de uiteindelijke verzendlocatie wanneer geautomatiseerde containerization is ingesteld voor de wavesjabloon.

1. Ga naar **Magazijnbeheer \> Instellen \> Locatie-instructies**.
1. Selecteer *Verkooporders* in het veld **Werkordertype**.
1. Hier kunt u de locatie-instructie selecteren die voor geautomatiseerde containvorming wordt gebruikt.
1. Selecteer op de werkbalk van het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.
1. Zoek in het dialoogvenster van de query-editor op het tabblad **Bereik** naar de rij waar **Veld** is ingesteld op *Locatieprofiel* en controleer of het veld **Criteria** voor die rij niet is ingesteld op een locatieprofiel met *Verpakking* als **Locatietype**. Pas het veld **Criteria** aan om de uiteindelijke wegzetlocatie te corrigeren.

Met de volgende procedure kunt u de lading opnieuw vrijgeven en werk-id's maken met de juiste uiteindelijke verzendlocatie.

1. Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.
1. Zoek in de sectie **Ladingen** de lading die moet worden vrijgegeven.
1. Selecteer **Vrijgeven \> Vrijgeven aan magazijn** op de werkbalk in de sectie **Laden** om de geselecteerde lading vrij te geven aan het magazijn.
1. Herhaal deze procedure zo nodig voor de andere ladingen.
