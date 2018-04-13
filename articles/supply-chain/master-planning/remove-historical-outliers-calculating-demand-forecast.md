---
title: Verwijder uitschieters uit historische transactiegegevens bij het berekenen van een vraagprognose
description: In dit artikel wordt beschreven hoe u uitschieters kunt verwijderen uit de historische gegevens die worden gebruikt om een vraagprognose te berekenen. Door uitschieters uit te sluiten, kunt u de prognosenauwkeurigheid verbeteren.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 714a892ff4c168ee3ba1cefd25ae18345af5631b
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Verwijder uitschieters uit historische transactiegegevens bij het berekenen van een vraagprognose

[!INCLUDE [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u uitschieters kunt verwijderen uit de historische gegevens die worden gebruikt om een vraagprognose te berekenen. Door uitschieters uit te sluiten, kunt u de prognosenauwkeurigheid verbeteren.

U kunt uitschieters uitsluiten om de prognosenauwkeurigheid te verbeteren. Deze taak is optioneel. Hier is een overzicht van het proces:

1.  Klik op **Hoofdplanning** &gt; **Instellen** &gt; **Vraagprognose** &gt; **Verwijdering van uitschieters** om de pagina **Verwijdering van uitschieters** te openen, waar u een query kunt gebruiken om de uit te sluiten transacties te selecteren.
2.  Selecteer het bedrijf waarop de query van toepassing is en geef een naam en een omschrijving op. Het veld **Querydatum** wordt automatisch ingesteld op de huidige datum.
3.  Schakel het selectievakje **Actief** in om de transacties die door de query worden gevonden uit de historische gegevens te verwijderen. Deze instelling is van kracht wanneer u een basislijnprognose maakt.
4.  Op de pagina **Query voor verwijdering van uitschieters** kunt u de criteria toevoegen, verwijderen en selecteren waarmee de transacties worden gedefinieerd die moeten worden uitgesloten wanneer de basislijnprognose wordt berekend. Selecteer bijvoorbeeld een bepaald artikel of een ordertransactie die u wilt uitsluiten.
5.  Klik op **Transacties weergeven**. Op de pagina **Transacties met uitschieters** worden de transacties weergegeven die voldoen aan de criteria die u in de query hebt gedefinieerd en die van de historische gegevens worden uitgesloten wanneer de vraagprognose wordt berekend.

**Opmerking:** u kunt ook een query maken die op een bestaande query is gebaseerd. Selecteer de query die u wilt kopiëren en klik op **Dupliceren**. Het veld **Querydatum** bevat de versie. U kunt de query zo gebruiken of klikken op **Query bewerken** om de criteria te wijzigen. U kunt de naam en omschrijving van de nieuwe query desgewenst wijzigen.

<a name="see-also"></a>Zie ook
--------

[Inleiding op vraagprognoses](introduction-demand-forecasting.md)

[Nauwkeurigheid van prognose bewaken](monitor-forecast-accuracy.md)




