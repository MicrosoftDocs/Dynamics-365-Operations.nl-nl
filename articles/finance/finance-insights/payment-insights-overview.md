---
title: Voorspellingen voor klantbetalingen
description: In dit artikel wordt beschreven hoe u betalingsvoorspellingen kunt gebruiken om de gebruikelijke betalingsmethoden van klanten beter te begrijpen. De functie kan helpen om omstandigheden te identificeren die kunnen rechtvaardigen dat incassoprocessen eerder worden begonnen dan normaal gesproken.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 5d16b42b4538a18ca3dd9d3bac25ed1af1441ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903155"
---
# <a name="customer-payment-predictions"></a>Voorspellingen voor klantbetalingen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u betalingsvoorspellingen kunt gebruiken om de gebruikelijke betalingsmethoden van klanten beter te begrijpen. De functie kan helpen om omstandigheden te identificeren die kunnen rechtvaardigen dat incassoprocessen eerder worden begonnen dan normaal gesproken.

## <a name="overview"></a>Overzicht

Organisaties vinden het vaak lastig om te voorspellen wanneer klanten hun facturen betalen. Dit gebrek aan inzichten kan de volgende problemen veroorzaken:

- Minder nauwkeurige cashflowprognoses
- Incassoprocessen die te laat beginnen
- Orders die worden vrijgegeven aan klanten die mogelijk verzuimen te betalen

Voorspellingen van klantbetalingen helpt organisaties te voorspellen wanneer een klantfactuur wordt betaald. Daarom kunnen zij incassostrategieën maken die helpen de kans te vergroten dat ze op tijd worden betaald.

## <a name="predictions"></a>Voorspellingen

Met betalingsvoorspellingen kunnen organisaties hun bedrijfsprocessen verbeteren doordat ze de facturen kunnen identificeren die waarschijnlijk te laat worden betaald. De organisatie kan die informatie gebruiken om acties uit te voeren die de kans vergroten dat ze op tijd worden betaald.

De functie voorspellingen van klantbetalingen gebruikt een Machine Learning-model om nauwkeuriger te voorspellen wanneer een klant een openstaande factuur betaalt. Dit Machine Learning-model bevat historische facturen, betalingen en klantgegevens.

Voor elke openstaande factuur wijst de functie drie betalingskansen toe:

- De waarschijnlijkheid dat de betaling op tijd wordt uitgevoerd
- De waarschijnlijkheid dat de betaling te laat wordt uitgevoerd
- De waarschijnlijkheid dat de betaling zeer laat wordt uitgevoerd

De functie biedt ook een totaaloverzicht van de verwachte betalingen.

[![Samengevoegde weergave van betalingsvoorspellingen.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Aan elke factuur wordt een waarschijnlijkheid van tijdige betaling toegewezen. Facturen waarvan de waarschijnlijkheid van tijdige betaling minder dan 50% is, worden gelabeld met een rode cirkel om aan te geven dat er mogelijk een incassomedewerker naar moet kijken.

[![Lijst met betalingswaarschijnlijkheden.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

De functie Voorspellingen van klantbetalingen biedt ook contextuele informatie om de voorspelling uit te leggen. Deze informatie bevat de belangrijkste factoren die invloed hebben op de voorspelling, de huidige status van zaken met de klant en details over het historische betalingsgedrag van de klant.

In veel bedrijven is het incassoproces een reactieve activiteit. Met andere woorden, het incassoproces begint pas op de uiterste betaaldatun van facturen. Met Voorspellingen van klantbetalingen kunnen organisaties proactiever omgaan met incasso's. Ze hoeven niet meer te wachten tot een transactie verschuldigd is om het incassoproces te starten. In plaats daarvan kunnen ze de functie voor betalingsvoorspellingen gebruiken om te bepalen of proactieve incasso's de kans op tijdige betaling vergroten.

## <a name="methodology"></a>Methodologie

In het verleden was het doorgaans moeilijk om een oplossing met kunstmatige intelligentie te ontwikkelen en te implementeren. Voor het proces was een team vereist met gegevenswetenschappers, deskundigen en ingenieurs, die gedurende langere tijd samenwerken om een bruikbare AI-oplossing te formuleren, te ontwikkelen, te implementeren en te onderhouden. Met Voorspellingen van klantbetalingen kunt u eenvoudig een AI-oplossing implementeren en gebruiken in Microsoft Dynamics 365 Finance. Microsoft neemt AI-oplossingen op die zijn gebouwd op basis van Microsoft AI Builder. Daarom kunnen gebruikers de AI-oplossing met één muisklik implementeren om voordeel te halen uit intelligente voorspellingen. Als u niet tevreden bent over de nauwkeurigheid van voorspellingen, kan een hoofdgebruiker (met één klik op de muisknop) opnieuw het AI Builder-hulpprogramma openen en vervolgens de velden voor het genereren van voorspellingen selecteren of wissen. Wanneer u klaar bent, kunt u het model 'trainen' en de wijzigingen publiceren. Het nieuwe getrainde model wordt automatisch opgehaald om voorspellingen te genereren in Dynamics 365 Finance.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
