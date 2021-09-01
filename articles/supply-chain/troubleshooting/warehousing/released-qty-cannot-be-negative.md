---
title: Kan een laadregel niet bijwerken omdat de vrijgegeven hoeveelheid dan negatief wordt
description: Dit probleem treedt op wanneer het bijwerken of verwijderen van een ladingsregel tot een negatieve vrijgegeven hoeveelheid leidt.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728454"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Kan een laadregel niet bijwerken omdat de vrijgegeven hoeveelheid dan negatief wordt

Foutcode: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Symptomen

Dit probleem treedt op wanneer het bijwerken of verwijderen van een ladingsregel tot een negatieve vrijgegeven hoeveelheid leidt. Wanneer u in dit geval probeert de ladingsregel bij te werken of te verwijderen, wordt het volgende foutbericht weergegeven:

> Vrijgegeven hoeveelheid kan niet negatief zijn voor artikel %1, partij %2.

U kunt de ladingsregel daarom niet bijwerken of verwijderen.

## <a name="cause"></a>Oorzaak

Nadat u een ladingsregel hebt bijgewerkt of verwijderd, wordt de vrijgegeven hoeveelheid van de gerelateerde verkoopregel *(whsSalesLine.ReleaseQty)* door het systeem bijgewerkt. Het systeem evalueert de vrijgegeven hoeveelheid en als wordt vastgesteld dat de vrijgegeven hoeveelheid van de regel negatief is na de update, kunt u de regel niet bijwerken of verwijderen. Deze validatie wordt uitgevoerd wanneer u de hoeveelheid van de ladingsregel of de maateenheid wilt bijwerken via verschillende acties, zoals het verwijderen van een ladingsregel, het verwijderen van een zending, het wijzigen van de hoeveelheid van een ladingsregel, het verminderen van de verzamelde hoeveelheid en kort orderverzamelen.

De meest voorkomende hoofdoorzaak van dit probleem is een wijziging in de eenheidsomrekening die wordt gebruikt voor openstaande ladingsregels. De eenheidsomrekening op het moment dat de verkooporder werd vrijgegeven, was bijvoorbeeld *50 st. = 1 PL*. Voordat de bijbehorende zending werd afgerond, werd de eenheidsomrekening echter gewijzigd in *100 st. = 1 PL*.

## <a name="resolution"></a>Oplossing

De oplossing is door de wijzigingen in de eenheidsomrekening terug te draaien, de ladingsregel bij te werken of te verwijderen en de omrekening vervolgens opnieuw implementeren. U moet ervoor zorgen dat andere ladingen die het item bevatten die het probleem veroorzaakte, pas worden verwerkt wanneer het probleem is opgelost. Anders kunnen de nieuwe omrekeningen worden gebruikt voor andere ladingen die al openstaan.

Om dit probleem te verhelpen, voert u de volgende taken uit:

1. Controleer de eenheidsomrekening die voor de ladingsregel is gebruikt.
2. Controleer de huidige eenheidsomrekening voor het item en breng wijzigingen aan die ervoor zorgen dat de ladingsregel kan worden bijgewerkt of verwijderd.
3. Werk de ladingsregel bij of verwijder de regel en maak de wijzigingen in de eenheidsomrekening ongedaan.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>De eenheidsomrekening controleren die voor de ladingsregel is gebruikt

Gebruik de volgende procedure om uw ladingsregels te controleren en maak een notitie van de eenheidsomrekening die voor de ladingsregel is gebruikt.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading met de ladingsregel die niet kan worden verwijderd of bijgewerkt.
1. Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.
1. Selecteer in het bovenste raster de relevante werk-id.
1. Bereken op het tabblad **Algemeen** onderaan de pagina de conversieverhouding tussen de waarde van de **Hoeveelheid werkvoorraad** en de waarde van de **Werkhoeveelheid**. Noteer de verhouding.
1. Herhaal deze procedure voor alle relevante werk-id's om ervoor te zorgen dat dezelfde omrekening is gebruikt.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>De huidige eenheidsomrekening voor het item controleren en correcties aanbrengen

Gebruik de volgende procedure om de eenheidsomrekening van uw product te controleren en breng correcties aan om ervoor te zorgen dat de eenheidsomrekening wordt afgestemd op de ladingsregel.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Open het relevante product om naar de bijbehorende pagina **Vrijgegeven productdetails** te gaan.
1. Selecteer in het Actievenster op het tabblad **Product** in de groep **Instellen** de optie **Eenheidsomrekeningen**.
1. Selecteer de omrekening tussen de eenheden en breng correcties aan met behulp van de omrekening die u hebt gevonden in de vorige sectie.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>De ladingsregel bijwerken of verwijderen en de wijzigingen in de eenheidsomrekening ongedaan maken

Gebruik de volgende procedure om de ladingsregel indien nodig te verwerken en de eenheidsomrekeningen ongedaan te maken.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Open de lading met de ladingsregel die niet kan worden verwijderd of bijgewerkt.
1. Selecteer de ladingsregel op het sneltabblad **Laadregels**.
1. Voer indien nodig door de vereiste acties uit. (U kunt bijvoorbeeld de ladingsregel verwijderen of de hoeveelheid ervan wijzigen.)
1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Open het relevante product om naar de bijbehorende pagina **Vrijgegeven productdetails** te gaan.
1. Selecteer in het Actievenster op het tabblad **Product** in de groep **Instellen** de optie **Eenheidsomrekeningen**.
1. Selecteer de omrekening tussen de eenheden en maak de correcties ongedaan die in de vorige sectie hebt aangebracht.
