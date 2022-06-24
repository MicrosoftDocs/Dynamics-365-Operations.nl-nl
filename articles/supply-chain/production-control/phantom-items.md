---
title: Phantom-artikelen
description: In dit artikel wordt beschreven hoe het regeltype Phantom kan worden gebruikt voor de regels van een stuklijst en een formule in Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 64139873216decd8ecb2fcaf1f284e726c53c332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893318"
---
# <a name="phantom-items"></a>Phantom-artikelen

[!include [banner](../includes/banner.md)]

In dit artikel wordt gedetailleerd beschreven hoe het regeltype Phantom kan worden gebruikt voor de regels van een stuklijst en een formule.

In afbeelding 1 is (a) de stuklijst voor het product H en de onderdelen F en G, en is (b) het routeblad voor product H en onderdeel F.

![Afbeelding 1: Technische stuklijst.](media/product-H-part-F.png)
*Afbeelding 1: Technische stuklijst*

In afbeelding 1 wordt een voorbeeld van een stuklijststructuur op twee niveaus weergegeven. Eindproduct H staat voor een product voor een machinemontage. De machinemontage bestaat uit twee delen, een elektrische eenheid (F) met twee materialen (A en B) en een groep van verpakkingsmaterialen (G), eveneens met twee materialen (C en D). Een ander materiaal (E) wordt gebruikt tijdens de algehele montage van de machine.

In afbeelding 1 wordt de technische stuklijst voor product H weergegeven. Deze structuur biedt een goed overzicht van de onderdelen en componenten van de totale montage van de machine. Hoewel productontwerpers de stuklijst misschien het liefst zo weergeven, komt deze structuur mogelijk niet exact overeen met de manier waarop de machine op de werkvloer wordt gebouwd.

In de technische stuklijst in afbeelding 1 wordt bijvoorbeeld aangegeven dat de elektrische eenheid F als afzonderlijk onderdeel in een afzonderlijke werkorder wordt gemonteerd. Op de werkvloer kan echter worden geconcludeerd dat het beter is om de elektrische eenheid als onderdeel van de algehele machinemontage te monteren, niet als aparte werkorder.

In deze elektrische stuklijst wordt onderdeel G ook als afzonderlijk onderdeel aangeduid. In deze structuur vertegenwoordigt onderdeel G echter geen fysiek onderdeel, maar een verzameling verpakkingsmaterialen.

Dus hoewel een technische stuklijst geweldige waarde voor het ontwerp van een product en het onderhoud van dat ontwerp biedt, is het mogelijk niet de meest logische manier om het productregistratieproces van het product te ondersteunen. Een productiestuklijst vertegenwoordigt daarentegen de beste manier om een product te bouwen.

In afbeelding 2 ziet u hoe de voorgaande technische stuklijst overgaat in een productiestuklijst. In afbeelding 2 is (a) de stuklijst voor product H en is (b) het routeblad voor product H.

![Afbeelding 2: Productiestuklijst.](media/product-H-part-B.png)
*Afbeelding 2: Productiestuklijst*

In deze structuur ziet u dat onderdelen F en G ontbreken en dat de materialen waaruit deze onderdelen bestaan naar het volgende stuklijstniveau zijn overgebracht.

In tegenstelling tot de technische stuklijst, die twee bewerkingsbladen had, heeft de productiestuklijst slechts één bewerkingsblad. De verpakkingsbewerking die aan onderdeel G was gekoppeld, is ook overgebracht en maakt nu deel uit van het bewerkingsblad voor product H. De montage van de elektrische eenheid is de eerste bewerking. Deze volgorde is logisch omdat deze eenheid wordt gebruikt in de volgende bewerking, de machinemontage. De laatste bewerking is de verpakkingsbewerking, waarbij twee verpakkingsmaterialen (C en D) worden verbruikt.

De overgang tussen de Engineering-stuklijst en de Productie-stuklijst wordt mogelijk door het regeltype Phantom-stuklijst. Met de term phantom wordt aangegeven dat de onderdelen F en G tijdens de overgang tussen de twee stuklijsttypen zijn verdwenen. In dit voorbeeld wordt het phantom-regeltype toegepast op de stuklijstregels voor onderdelen F en G in de technische stuklijst. Wanneer een productie- of batchorder wordt gemaakt, wordt de technische stuklijst gekopieerd naar de productie- of batchorder. Wanneer de order vervolgens wordt geraamd, vindt de overgang van de technische stuklijst naar de productiestuklijst plaats, zoals in afbeelding 2 wordt weergegeven. Van het verpakkingsblad in afbeelding 2 worden de verpakkingsmaterialen C en D ingevoerd voor de bewerking.

## <a name="multilevel-phantom-bom-structures"></a>Phantom-stuklijststructuren met meerdere niveaus

Het phantom-regeltype kan worden gebruikt in stuklijststructuren met meerdere niveaus, zoals in afbeelding 3 wordt weergegeven. In afbeelding 3 is (a) de stuklijst voor product G en is (b) het routeblad voor de onderdelen E en F, en product G.

![Afbeelding 3: Technische stuklijst onderdeel G.](media/product-G.png)
*Afbeelding 3: Technische stuklijst onderdeel G*

In afbeelding 4 ziet u de resulterende productiestuklijst en het routeblad als de stuklijstregels voor onderdelen E en F zo worden geconfigureerd dat het regeltype Phantom is. In afbeelding 4 is (a) de stuklijst voor product G en is (b) het routeblad voor product G.

![Afbeelding 4: Productiestuklijst onderdeel G.](media/product-G-route-sheet-G.png)
*Afbeelding 4: Productiestuklijst onderdeel G*

## <a name="phantom-and-route-network"></a>Phantom en routenetwerk

Phantom-stuklijsten kunnen ook worden gebruikt voor een stuklijst met een routenetwerk. In een routenetwerk worden een of meer bewerkingen tegelijkertijd uitgevoerd. De afbeelding 5 bevat een voorbeeld van een routenetwerk dat wordt gebruikt in een stuklijst met meerdere niveaus. In afbeelding 5 is (a) de stuklijst voor product G en onderdeel F, en is (b) het routeblad voor product G en onderdeel F, dat een routenetwerk heeft.

![Afbeelding 5: Technische stuklijst onderdeel G, routenetwerk.](media/product-G-part-F.png)
*Afbeelding 5: Technische stuklijst onderdeel G, routenetwerk*

In afbeelding 6 is (a) de stuklijst voor product G en F, en is (b) het routeblad voor de onderdelen G en F.

![Afbeelding 6: Productiestuklijst onderdeel G, routenetwerk.](media/product-G-part-F-with-route-sheet.png)
*Afbeelding 6: Productiestuklijst onderdeel G, routenetwerk*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]