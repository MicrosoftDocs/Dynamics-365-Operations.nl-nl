---
title: Parameters voor automatisering van incassoproces configureren
description: In dit artikel worden de parameters beschreven die invloed hebben op geautomatiseerde incassoprocessen en worden richtlijnen gegeven voor het instellen ervan, zodat het geautomatiseerde proces voldoet aan uw bedoelingen en verwachtingen.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c5d0f801c47ef2d98d8ba410dc593bd7640839c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900037"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Parameters voor automatisering van incassoproces configureren

[!include [banner](../includes/banner.md)]

In dit artikel worden de parameters beschreven die invloed hebben op geautomatiseerde incassoprocessen en worden richtlijnen gegeven voor het instellen ervan, zodat het geautomatiseerde proces voldoet aan uw bedoelingen en verwachtingen. Voor meer informatie over het automatiseren van incassoprocessen zie [Automatisering van incassoproces](collections-process-automate.md).

## <a name="general"></a>Algemeen
Voer in **Percentage klanten per batchtaak** een getal in om het aantal batchtaken per geautomatiseerd proces te bepalen. Stel **Aanmaningen automatisch boeken** in op **Ja** zodat het actietype van de aanmaning de brief automatisch boekt tijdens de automatisering. Stel **Activiteiten maken voor automatisering** in op **Ja** om activiteiten voor niet-activiteitsactietypen te maken en af te sluiten om alle geautomatiseerde stappen voor een rekening weer te geven. Definieer het aantal dagen dat de incassohistorie wordt bewaard in **Aantal dagen om automatisering van incassoproces te behouden**. Wanneer een factuur de laatste stap van het incassoproces bereikt, wordt deze niet gebruikt voor het maken van toekomstige actietypen voor procesautomatisering als **Factuur uitsluiten na activeren van laatste processtap** is ingesteld op **Ja**. De volgende oudste factuur bepaalt de volgende stap voor procesautomatisering om ervoor te zorgen dat procesautomatiseringsacties voor incasso worden voortgezet. 

## <a name="payment-predictions"></a>Betalingsvoorspellingen
Vanaf versie 10.0.21 geven Voorspellingen voor klantbetalingen, in Finance insights, een prognose of een factuur op tijd, te laat of zeer laat wordt betaald. U kunt al deze categorieën configureren in Finance insights. Als wordt voorspeld dat facturen te laat worden betaald, is het belangrijk om het incassoproces te starten voor de vervaldatum van de factuur. Deze voorspellingen kunnen worden gebruikt om incassoactiviteiten te maken wanneer automatisering van incassoprocessen wordt uitgevoerd. Stel **Voorspellingen voor klantbetalingen inschakelen** in op **Ja** om prognoses van klantbetalingen te gebruiken om incassoactiviteiten te maken op basis van de waarschijnlijkheid dat de factuur te laat wordt betaald. 

Zie [Voorspellingen voor klantbetalingen](payment-insights-overview.md) voor meer informatie over voorspellingen van klantbetalingen en Finance insights.

Wanneer het model voor het voorspellen van klantbetalingen wordt uitgevoerd, wordt er een percentage toegewezen aan de voorspelling voor of de factuur op tijd, te laat of zeer laat wordt betaald. U kunt die informatie gebruiken om automatisch incassoactiviteiten te starten met behulp van Automatisering van incassoproces in gevallen waarin te late betaling wordt verwacht. U kunt deze percentages weergeven op de pagina **Betalingsvoorspellingen per klant** of **Betalingsvoorspellingen per transactie** onder **Crediteringen en aanmaningen > Aanmaningen**. 

Als de gemiddelde betalingsprognose voor een klantfactuur lager is dan het benchmarkpercentage, wordt er geen activiteit gemaakt. Als de betalingsprognose voor een klantfactuur groter dan of gelijk aan is het benchmarkpercentage, wordt er een activiteit gemaakt per klant. Voer voor **Voorspelling: Te laat** het **Benchmarkpercentage** in waarbij incassoprocesautomatisering incassoactiviteiten moet maken. Dit is een samengevoegde waarde van te laat en zeer laat. Selecteer een **Bedrijfsdocumentsjabloon** om te gebruiken voor de activiteit die is gemaakt, of om een nieuwe te maken. Hiermee worden **Type**, **Doel** en **Dagen tot activiteit gesloten** aangegeven. Voer **Opmerkingen** die worden gebruikt als omschrijving wanneer de activiteit wordt gemaakt. Voer voor **Voorspelling: Zeer laat** het **Benchmarkpercentage** in waarbij incassoprocesautomatisering incassoactiviteiten moet maken voor een klant voor wie wordt voorspeld dat deze facturen zeer laat betaalt. Selecteer een **Bedrijfsdocumentsjabloon** om te gebruiken voor de activiteit die wordt gemaakt. Hiermee worden **Type**, **Doel** en **Dagen tot activiteit gesloten** aangegeven. Voer **Opmerkingen** die worden gebruikt als omschrijving wanneer de activiteit wordt gemaakt. 

### <a name="example"></a>Voorbeeld
Als het benchmarkpercentage voor te laat is ingesteld op 60%. Wanneer voorspellingen van klantbetalingen worden uitgevoerd voor elke factuur, wordt er een percentage toegewezen aan de voorspelling voor of de factuur op tijd, te laat of zeer laat wordt betaald. Als de betalingsprognose dat de factuur te laat wordt betaald 59% of minder is, wordt er geen incassoactiviteit gemaakt voor de factuur door het automatische incassoproces. Als de voorspelling van de klantbetaling voor een factuur groter is dan of gelijk is aan 60%, wordt er een incassoactiviteit gemaakt door het automatische incassoproces. 

> [!NOTE]
> De zeer late voorspelling wordt geëvalueerd vóór de te late voorspelling, omdat onder zeer laat ook facturen vallen die naar verwachting te laat worden betaald. Het incassoproces genereert slechts één activiteit als de factuur zowel in de benchmark Te laat als de benchmark Zeer laat valt. In dat geval worden de activiteit en het bedrijfsdocument voor zeer laat gebruikt, omdat zeer laat een hogere prioriteit heeft. Acties die al eerder zijn gegenereerd, worden niet voor een tweede keer gegenereerd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
