---
title: Kostentoewijzingsmethode
description: Dit artikel bevat richtlijnen voor het gebruik van de totale kostentoewijzing (TCA). TCA is een methode om de kosten te berekenen tussen het belangrijkste formuleartikel voor een batchorder en de coproducten die voor de formule zijn gedefinieerd.
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0abcb421eed20f1bca3b39b7d43abd9928f33eb2
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="total-cost-allocation-method"></a>Kostentoewijzingsmethode

[!include[banner](../includes/banner.md)]


Dit artikel bevat richtlijnen voor het gebruik van de totale kostentoewijzing (TCA). TCA is een methode om de kosten te berekenen tussen het belangrijkste formuleartikel voor een batchorder en de coproducten die voor de formule zijn gedefinieerd.

De totale kostentoewijzing (TCA) is een methode om de kosten te berekenen tussen het belangrijkste formuleartikel voor een batchorder en de coproducten die voor de formule zijn gedefinieerd. Deze methode is dynamisch. De kosten worden berekend als een gewogen gemiddelde tussen de hoeveelheden die gereed worden gemeld voor het formuleartikel en de coproducten. Wanneer TCA wordt gebruikt, hoeft u geen kostentoewijzingen te beoordelen voor elke batchorder. Als TCA niet wordt gebruikt, gebruikt de formuleberekening bestaande functionaliteit.

## <a name="using-tca-for-coproducts"></a>Totale kostentoewijzing (TKT) gebruiken voor coproducten
Hieronder staan enkele richtlijnen voor het gebruik van TCA voor coproducten:

-   Als u de schuifregelaar **Totale kostentoewijzing** instelt op **Ja** voor een formuleversie, moeten coproducten een kostprijs hebben die meer dan 0 (nul) is. De waarde kan worden opgehaald van de actieve kostprijsversie voor dezelfde locatie, of voor de eerste locatie voor een formule die niet sitespecifiek is. Deze voorwaarde wordt gevalideerd wanneer de formule wordt goedgekeurd.

    -   U hoeft niet handmatig kostentoewijzingspercentages in te voeren voor coproducten. In plaats daarvan stelt het systeem automatisch het kostentoewijzingspercentage vast als het gemiddelde van de actieve kostprijzen van coproducten. 
    -   U hoeft geen standaardkostprijs in te voeren voor niet-standaard kostenartikelen die coproducten zijn. Er zijn twee typen kostprijsberekeningsversies in het systeem: standaardkosten en geplande kosten 
    -   Als een artikel niet wordt gewaardeerd door de standaardwaarderingsmethode, adviseren wij u een actieve kostprijs te gebruiken in de geplande kostenversie. Deze prijs wordt gebruikt voor kostenraming, bijvoorbeeld stuklijstberekening raming van de productiekosten en terugvalprijs in het voorraadwaarderingsproces. 

-   Als u de schuifregelaar **Totale kostentoewijzing** instelt op **Ja** voor de formuleversie en de volgende condities waar zijn, is de kostentoewijzingsmethode **TCA** en is het percentage van kostentoewijzing ongewijzigd:
    -   U hebt coproducten toegevoegd.
    -   U hebt een andere kostentoewijzingsmethode voor de coproducten gebruikt.
-   Als u de schuifregelaar **Totale kostentoewijzing** instelt op **Nee** voor de formuleversie en de volgende condities waar zijn, wordt de kostentoewijzingsmethode gewijzigd in **Handmatig** en is het percentage van kostentoewijzing ongewijzigd:
    -   U hebt coproducten toegevoegd.
    -   Het percentage van kostentoewijzing is meer dan 0 (nul).
-   Voordat u een formuleberekening kunt uitvoeren, moet u de percentages van kostentoewijzing ramen. U kunt deze stap handmatig uitvoeren of met behulp van de optie **Geschatte kosten** op de pagina **Coproducten**. **Opmerking:** de optie **Geschatte kosten** is alleen beschikbaar wanneer de schuifregelaar **Totale kostentoewijzing** is ingesteld op **Ja** voor de formuleversie. U kunt de verwachte toewijzing weergeven als de hoeveelheden van de batchorder die als gereed worden gemeld, overeenkomen met hoeveelheden in de formule.
-   Wanneer een batchorder handmatig is gemaakt of een geplande batchorder wordt gefiatteerd, wordt de waarde van de schuifregelaar **Totale kostentoewijzing** voor de formuleversie gekopieerd naar de batchorder. Echter, u kunt deze instelling in de batchorder wijzigen. Als de schuifregelaar **Totale kostentoewijzing** is ingesteld op **Nee** voor de formuleversie en vervolgens wordt gewijzigd in **Ja** voor de batchorder, wordt de methode van kostentoewijzing voor elke regel die was ingesteld op **Handmatig**, gewijzigd in **TCA**. Een kostentoewijzing van **Geen** blijft ongewijzigd. Als de schuifregelaar **Totale kostentoewijzing** is ingesteld op **Ja** voor de formuleversie en vervolgens wordt gewijzigd in **Nee** voor de batchorder, wordt de methode van kostentoewijzing voor elk coproduct dat was ingesteld op het type **Productie**, gewijzigd in **Handmatig**. Elk geschat percentage van kostentoewijzing is ongewijzigd.
-   De pagina **Kostentoewijzing van coproducten** toont het berekende kostprijstoewijzingspercentage. U kunt deze pagina openen vanaf de pagina **Batchorder**. Deze informatie is handig wanneer producten en hoeveelheden die worden gemeld, afwijken van de geplande of gestarte hoeveelheden in de batchorder. Wanneer de kosten zijn voltooid, worden deze nieuwe percentagetoewijzingen vanuit TCA weergegeven op de pagina **Kostentoewijzing van coproducten**.

## <a name="calculating-the-burden-for-byproducts"></a>Overhead voor bijproducten berekenen
Het veld **Kostentoewijzing bijproduct** op de pagina **Coproducten** is een opsommingsveld dat alleen voor bijproducten wordt gebruikt. Voor coproducten is de waarde van dit veld altijd **Geen**. Voor bijproductregels definieert dit veld hoe het kostenbedrag voor de bijproductregel bij de totale kosten van de productie wordt opgeteld. De volgende opties zijn beschikbaar:

-   **Geen**: er wordt geen bedrag opgeteld bij de totale kosten van de productie voor deze bijproductregel.
-   **Percentage**: het kostenbedrag wordt berekend als percentage van de totale kosten van grondstoffen die worden verbruikt in de productie. Het percentage dat wordt gebruikt voor de berekening, wordt ingevoerd in het veld.
-   **Per reeks**: het kostenbedrag wordt berekend als een bedrag per standaardbatchgrootte van de productieorder. Dit bedrag is onafhankelijk van de gerapporteerde hoeveelheid in de productie. Het bedrag dat wordt gebruikt voor de berekening, wordt ingevoerd in het veld.
-   **Per hoeveelheid**: het kostenbedrag wordt berekend als een bedrag per gerapporteerde hoeveelheid van het formuleartikel in de productie. Het bedrag dat wordt gebruikt voor de berekening, wordt ingevoerd in het veld.





