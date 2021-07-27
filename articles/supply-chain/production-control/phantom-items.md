---
title: Phantom-artikelen
description: In dit onderwerp wordt gedetailleerd beschreven hoe het regeltype Phantom kan worden gebruikt voor de regels van een stuklijst en een formule in Dynamics 365 Supply Chain Management.
author: ShylaThompson
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: cb04502721740c48004b62bc96ff13ca063e06db
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360893"
---
# <a name="phantom-items"></a>Phantom-artikelen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt gedetailleerd beschreven hoe het regeltype Phantom kan worden gebruikt voor de regels van een stuklijst en een formule. In de volgende afbeelding is (a) de stuklijst voor het product H en de onderdelen F en G, en is (b) het routeblad voor product H en onderdeel F.

![Product H en onderdeel F.](media/product-H-part-F.png)


In deze afbeelding wordt een voorbeeld van een stuklijststructuur op twee niveaus weergegeven. Eindproduct H staat voor een product voor een machinemontage. De machinemontage bestaat uit twee delen, een elektrische eenheid (F) met twee materialen (A en B) en een groep van verpakkingsmaterialen (G), eveneens met twee materialen (C en D). Een ander materiaal (E) wordt gebruikt tijdens de algehele montage van de machine.

![Product H en onderdeel F.](media/product-H-part-B.png)

In de bovenstaande afbeelding wordt de technische stuklijst voor product H weergegeven. Deze structuur biedt een goed overzicht van de onderdelen en componenten van de totale montage van de machine. Hoewel productontwerpers de stuklijst misschien het liefst zo weergeven, komt deze structuur mogelijk niet exact overeen met de manier waarop de machine op de werkvloer wordt gebouwd. 

In de technische stuklijst wordt bijvoorbeeld aangegeven dat de elektrische eenheid F als afzonderlijk onderdeel in een afzonderlijke werkorder wordt gemonteerd. Op de werkvloer kan echter worden geconcludeerd dat het beter is om de elektrische eenheid als onderdeel van de algehele machinemontage te monteren, niet als aparte werkorder.

In deze elektrische stuklijst wordt onderdeel G ook als afzonderlijk onderdeel aangeduid. In deze structuur vertegenwoordigt onderdeel G echter geen fysiek onderdeel, maar een verzameling verpakkingsmaterialen. 

Dus hoewel een technische stuklijst geweldige waarde voor het ontwerp van een product en het onderhoud van dat ontwerp biedt, is het mogelijk niet de meest logische manier om het productregistratieproces van het product te ondersteunen. Een productiestuklijst vertegenwoordigt daarentegen de beste manier om een product te bouwen.

In de volgende afbeelding ziet u hoe de voorgaande technische stuklijst overgaat in een productiestuklijst. In deze afbeelding is (a) de stuklijst voor product H en is (b) het routeblad voor product H.

In deze structuur ziet u dat onderdelen F en G ontbreken en dat de materialen waaruit deze onderdelen bestaan naar het volgende stuklijstniveau zijn overgebracht. 

In tegenstelling tot de technische stuklijst, die twee bewerkingsbladen had, heeft de productiestuklijst slechts één bewerkingsblad. De verpakkingsbewerking die aan onderdeel G was gekoppeld, is ook overgebracht en maakt nu deel uit van het bewerkingsblad voor product H. De montage van de elektrische eenheid is de eerste bewerking. Deze volgorde is logisch omdat deze eenheid wordt gebruikt in de volgende bewerking, de machinemontage. De laatste bewerking is de verpakkingsbewerking, waarbij twee verpakkingsmaterialen (C en D) worden verbruikt.

De overgang tussen de Engineering-stuklijst en de Productie-stuklijst wordt mogelijk door het regeltype Phantom-stuklijst. Met de term phantom wordt aangegeven dat de onderdelen F en G tijdens de overgang tussen de twee stuklijsttypen zijn verdwenen. In dit voorbeeld wordt het phantom-regeltype toegepast op de stuklijstregels voor onderdelen F en G in de technische stuklijst. Wanneer een productie- of batchorder wordt gemaakt, wordt de technische stuklijst gekopieerd naar de productie- of batchorder. Wanneer de order vervolgens wordt geraamd, vindt de overgang van de technische stuklijst naar de productiestuklijst plaats, zoals in de voorgaande afbeeldingen wordt weergegeven. Van het verpakkingsblad in de tweede afbeelding worden de verpakkingsmaterialen C en D ingevoerd voor de bewerking. 

## <a name="multilevel-phantom-bom-structures"></a>Phantom-stuklijststructuren met meerdere niveaus
Het phantom-regeltype kan worden gebruikt in stuklijststructuren met meerdere niveaus, zoals in de volgende afbeelding wordt weergegeven. In deze afbeelding is (a) de stuklijst voor product G en is (b) het routeblad voor de onderdelen E en F, en product G. 

![Product G en onderdeel F met routebladen.](media/product-G-route-sheet-G.png)


In de volgende afbeelding ziet u de resulterende productiestuklijst en het routeblad als de stuklijstregels voor onderdelen E en F zo worden geconfigureerd dat het regeltype Phantom is. In deze afbeelding is (a) de stuklijst voor product G en is (b) het routeblad voor product G.

![Product G.](media/product-G.png)


## <a name="phantom-and-route-network"></a>Phantom en routenetwerk
Phantom-stuklijsten kunnen ook worden gebruikt voor een stuklijst met een routenetwerk. In een routenetwerk worden een of meer bewerkingen tegelijkertijd uitgevoerd. De volgende afbeelding bevat een voorbeeld van een routenetwerk dat wordt gebruikt in een stuklijst met meerdere niveaus. In deze afbeelding is (a) de stuklijst voor product G en onderdeel F, en is (b) het routeblad voor product G en onderdeel F, dat een routenetwerk heeft.

![Product G en onderdeel F.](media/product-G-part-F.png)


In de volgende afbeelding is (a) de stuklijst voor het product G en onderdeel F, en is (b) het routeblad voor product G en onderdeel F.

![Product G en onderdeel F met routebladen.](media/product-G-part-F-with-route-sheet.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]